FROM alpine:3.12.1

ENV TARGETFILE volume-backup.tar.gz
RUN echo "tar xvf /import/\$TARGETFILE" > /root/restore.sh
WORKDIR /target
VOLUME /target
VOLUME /import
CMD ["/bin/sh", "/root/restore.sh"]
