FROM tomcat:9.0.62-jdk8-openjdk
MAINTAINER r995
# copy war file into container image under app directory
#COPY build/libs/*.war /usr/local/tomcat/webapps/inspect.war

COPY ./docker/tomcat9062/libs/jfxrt.jar /usr/local/openjdk-8/jre/lib/ext/
# expose server port accept connections
RUN sed -i 's/port="8080"/port="9000"/' /usr/local/tomcat/conf/server.xml
EXPOSE 9000
# start application
CMD ["/usr/local/tomcat/bin/catalina.sh","run"]