# eos-docker-compose

Dockerized cleos and keosd from docker-compose.


## Initialize

```
git clone https://github.com/kosamit/eos-docker-compose.git
cd eos-docker-compose
./init.sh
```

## Run docker

```
docker-compose up -d
```

## Stop docker

```
docker-compose down
```

## Use cleos commands

```
./cleos.sh
```

## error comes out that "database dirty flag set" when running "docker-compose up"

### Solution
Set "--hard-replay" to the command of nodeosd in docker-compose.yml.

```
	command: /opt/eosio/bin/nodeosd.sh --data-dir /opt/eosio/bin/data-dir -e --http-alias=nodeosd:8888 --http-alias=127.0.0.1:8888 --http-alias=localhost:8888 --hard-relay
```
