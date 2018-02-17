FROM php:7.2
RUN apt-get update
RUN apt-get install -y wget unzip
RUN wget -O /tmp/master.zip https://github.com/pierallard/ratchet/archive/master.zip
RUN unzip /tmp/master.zip -d /tmp/ratchet/
RUN mv /tmp/ratchet/ratchet-master/* /root/
RUN wget https://getcomposer.org/download/1.6.2/composer.phar -P /root/
RUN cd /root/ && php /root/composer.phar install
ENTRYPOINT cd /root/ && php bin/chat-server.php
