# Make a sample file in VM at the hadoop directory

nano sample.txt

# Make an input directory in hdfs

hdfs dfs -mkdir input

# Put the sample file in input

hdfs dfs -put sample.txt input

###############################################################

# Compile and build the jar file in intellij in the local system.

# Jar file is located in the out/artifacts folder.

# Move the file from local system to the hadoop folder in VM through SCP.

# Use the below command to run the jar file in the virtual server

bin/hadoop jar NGram.jar  input/ output/ 2



###############################################################

# To check the output run

bin/hdfs dfs -cat output/*

###############################################################

# Delete the output directory

bin/hdfs dfs -rm -r output
###############################################################