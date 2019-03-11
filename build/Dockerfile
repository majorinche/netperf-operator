FROM alpine:3.6

RUN adduser -D netperf-operator
USER netperf-operator

ADD netperf-operator /usr/bin/netperf-operator
ENTRYPOINT ["/usr/bin/netperf-operator"]
