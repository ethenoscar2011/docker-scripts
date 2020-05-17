FROM redis:5.0.9-alpine
LABEL maintainer="EthenLu ethenoscar2011@163.com"
ENV TIME_ZONE=Asia/Shanghai 
RUN ln -snf /usr/share/zoneinfo/$TIME_ZONE /etc/localtime && echo $TIME_ZONE > /etc/timezone
ENTRYPOINT echo "yes"|redis-cli -a redis@cluster@2020 --cluster create 172.19.0.2:6379 172.19.0.3:6379 172.19.0.4:6379 172.19.0.5:6379 172.19.0.6:6379 172.19.0.7:6379 --cluster-replicas 1
