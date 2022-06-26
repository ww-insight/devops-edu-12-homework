FROM ubuntu
RUN apt update
RUN apt install default-jdk -y
RUN apt install tomcat9 -y
RUN apt install maven -y
RUN apt install git -y
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git
RUN mvn package -f App42PaaS-Java-MySQL-Sample/
RUN cp App42PaaS-Java-MySQL-Sample/target/*.war /var/lib/tomcat9/webapps
COPY Config.properties /ROOT/Config.properties
EXPOSE 8080
ENV CATALINA_BASE /var/lib/tomcat9/
ENV CATALINA_HOME /usr/share/tomcat9
CMD $CATALINA_HOME/bin/catalina.sh run