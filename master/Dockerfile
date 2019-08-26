FROM nogala/spark-base:2.4.3

MAINTAINER Norberto Garcia <nogala@gmail.com>

COPY master.sh /

ENV SPARK_MASTER_PORT 7077
ENV SPARK_MASTER_WEBUI_PORT 8080
ENV SPARK_MASTER_LOG /spark/logs

HEALTHCHECK CMD curl -f http://localhost:8080/ || exit 1

EXPOSE 8080 7077 6066

CMD ["/bin/bash", "/master.sh"]
