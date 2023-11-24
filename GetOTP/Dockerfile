FROM image-registry.openshift-image-registry.svc:5000/openshift/redhat-openjdk18-openshift:1.12


COPY target/getopt-1.0.0.jar /home/jboss/test.jar

# Expose the ports we're interested in
EXPOSE 8180

CMD ["java", "-jar", "/home/jboss/test.jar"]
