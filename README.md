[![Docker Repository on Quay.io](https://quay.io/repository/heximcz/knotdns/status "Docker Repository on Quay.io")](https://quay.io/repository/heximcz/knotdns)
[![](https://images.microbadger.com/badges/image/hexim/knotdns.svg)](http://microbadger.com/images/hexim/knotdns "Get your own image badge on microbadger.com")

# heximcz/knotdns:2.5.4

- **High-performance authoritative-only DNS server**
- Knot DNS is a high-performance authoritative-only DNS server which supports all key features of the modern domain name system.
- Knot maintainer: [CZ.NIC Labs](https://www.knot-dns.cz/) Knot DNS is developed by CZ.NIC Labs, the R&D department of .CZ registry and hence is well suited to run anything from the root zone, the top-level domain, to many smaller standard domain names. 
- Documentation for Knot DNS 2.x: [html](https://www.knot-dns.cz/docs/2.x/html/),[html single page](https://www.knot-dns.cz/docs/2.x/singlehtml/),[PDF](https://www.knot-dns.cz/docs/2.x/KnotDNS.pdf)


## Docker Knot DNS:
- latest version: **docker pull hexim/knotdns:2.5.4**

## Additional modules:

- php5-cli, php5-mysql, php5-curl, phpunit (for [SynKnot](https://synknot.cz/))
- vim (powerful text editor)
- ntpdate (sync date)
- net-tools (netstat,...)
- mc (Midnight Commander)
- nano (text editor)

## Example: docker-compose.yml


```
version: '2'
services:
  knot:
    container_name: knotdns
    image: 'hexim/knotdns:latest'
    ports:
     - "5053/tcp:53/tcp"
     - "5053/udp:53/udp"
    stdin_open: true
    volumes:
     - /opt/synknot:/opt/synknot
     - /opt/knot/etc:/etc/knot
     - /opt/knot/var/lib:/var/lib/knot
```


## Knot DNS configurations

[Read more examples on github](https://github.com/heximcz/docker-knotdns/tree/master/examples)


