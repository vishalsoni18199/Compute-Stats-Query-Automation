Working of the script=>
---------------------
1. This script takes that Database name as input parameter,
      (for example: script.sh Database_name)
2. Runs a "show tables" query with this Database_name,
3. Concate the "compute stats" with each table that are found from previous query,
4. and create a file with previous concatination output and save it in .sql file
      (for example: compute stats Table_name,....(more tables) and save it in output.sql file.)
5. Runs this output.sql file,
6. If you want to add logging in this the command attached with this script just uncomment that part and use this.
7. Show the message after the successful runs.

================================================================================================================================================================

To run the script automatically on a weekly basis using Hue, you can use a scheduling tool such as Oozie. Here are the general steps to set up the scheduling:

  1. Create a new workflow in Oozie and add a coordinator to schedule the workflow.
  2. In the coordinator configuration, specify the frequency of the scheduling (e.g., weekly), the start and end times, and the timezone.
  3. Add an action to the workflow that runs the shell script with the database name as a parameter.
  4. Upload the script to HDFS or a shared location accessible from the Hue cluster.
  5. Set the appropriate permissions on the script and any necessary files (e.g., the password file).
  6. Test the workflow to ensure it runs correctly and produces the desired output.
    --Note that the exact steps may vary depending on your specific setup and requirements. You may need to consult the documentation or seek further assistance from a   Hadoop administrator or consultant.


