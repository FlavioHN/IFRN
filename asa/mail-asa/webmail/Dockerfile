# Configuração de webmail com postfix

FROM ubuntu:20.04

RUN apt update && apt upgrade -y

RUN apt install postfix nano -y

COPY main.cf /etc/postfix
