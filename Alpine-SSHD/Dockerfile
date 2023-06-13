FROM        alpine:latest

LABEL       maintainer="Tibet"

#RUN        apk add --update --no-cache doas && \
#		    adduser -h /home/tibet -s /bin/sh -D tibet -G wheel && \
#		    echo -n 'tibet:Qwerty1234' | chpasswd && \
#		    echo 'permit nopass :wheel as root' > /etc/doas.d/doas.conf

RUN		    adduser -h /home/tibet -s /bin/sh -D tibet -G wheel; \
		    echo -n 'tibet:Qwerty1234' | chpasswd

RUN		    apk add --update --no-cache openssh; \
		    echo 'PasswordAuthentication yes' >> /etc/ssh/sshd_config

ENTRYPOINT  ["/entrypoint.sh"]

EXPOSE		22

COPY		entrypoint.sh /