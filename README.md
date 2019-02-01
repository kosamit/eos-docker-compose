# Run cleos and keosd from docker-compose

## Official Docker files

https://github.com/EOSIO/eos/tree/master/Docker

## Init

mkdir nodeos-data-dir
mkdir keosd-data-dir
mkdir contracts
docker-compose build

## Run docker

docker-compose up -d

## Stop docker

docker-compose -f docker-compose-eosio-latest.yaml down

## Execute cleos commands

./cleos.sh