FROM java:8-jre-alpine

ENV FILE_NAME=apache-ignite-fabric-2.0.0-bin
ENV IGNITE_HOME=/ignite/ignite

RUN mkdir -p /ignite/log && \
    apk update && \
    apk add curl bash && \
    curl -O http://apache.mirror.cdnetworks.com/ignite/2.0.0/${FILE_NAME}.zip && \
    unzip ${FILE_NAME}.zip -d /ignite && \
    mv /ignite/${FILE_NAME} /ignite/ignite && \
    rm ${FILE_NAME}.zip

CMD ["/ignite/ignite/bin/ignite.sh"]
