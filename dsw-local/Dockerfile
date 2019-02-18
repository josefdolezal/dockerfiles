FROM ubuntu:bionic

RUN apt-get update
# Install required packages
RUN apt-get install -y curl gnupg2 wkhtmltopdf
# Add nodejs repository source
RUN curl -sL https://deb.nodesource.com/setup_11.x | bash -
# Install nodejs
RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y \
            nodejs yarn
# Install Haskell stack
RUN curl -sSL https://get.haskellstack.org/ | sh
# Install mongodb
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 9DA31620334BD75D9DCB49F368818C72E52529D4
RUN echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.0 multiverse" | tee /etc/apt/sources.list.d/mongodb-org-4.0.list
RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y mongodb-org
RUN mkdir -p /var/mongodb

EXPOSE 80

# Run mongo as default command
CMD [ "mongod", "--dbpath", "/var/mongodb"]
