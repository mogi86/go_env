# go_env

## Description

* Golangを動かすためのdocker環境を提供するためのリポジトリ。
* DBなどを自身のローカルPCに作成したくない場合など、ローカルPCを汚したくない場合に使う。
    * DBはdocker環境にしかインストールしないのでDB関連の機能を使う場合は、このリポジトリの使用が必要。

## Set up

### Docker set up

```bash
$ cd /path/to/go_env
$ docker-compose build
$ docker-compose up -d
```

### Provisioning

```bash
$ cd /path/to/go_env
$ ansible-playbook -i ansible/inventories/local site.yml
```

## Login docker container

```bash
$ cd /path/to/go_env
$ docker exec -it go_env /bin/bash --login
```
