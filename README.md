#Tutorial https://ci.apache.org/projects/flink/flink-docs-release-1.7/tutorials/local_setup.html
#Get Apache Flink

cd ~/Downloads        # Go to download directory
tar xzf flink-*.tgz   # Unpack the downloaded archive
cd flink-1.7.0

# Start a Local Flink Cluster
./bin/start-cluster.sh

# Check the Dispatcher’s web frontend at http://localhost:8081 and make sure everything is up and running.
# The web frontend should report a single available TaskManager instance.

#Check logs
tail log/flink-*-standalonesession-*.log

# Start local server 
nc -l 9000

# run SocketWindowWordCount with --port 9000
