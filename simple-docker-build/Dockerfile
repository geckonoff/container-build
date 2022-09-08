ARG VERSION=latest
FROM busybox:$VERSION
ARG VERSION
ENV MY_NAME="John Doe"

RUN echo $MY_NAME
RUN echo $VERSION
RUN echo $HTTP_PROXY

ENTRYPOINT [ "while true; do sleep 30; done;" ]
CMD [ "/bin/bash", "-c", "--" ] 
