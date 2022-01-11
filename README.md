# docker-volume-backup

Dockerfile to backup/restore files in Docker Volumes

## Usage

e.g.) backup/restore `app_mongo_db` volume

### backup

```sh
docker run --rm -v app_mongo_db:/target -v `pwd`:/export -e NAME=mongo_db ghcr.io/tiryoh/docker-volume-backup
```

### restore

```sh
docker run --rm -v app_mongo_db:/target -v `pwd`:/import -e TARGETFILE=$(ls mongo_db-*.tar.gz) ghcr.io/tiryoh/docker-volume-restore
```

## License

Copyright (c) 2020 Daisuke Sato

This repository is licensed under the MIT license, see [LICENSE](./LICENSE).
Unless attributed otherwise, everything in this repository is licensed under the MIT license.

## Reference

This project is based on [@74th](https://github.com/74th)'s work.

dockerのデータボリュームとそのバックアップ方法 - Qiita  
https://qiita.com/74th/items/41393f506d223850f2c3

* https://github.com/74th/dockervolumerestore
* https://github.com/74th/dockervolumebackup