FROM openjdk:8-jdk
MAINTAINER mohinder.dick@gmail.com

RUN mkdir -p /opt/matlab/mcr
RUN mkdir -p /opt/matlab/apps
WORKDIR /opt/matlab/mcr 
RUN wget -O mcr_installer.zip http://ssd.mathworks.com/supportfiles/downloads/R2017b/deployment_files/R2017b/installers/glnxa64/MCR_R2017b_glnxa64_installer.zip
RUN unzip mcr_installer.zip -d install/
WORKDIR install
RUN ./install -mode silent -agreeToLicense yes
WORKDIR /opt/matlab/apps