#!/bin/bash
# get database name from user input
dbname=$1
# make sure database name is provided
if [ -z "$dbname" ]; then
  echo "Please provide the database name as a parameter"
  exit 1
fi
# run SQL query to get list of tables in database
tables=$(echo "SHOW TABLES" | mysql -N -u root $dbname)
# loop through list of tables and add "compute stats" to each tablename
for table in $tables; do echo "compute stats $table;" >> output.sql
done

#echo "Done! SQL file with compute stats commands has been created."

# execute output.sql file
mysql -u root $dbname < output.sql
#use "">> script_logs.txt 2>&1"" code if you want to add log file right after "output.sql"
echo "compute stats runs successfully."