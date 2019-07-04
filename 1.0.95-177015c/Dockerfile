FROM amazonlinux:latest

ADD rescale.jar /usr/local/bin/

RUN yum update -y; \
    yum install -y java; \
    groupadd -r rescale && useradd -r -g rescale rescale; \
    mkdir /home/rescale; \
    chown rescale /home/rescale; \
    chgrp rescale /home/rescale

USER rescale
WORKDIR /home/rescale
CMD ["java","-jar","/usr/local/bin/rescale.jar","-h"]
