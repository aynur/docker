FROM donshea/ocssw-run:1.2 
COPY $HOME/.netrc /root/.netrc 
COPY seadas-ocsswserver.jar /root/seadas-ocsswserver.jar 
VOLUME /root/seadasClientServerShared 
VOLUME /root/ocssw
RUN cat ocsswserver.config 
CMD ["jre1.8.0_321/bin/java", "-Xmx4G", "-jar", "seadas-ocsswserver.jar", "ocsswserver.config"] 
EXPOSE 6400 6402 6403

LABEL "gov.nasa.gsfc.seadas"="NASA OEL SeaDAS"
LABEL version="1.0"
LABEL description="This Dockerfile is used to create the ocssw-run image."

