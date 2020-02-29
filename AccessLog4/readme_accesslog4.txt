# Upload access_log file into hadoop folder in VM through SCP
# Make an input directory in hdfs

hdfs dfs -mkdir input1


# Put the access_log file in input1

hdfs dfs -put access_log input1

###############################################################

# Compile and build the jar file in intellij in the local system.

# Jar file is located in the out/artifacts folder.

# Move the file from local system to the hadoop folder in VM through SCP.

# Use the below command to run the jar file in the virtual server

bin/hadoop jar AccessLog4.jar  input1/ output/



###############################################################

# To check the output run

bin/hdfs dfs -cat output/*

###############################################################

# Delete the output directory

bin/hdfs dfs -rm -r output
###############################################################