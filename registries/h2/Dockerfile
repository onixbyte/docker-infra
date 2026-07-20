# Use a lightweight JRE base image
FROM amazoncorretto:21-alpine

# Define the H2 database version
ARG H2_VERSION=2.3.232

# Set up environment variables for the data directory
ENV H2_DATA=/opt/h2-data

# Create the necessary directories and set the working directory
RUN mkdir -p ${H2_DATA}
WORKDIR /opt/h2

# Download the H2 database JAR file
RUN wget -q "https://repo1.maven.org/maven2/com/h2database/h2/${H2_VERSION}/h2-${H2_VERSION}.jar" -O h2.jar

# Expose the standard ports:
# 8082: Web Console
# 9092: TCP Server
EXPOSE 8082 9092

# Define a volume to persist the database files, preventing data loss on container restart
VOLUME ${H2_DATA}

# Set the command to initialise and start the H2 server
# -webAllowOthers authorises external connections to the web console
# -tcpAllowOthers authorises external TCP connections
# -baseDir specifies the centre of the data storage
# -ifNotExists allows creating a new database automatically
CMD ["java", "-cp", "h2.jar", "org.h2.tools.Server", \
     "-web", "-webAllowOthers", "-webPort", "8082", \
     "-tcp", "-tcpAllowOthers", "-tcpPort", "9092", \
     "-baseDir", "/opt/h2-data", \
     "-ifNotExists"]