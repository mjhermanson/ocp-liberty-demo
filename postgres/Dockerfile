# WebSphere Liberty base image
FROM websphere-liberty:latest

# Add config, app and jdbc driver
COPY --chown=1001:0 src/main/liberty/config/server.xml /config/server.xml
COPY --chown=1001:0 target/javaee-cafe.war /config/apps/
COPY --chown=1001:0 postgresql-42.2.4.jar /opt/ibm/wlp/usr/shared/resources/

# This script will add the requested XML snippets, grow image to be fit-for-purpose and apply interim fixes
RUN configure.sh
