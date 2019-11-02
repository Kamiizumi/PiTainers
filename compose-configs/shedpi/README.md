# docker-compose for ShedPi

This docker-compose file starts up the services I use on ShedPi (a Raspberry Pi attached to the side of the shed).

## Usage

Ensure that the `ds18b20-mqtt` and `rtl_433` images have been built or are available to the Docker daemon.

To bring up ShedPi services run the following command:

```sh
docker-compose up
```
