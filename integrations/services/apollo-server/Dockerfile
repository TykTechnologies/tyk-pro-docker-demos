FROM        node:latest

MAINTAINER  Zaid Albirawi

RUN         mkdir -p /var/www/
COPY        ./integrations/services/apollo-server/src/* /var/www/
WORKDIR     /var/www
RUN         npm i

ENTRYPOINT  node index.js
