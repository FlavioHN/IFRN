# Configuração de server email com postfix e dovecot 

FROM ubuntu:latest

RUN apt update \
nano telnet net-tools \
postfix \
dovecot-core dovecot-pop3d dovecot-imapd -y

RUN apt upgrade -y

COPY /smtp/main.cf /etc/postfix/main.cf

COPY /imap/10-auth.conf /etc/dovecot/conf.d/10-auth.conf
COPY /imap/10-mail.conf /etc/dovecot/conf.d/10-mail.conf
COPY /imap/10-master.conf /etc/dovecot/conf.d/10-master.conf
COPY /imap/dovecot.conf /etc/dovecot/dovecot.conf

EXPOSE 25 110 143 993 995

CMD tail -F /dev/null