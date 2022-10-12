FROM gcr.io/datadoghq/agent:latest-jmx

COPY ./conf.yaml /etc/datadog-agent/conf.d/tomcat.d/conf.yaml

EXPOSE 8126

EXPOSE 10516

# RUN echo 'logs_enabled: true' >> /etc/datadog-agent/datadog-docker.yaml

# COPY ./datadog.yaml /etc/datadog-agent/datadog.yaml