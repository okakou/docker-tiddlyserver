# Base image
FROM debian:stretch

# Maintainer
MAINTAINER Kouta Okamoto <okakou0512@gmail.com>

# Set non interactive install
ENV DEBIAN_FRONTEND=noninteractive

# Install nodejs
RUN apt-get update && apt-get install -y \
apt-utils curl wget zip gnupg
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get update && apt-get install -y \
nodejs

# Install tiddlyserver
RUN wget https://github.com/Arlen22/TiddlyServer/archive/2.0.14-fixed.zip
RUN unzip 2.0.14-fixed.zip

# Access port
EXPOSE 8080

# Set run command
CMD [ "bash", "-c", "node /TiddlyServer-2.0.14-fixed/server.js /config/settings.json < /dev/null" ]
