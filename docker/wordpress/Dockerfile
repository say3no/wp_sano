FROM wordpress:5.1.1-php7.1-apache
LABEL maintainer="say3no"

# install wp-cli
RUN curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
RUN chmod +x wp-cli.phar
RUN mv wp-cli.phar /usr/local/bin/wp

RUN wp plugin install broken-link-checker contact-form-7 --activate
#COPY ./original_wp_plugin/ /path/to/plugins

COPY ./unpko.txt /var/www/html/.
RUN chmod 777 /var/www/html/unpko.txt
