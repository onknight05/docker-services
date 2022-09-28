## How to use

Create ```.env``` file by copy ```.env-example``` and update corresponding.

Start a service
```bash
$ docker-compose up <service_name> #add & to run in background
```
Start all
```bash
$ docker-compose up
```
Stop by ```docker-compose down```

## Useful command

- Clean data in a dir
```bash script/clean_data.sh ./data/mongo```
