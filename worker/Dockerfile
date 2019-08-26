FROM nogala/spark-base:2.4.3

MAINTAINER Norberto Garcia <nogala@gmail.com>

COPY worker.sh /

ENV SPARK_WORKER_WEBUI_PORT 8081
ENV SPARK_WORKER_LOG /spark/logs
ENV SPARK_MASTER "spark://spark-master:7077"

HEALTHCHECK CMD curl -f http://localhost:8081/ || exit 1

EXPOSE 8081

CMD ["/bin/bash", "/worker.sh"]
