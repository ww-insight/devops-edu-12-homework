FROM tomcat
RUN apt update
RUN apt install default-jdk -y
RUN apt install maven -y
RUN apt install git -y
RUN git clone https://github.com/ww-insight/devops-edu-12-homework-java.git
RUN mvn package -f devops-edu-12-homework-java
RUN cp devops-edu-12-homework-java/target/*.war /usr/local/tomcat/webapps