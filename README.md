# go-coffeeshop

The coffeeshop with golang stack

## Package

```go
go get -u github.com/ilyakaznacheev/cleanenv
```

## Debug Apps

[Debug golang app in monorepo](https://github.com/thangchung/go-coffeeshop/wiki/Golang#debug-app-in-monorepo)

## Connect to app running on host machine in `docker-from-docker` feature

From host machine, Ubuntu 22.04 at here, type:

```bash
> ifconfig
```

Then find `docker0` IP address in the output, just like

```bash
docker0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
    inet 172.17.0.1  netmask 255.255.0.0  broadcast 172.17.255.255
    inet6 fe80::42:6dff:fe39:ba02  prefixlen 64  scopeid 0x20<link>
    ether 02:42:6d:39:ba:02  txqueuelen 0  (Ethernet)
    RX packets 994  bytes 122399 (122.3 KB)
    RX errors 0  dropped 0  overruns 0  frame 0
    TX packets 759  bytes 772987 (772.9 KB)
    TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

In here, we can find `172.17.0.1`, then use it for all accesses in `docker-from-docker`

## Generate Protobuf/gRPC

```bash
> buf mod update proto
> buf generate
```

## Project structure

- [project-layout](https://github.com/golang-standards/project-layout)
- [repository-structure](https://peter.bourgon.org/go-best-practices-2016/#repository-structure)
- [go-build-template](https://github.com/thockin/go-build-template)
- [go-wiki](https://github.com/golang/go/wiki/Articles#general)
