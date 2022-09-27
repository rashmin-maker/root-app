FROM ubuntu

ARG http_proxy=http://proxy-dmz.intel.com:912
ARG https_proxy=http://proxy-dmz.intel.com:912
ARG no_proxy=intel.com,.intel.com,10.0.0.0/8,192.168.0.0/16,localhost,127.0.0.0/8,134.134.0.0/16,172.16.0.0/16

ENV http_proxy ${http_proxy}
ENV https_proxy ${https_proxy}
ENV no_proxy ${no_proxy}

RUN apt update
RUN apt install -y apache2
RUN apt install -y apache2-utils
RUN apt clean

EXPOSE 80
CMD ["apache2ctl", "-D", "FOREGROUND"]