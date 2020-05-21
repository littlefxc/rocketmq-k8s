FROM rocketmqinc/rocketmq:4.4.0

ENV TimeZone=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TimeZone /etc/localtime && echo $TimeZone > /etc/timezone

RUN rm /etc/yum.repos.d/* -rf

ADD CentOS-Base.repo  /etc/yum.repos.d/

RUN rm -rf rm -rf /opt/rocketmq-4.4.0/conf/2m* && \
    rm -rf /opt/rocketmq-4.4.0/conf/broker.conf && \
    rm -rf /opt/rocketmq-4.4.0/bin/*.cmd

#sudo docker build -t 192.168.195.2/dev/rocketmq:v4.4.0 .

