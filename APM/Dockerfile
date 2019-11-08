FROM tomcat 

RUN wget -P $CATALINA_HOME/ https://repo1.maven.org/maven2/co/elastic/apm/elastic-apm-agent/1.11.0/elastic-apm-agent-1.11.0.jar 
ENV JAVA_OPTS=-javaagent:$CATALINA_HOME/elastic-apm-agent-1.11.0.jar

ENV JAVA_OPTS=-javaagent:$CATALINA_HOME/elastic-apm-agent-1.11.0.jar \
              -Delastic.apm.service_name=tomcat-test \
              -Delastic.apm.application_packages=org.example \
              -Delastic.apm.server_url=http://apm-server:8200
			  

