FROM openjdk:11

ARG kafka_version=3.0.0
ARG kafka_home=/opt/kafka
ARG scala_version=2.13

ENV KAFKA_VERSION=$kafka_version
ENV SCALA_VERSION=$scala_version
ENV KAFKA_HOME=$kafka_home

# add kafka to path
ENV PATH=${PATH}:${KAFKA_HOME}/bin

# download and install kafka
RUN curl "https://dlcdn.apache.org/kafka/${KAFKA_VERSION}/kafka_${SCALA_VERSION}-${KAFKA_VERSION}.tgz" -o /tmp/kafka_${SCALA_VERSION}-${KAFKA_VERSION}.tgz \
 && tar xfz /tmp/kafka_${SCALA_VERSION}-${KAFKA_VERSION}.tgz -C /opt \
 && rm /tmp/kafka_${SCALA_VERSION}-${KAFKA_VERSION}.tgz \
 && ln -s /opt/kafka_${SCALA_VERSION}-${KAFKA_VERSION} ${KAFKA_HOME}

COPY start-zookeeper.sh /usr/bin

RUN chmod +x /usr/bin/start-zookeeper.sh

CMD ["start-zookeeper.sh"]

