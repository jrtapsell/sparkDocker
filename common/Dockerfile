# Use Java 8
FROM openjdk:8-alpine
# Install needed tools
RUN apk --no-cache --update add wget tar bash file python3
# Download Spark
RUN wget "http://mirror.ox.ac.uk/sites/rsync.apache.org/spark/spark-2.4.5/spark-2.4.5-bin-hadoop2.7.tgz"
# Check file type
RUN file spark-2.4.5-bin-hadoop2.7.tgz
# Extract spark
RUN tar -xzf spark-2.4.5-bin-hadoop2.7.tgz && \
    mv spark-2.4.5-bin-hadoop2.7 /spark && \
    rm spark-2.4.5-bin-hadoop2.7.tgz
ENV SPARK_HOME="/spark/"
ENV PYSPARK_PYTHON="/usr/bin/python3"