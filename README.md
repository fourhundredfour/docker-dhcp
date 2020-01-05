# DHCP Server
A fully operable (ISC-) DHCP-Server running on Alpine-Linux.

## Index

* [Requirements](#requirements)
* [Installation](#installation)

## Requirements

* Network Interface
* Docker

## Installation

1. Pull the image or build it by executing the following command.
`$ docker build . -t docker-dhcp`
2. Create the container.
`$ docker run --restart=always -d --net=host docker-dhcp`
3. (optional) If you want to use your own configuration, then use a volume.
`$ docker run -v $PWD/files/dhcpd.conf:/etc/dhcp/dhcpd.conf --restart=always -d --net=host docker-dhcp`