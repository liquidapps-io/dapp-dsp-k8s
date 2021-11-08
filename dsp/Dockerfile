FROM node:12.22.1

RUN apt update && \
    apt install -y curl wget net-tools telnet postgresql-client && \
    rm -rf /*.deb /var/lib/apt/lists/*

RUN npm install -g pm2 -unsafe-perm=true \
    npm install -g @liquidapps/dsp --unsafe-perm=true \
    npm install -g @liquidapps/box-utils --unsafe-perm=true 

RUN cd $(readlink -f `which setup-dsp` | xargs dirname)

WORKDIR /usr/local/lib/node_modules/@liquidapps/dsp/zeus_boxes

CMD [ "setup-dsp" ]
