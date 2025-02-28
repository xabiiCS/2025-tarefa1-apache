FROM debian:12

RUN apt update && apt install -y nano apache2 && apt clean && rm -rf /var/lib/apt/lists/*

RUN a2enmod ssl 
RUN a2enmod auth_digest.load
RUN a2enmod authz_groupfile.load
RUN rewrite.load
EXPOSE 80

CMD ["apache2ctl", "-D", "FOREGROUND"]

