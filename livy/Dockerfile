ARG SPARK_COMMON
FROM ${SPARK_COMMON}
RUN apk add --no-cache bash procps
WORKDIR /livy
RUN wget "http://mirror.ox.ac.uk/sites/rsync.apache.org/incubator/livy/0.7.0-incubating/apache-livy-0.7.0-incubating-bin.zip"
RUN unzip apache-livy-0.7.0-incubating-bin.zip && rm apache-livy-0.7.0-incubating-bin.zip && mv apache-livy-0.7.0-incubating-bin/* ./
RUN mkdir /livy/logs
COPY ./livy.conf /livy/conf/
CMD ["/livy/bin/livy-server"]