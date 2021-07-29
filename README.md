# WordCount

Running word count program on hadoop

# Start all services:

:~$ start-all.sh

# Check if they are on:

:~$ jps

# Create directory :

$ hadoop fs -mkdir /wordcountpython/input/

# Upload input.txt file in input directory on hadoop:

$ hadoop fs -put /home/neo/Downloads/input.txt /wordcountpython/input

# To check the content of the directory on hadoop:

$ hadoop fs -ls /wordcountpython/input

# Execution :

$ hadoop jar/home/neo/Programs/WordCount/hadoop-streaming-2.7.3.jar -file /home/neo/Programs/WordCount/mapper.py -mapper "python3 mapper.py" -file /home/neo/Programs/WordCount/reducer.py -reducer "python3 reducer.py" -input /wordcountpython/input -output /wordcountpython/output

**** delete the output dir if rerunning again and its throwing error
