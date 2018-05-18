FROM ubuntu:14.04

RUN apt-get update && apt-get install -y \
	htop \
	vim \
	nano \
	curl \
        git \
        software-properties-common \
        apt-transport-https ca-certificates 

# Install Java.
RUN \
  echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
  add-apt-repository -y ppa:webupd8team/java && \
  apt-get update && \
  apt-get install -y oracle-java8-installer 
  #apt-get install -y oracle-java8-installer && \
  #rm -rf /var/lib/apt/lists/* && \
  #rm -rf /var/cache/oracle-jdk8-installer

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-8-oracle


# Install Jenkin
RUN \
   wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add - && \
   echo deb https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list && \
   apt-get update && \
   apt-get install -y jenkins
  

CMD ["echo", "Hello Docker"]
