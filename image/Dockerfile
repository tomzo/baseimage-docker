FROM debian:wheezy
MAINTAINER Tomasz Setkowski <tom@ai-traders.com>

ENV HOME /root
RUN mkdir /build
ADD . /build

RUN /build/prepare.sh && \
	/build/system_services.sh && \
	/build/utilities.sh && \
	/build/cleanup.sh

RUN /usr/sbin/enable_insecure_key

CMD ["/sbin/my_init"]
