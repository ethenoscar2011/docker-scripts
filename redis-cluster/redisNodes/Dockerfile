FROM redis:5.0.9-alpine
LABEL maintainer="EthenLu ethenoscar2011@163.com"
ENV TIME_ZONE=Asia/Shanghai 
RUN ln -snf /usr/share/zoneinfo/$TIME_ZONE /etc/localtime && echo $TIME_ZONE > /etc/timezone
EXPOSE 6379 16379
COPY redis.conf /etc/redis/redis.conf
ENTRYPOINT redis-server /etc/redis/redis.conf