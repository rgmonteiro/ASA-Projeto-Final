FROM debian:buster

RUN apt-get update \
    && apt-get install -y \
    apache2 apache2-utils libapache2-mod-php \
    php php-cli php-curl php-xml php-imap \
    nano 

RUN apt-get upgrade -y

COPY email_1.sh .
COPY email_2.sh .
RUN ./email_2.sh

CMD tail -F /dev/null