# docker-volume-backup
Dockerfile to backup/restore Docker Volumes

## Usage

backup/restore `app_mongo_db` volume
### backup

```sh
docker run --rm -v app_mongo_db:/target -v `pwd`:/export -e NAME=mongo_db ghcr.io/tiryoh/docker-volume-backup
```

### restore

```sh
docker run --rm -v app_mongo_db:/target -v `pwd`:/import -e TARGETFILE=$(ls mongo_db-*.tar.gz) ghcr.io/tiryoh/docker-volume-restore
```