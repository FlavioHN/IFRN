# Configuração de server email com postfix e dovecot 

FROM ubuntu:latest

RUN apt-get update && apt-get install -y \ 
nano \ 
telnet \
net-tools \
netcat \
postfix \
dovecot-core dovecot-pop3d dovecot-imapd

RUN apt-get upgrade -y

COPY /smtp-postfix/main.cf /etc/postfix/main.cf

#COPY /imap-pop-dovecot/10-auth.conf /etc/dovecot/conf.d/10-auth.conf
#COPY /imap-pop-dovecot/10-mail.conf /etc/dovecot/conf.d/10-mail.conf
#COPY /imap-pop-dovecot/10-master.conf /etc/dovecot/conf.d/10-master.conf
#COPY /imap-pop-dovecot/dovecot.conf /etc/dovecot/dovecot.conf

EXPOSE 25 110 143 993 995

CMD tail -F /dev/null