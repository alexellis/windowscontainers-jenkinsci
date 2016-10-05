FROM windows-java:jre1.8.0_91

SHELL ["powershell"]
ARG BASE_URL
ARG SECRET

RUN (New-Object System.Net.WebClient).DownloadFile('{0}/jnlpJars/slave.jar' -f $env:BASE_URL, 'slave.jar') ;
ENTRYPOINT ["C:\\Java\\jre1.8.0_91\\bin\\java.exe", "-jar", ".\\slave.jar"]
