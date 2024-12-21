FROM drupal

RUN apt-get update && \
    apt-get install -y git && \
    rm -rf /var/lib/apt/lists/* ;

WORKDIR /var/www/html/themes

RUN git clone --branch 5.0.x --single-branch --depth 1 https://git.drupalcode.org/project/bootstrap.git && \
    chown -R www-data:www-data bootstrap

WORKDIR /var/www/html

VOLUME [ "drupal-modules:/var/www/html/modules", \
	     "drupal-profiles:/var/www/html/profiles", \
	     "drupal-sites:/var/www/html/sites", \
	     "drupal-themes:/var/www/html/themes " ]

EXPOSE 80