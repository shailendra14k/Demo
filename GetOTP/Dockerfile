FROM registry.redhat.io/redhat-openjdk-18/openjdk18-openshift


COPY target/getopt-1.0.0.jar /home/jboss/test.jar

# Expose the ports we're interested in
EXPOSE 8180

CMD ["java", "-jar", "/home/jboss/test.jar"]
