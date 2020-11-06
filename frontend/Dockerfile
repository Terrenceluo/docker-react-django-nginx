FROM node:10.22.1

WORKDIR /app/frontend

RUN npm config set registry https://registry.npm.taobao.org \
&& npm install -g serve

COPY ./build ./build

COPY start.sh ./start.sh

RUN sed -i 's/\r//' ./start.sh \
&& chmod +x ./start.sh
