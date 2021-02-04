# The Alpine Docker image with latest GCC

This image is based on Alpine Linux image and contains [C/C++ compiler](https://gcc.gnu.org/) (GCC 7/8/9/10).

- Forked from: https://github.com/n0madic/alpine-gcc

## Docker Hub images

- From: https://github.com/n0madic/alpine-gcc
- Docker Hub: https://hub.docker.com/r/n0madic/alpine-gcc

### Alpine Linux with GCC 7.x

```bash
# GCC 7.x
docker pull n0madic/alpine-gcc:7.5.0
```

### Alpine Linux with GCC 8.x

```bash
# GCC 8.x
docker pull n0madic/alpine-gcc:8.4.0
```

### Alpine Linux with GCC 9.x

```bash
# GCC 9.x
docker pull n0madic/alpine-gcc:9.2.0
```

### Alpine Linux with GCC 10.x

```bash
# GCC 10.x
docker pull n0madic/alpine-gcc:10.1.0
```

## Build image and usage

- GCC 9.x: `GCC_VERSION='9.3.0'`
- GCC 10.x: `GCC_VERSION='10.2.0'`

```bash
cd /tmp && \
git clone https://github.com/theUncanny/alpine-gcc.git && \
cd alpine-gcc && \
docker build \
    --build-arg GCC_VERSION='10.2.0' \
    -t alpine-gcc . && \
docker run \
    --rm \
    -it 
    -v $(pwd):/src \
    alpine-gcc
```
