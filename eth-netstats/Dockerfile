FROM node:8-alpine
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/' /etc/apk/repositories
RUN apk add --update git

RUN git clone https://github.com/cubedro/eth-netstats

WORKDIR /eth-netstats

RUN npm install -g cnpm --registry=https://registry.npm.taobao.org

RUN cnpm install
RUN cnpm install -g grunt-cli
RUN grunt

EXPOSE 3000

CMD ["npm", "start"]
