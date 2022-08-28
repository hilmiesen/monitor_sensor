FROM alpine:3.16.2
ENV PS1='\u@\h \w # '
RUN apk --update add --no-cache python3 py3-pip py3-redis py3-requests
CMD /collectd_script/collectd_script