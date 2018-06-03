# pwa-starter-kit

This image should work for there architectures:
 -amd64, arm32v6, arm32v7, arm64v8, i386, ppc64le, s390x

Docker image files in [DockerHub](https://hub.docker.com/r/elswork/pwa-starter-kit/)

You can build your own images with the following command:

```sh
docker build -t elswork/pwa-starter-kit:latest .
```

You may clone and open the application directory:

```sh
git clone --depth 1 https://github.com/Polymer/pwa-starter-kit my-app
cd my-app
```

Then you can execute some npm commands (install, start, ...)

```sh
docker run -it --rm -v $(pwd):/root/my-app elswork/pwa-starter-kit npm install
docker run -it --rm -p 8081:8081 -v $(pwd):/root/my-app elswork/pwa-starter-kit npm start -- --hostname 0.0.0.0 --port 8081
docker run -it --rm -v $(pwd):/root/my-app elswork/pwa-starter-kit npm run build:static
```
