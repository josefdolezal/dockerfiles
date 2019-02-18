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

CMD [ "bash" ]