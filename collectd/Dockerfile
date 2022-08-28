FROM alpine:3.16.2
ENV PS1='\u@\h \w # '
RUN apk --update add --no-cache collectd collectd-snmp collectd-write_redis
CMD /usr/sbin/collectd -f