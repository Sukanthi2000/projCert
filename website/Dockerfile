FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

# Install Apache and PHP
RUN apt-get update && \
    apt-get install -y apache2 php libapache2-mod-php && \
    apt-get clean

# Remove Apache's default index.html
RUN rm -f /var/www/html/index.htm

# Copy your app (including index.php) to Apache root
COPY . /var/www/html/

EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND"]

