FROM node:6.15-alpine
RUN apk add --update tini \
&& mkdir -p /usr/src/app
WORKDIR /usr/src/app
COPY package.json package.json
RUN npm install \
&& npm cache clean
COPY . .
EXPOSE 3000
CMD ["/sbin/tini", "--", "node", "./bin/www"]

 



