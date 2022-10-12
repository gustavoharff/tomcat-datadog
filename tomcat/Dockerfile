FROM tomcat:8-jdk8

COPY ./sdk/dd-java-agent.jar /usr/local/tomcat/lib/dd-java-agent.jar

RUN touch ./bin/setenv.sh

RUN rm -rf /usr/local/tomcat/lib/log4j.properties

COPY ./log4j.properties /usr/local/tomcat/log4j.properties

RUN echo 'CATALINA_OPTS="$CATALINA_OPTS -Dcom.sun.management.jmxremote -Dcom.sun.management.jmxremote.port=9012 -Dcom.sun.management.jmxremote.ssl=false -Dcom.sun.management.jmxremote.authenticate=false -javaagent:/usr/local/tomcat/lib/dd-java-agent.jar"' >> ./bin/setenv.sh

EXPOSE 9012