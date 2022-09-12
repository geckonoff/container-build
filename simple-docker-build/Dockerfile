ARG VERSION=latest
FROM busybox:$VERSION
ARG VERSION
ENV MY_NAME="John Doe"

RUN echo $MY_NAME
RUN echo $VERSION
RUN echo $HTTP_PROXY
WORKDIR /tmp
RUN ls ./

ADD run.sh /tmp/run.sh
RUN chmod +x /tmp/run.sh
ENTRYPOINT ["/tmp/run.sh"]
