FROM ubuntu:18.04
EXPOSE 5000
RUN apt-get update
RUN apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash
RUN apt-get install -y nodejs
COPY . .
RUN npm install
RUN npm run build
RUN npm install -g serve
CMD serve -s -l 5000 build
