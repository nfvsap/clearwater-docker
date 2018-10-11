FROM ubuntu:14.04
RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y curl vim
RUN apt-get install -y apt-transport-https unzip
COPY sysctl /sbin/sysctl
RUN echo deb http://repo.cw-ngv.com/stable binary/ > /etc/apt/sources.list.d/clearwater.list
RUN curl -L http://repo.cw-ngv.com/repo_key | apt-key add -
RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y --force-yes clearwater-sip-stress-coreonly
COPY run_stress /usr/share/clearwater/bin/run_stress
EXPOSE 5082
CMD exec /bin/sh -c "trap : TERM INT; (while true; do sleep 1000; done) & wait"
