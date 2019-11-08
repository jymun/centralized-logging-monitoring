FROM  openjdk

COPY hello-demo.jar hello-demo.jar
RUN  curl -O  https://repo1.maven.org/maven2/co/elastic/apm/elastic-apm-agent/1.11.0/elastic-apm-agent-1.11.0.jar


ENTRYPOINT java -javaagent:elastic-apm-agent-1.11.0.jar \
         -Delastic.apm.service_name=my-application \
         -Delastic.apm.server_url=http://apm-server:8200 \
         -Delastic.apm.application_packages=org.example \
         -jar -Dserver.port=8080 hello-demo.jar
