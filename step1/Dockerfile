FROM debian:buster

RUN apt-get update -yq \
&& apt-get install curl -yq \
&& curl -fsSL https://deb.nodesource.com/setup_15.x | bash \
&& apt-get install nodejs -yq \
&& apt-get clean -y

ADD . /app/
WORKDIR /app
RUN npm install

EXPOSE 3000

CMD node app
