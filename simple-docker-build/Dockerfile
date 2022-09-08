ARG VERSION=latest
FROM busybox:$VERSION
ARG VERSION
ENV MY_NAME="John Doe"

RUN echo $MY_NAME
RUN echo $VERSION
RUN echo $HTTP_PROXY

CMD [ "/bin/bash", "-c", "--" ] 
CMD [ "while", "true", ";", "do", "sleep", "30", ";", "done", ";" ]
