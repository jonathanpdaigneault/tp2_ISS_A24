FROM drupal

RUN apt update && \
    apt install -y git; \
    rm -rf /var/lib/apt/lists/*;

    
WORKDIR /var/www/html/themes

RUN git clone --branch 5.0.x --single-branch --depth 1 https://git.drupalcode.org/project/bootstrap.git && \
chown -R www-data:www-data bootstrap ;