percona-server-5.6-persistent
=============

Docker image for Percona Server 5.6 with persistent data (using data volume)


Build
-----

```bash
docker build -t andreisusanu/percona-server-5.6-persistent .
```

Create data volume
-----
```bash
docker volume create --name MySQLStorageVolume
```

Run
-----
```bash
docker run \
    --name percona-server-5.6 \
    -p 3306:3306 \
    -v MySQLStorageVolume:/var/lib/mysql \
    andreisusanu/percona-server-5.6-persistent
```

MySQL redentials
-----
root without password (blank password)
