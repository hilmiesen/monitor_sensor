FROM alpine:3.16.2
ENV PS1='\u@\h \w # '
RUN apk --update add --no-cache redis
CMD /usr/bin/redis-server /etc/redis.conf