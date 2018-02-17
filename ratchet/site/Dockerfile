FROM httpd:2.4
RUN apt-get update
RUN apt-get install -y wget unzip
RUN wget -O /tmp/master.zip https://github.com/pierallard/ratchet/archive/master.zip
RUN unzip /tmp/master.zip -d /tmp/ratchet/
RUN mv /tmp/ratchet/ratchet-master/* /usr/local/apache2/htdocs/
RUN mv /usr/local/apache2/htdocs/web /usr/local/apache2/htdocs/console
