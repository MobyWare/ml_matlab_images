FROM microsoft/windowsservercore
MAINTAINER mohinder.dick@gmail.com

RUN md C:\applications\matlab\opt
RUN md C:\applications\matlab\app

WORKDIR "C:\\applications\\matlab\\opt"

# Get Matlab Run-time for 2013a. Use zip format to allow for Expand-Archive
RUN powershell Invoke-WebRequest -OutFile MCR_R2017b_win64_installer.zip "http://ssd.mathworks.com/supportfiles/downloads/R2017b/deployment_files/R2017b/installers/win64/MCR_R2017b_win64_installer.exe"

RUN powershell Expand-Archive MCR_R2017b_win64_installer.zip -DestinationPath .

WORKDIR "bin\\win64"

# set up adds run-time to the PATH
RUN setup.exe -mode silent -agreeToLicense yes

WORKDIR "C:\\applications\\matlab\\app"