FROM redis:5.0.9-alpine
LABEL maintainer="EthenLu ethenoscar2011@163.com"
ENV TIME_ZONE=Asia/Shanghai 
RUN ln -snf /usr/share/zoneinfo/$TIME_ZONE /etc/localtime && echo $TIME_ZONE > /etc/timezone
EXPOSE 26379
COPY sentinel.conf /etc/redis/sentinel.conf
ENTRYPOINT redis-server /etc/redis/sentinel.conf --sentinel