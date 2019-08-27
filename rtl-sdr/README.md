# rtl-sdr

rtl-sdr is a Docker container with the rtl-sdr package installed, allowing use of rtl-sdr commands. The container also has [heatmap](https://github.com/keenerd/rtl-sdr-misc/tree/master/heatmap) to generate heat map images from rtl_power output.

## Building

The Dockerfile this container uses is based on an arm32v6 base image, meaning an arm32v6 capable host is required (e.g. the *Raspberry Pi 1*).

The Docker container can be built by running the following command from this folder:

```sh
docker build -t rtl-sdr .
```

## Usage

This container is expected to be used interactively. The container can be started with the following command:

```sh
docker run -it --rm --privileged rtl-sdr
```

- `-it` starts the container interactively
- `--rm` deletes the container after it exits
- `--privileged` is required so the container can access RTL-SDR devices

rtl-sdr is installed globally, so rtl commands are available anywhere. The `heatmap.py` script is installed in the root of the container.
