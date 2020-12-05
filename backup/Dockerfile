FROM alpine:3.12.1

ENV NAME volume-backup
RUN echo "export TIMESTAMP=\$(date '+%Y%m%d%H%M%S')" > /root/backup.sh && \
    echo "tar cvf /export/\$NAME-\$TIMESTAMP.tar.gz ." >> /root/backup.sh
WORKDIR /target
VOLUME /target
VOLUME /export
CMD ["/bin/sh", "/root/backup.sh"]
