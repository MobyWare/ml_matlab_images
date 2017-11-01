FROM microsoft/windowsservercore
MAINTAINER mohinder.dick@gmail.com

RUN md C:\applications\matlab\opt
RUN md C:\applications\matlab\app

WORKDIR "C:\\applications\\matlab\\opt"

# Get Matlab Run-time for 2013a. Use zip format to allow for Expand-Archive
RUN powershell Invoke-WebRequest -OutFile MCR_R2013a_win64_installer.zip "http://ssd.mathworks.com/supportfiles/MCR_Runtime/R2013a/MCR_R2013a_win64_installer.exe"

RUN powershell Expand-Archive MCR_R2013a_win64_installer.zip -DestinationPath .

WORKDIR "bin\\win64"
 
RUN setup.exe -mode silent -agreeToLicense yes

WORKDIR "C:\\applications\\matlab\\app"