To run the script automatically on a weekly basis using Hue, you can use a scheduling tool such as Oozie. Here are the general steps to set up the scheduling:

Create a new workflow in Oozie and add a coordinator to schedule the workflow.
In the coordinator configuration, specify the frequency of the scheduling (e.g., weekly), the start and end times, and the timezone.
Add an action to the workflow that runs the shell script with the database name as a parameter.
Upload the script to HDFS or a shared location accessible from the Hue cluster.
Set the appropriate permissions on the script and any necessary files (e.g., the password file).
Test the workflow to ensure it runs correctly and produces the desired output.
Note that the exact steps may vary depending on your specific setup and requirements. You may need to consult the documentation or seek further assistance from a Hadoop administrator or consultant.