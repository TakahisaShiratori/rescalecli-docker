FROM amazonlinux:latest

ADD rescale-cli_linux_1_1_14-fdc7a1ea47.rpm /tmp/

RUN yum update -y; \
    yum install -y shadow-utils.x86_64; \
    rpm -i /tmp/rescale-cli_linux_1_1_14-fdc7a1ea47.rpm; \
    rm /tmp/rescale-cli_linux_1_1_14-fdc7a1ea47.rpm; \
    groupadd -r rescale && useradd -r -g rescale rescale; \
    mkdir /home/rescale; \
    chown rescale /home/rescale; \
    chgrp rescale /home/rescale

USER rescale
WORKDIR /home/rescale
CMD ["rescale-cli","-h"]
