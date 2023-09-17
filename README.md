# DNS and Reverse Proxy server

DNS server and reverse proxy with BIND9 and NGINX to deploy on your local network.

## Requirements

-   Docker
-   Docker Compose

## Built with

-   [![Bind9][Bind9]][Bind9-url]
-   [![Nginx][Nginx]][Nginx-url]

## Deploy Locally

1. Clone this repository to your local machine:

```bash
git clone https://github.com/jvillegasl/dns-with-reverse-proxy.git
```

2. Navigate to the project directory:

```bash
cd dns-with-reverse-proxy
```

3. Edit the DNS records in `./dns/example-home.zone` to match your machine IP.

4. Start the application using Docker Compose:

```docker
docker-compose up
```

5. Set your localhost as your DNS.

_Note: Consider that IPv6 takes prevalence over IPv4. In some cases it may be necessary to set your DNS IPv6._

6. Add your own DNS records at `./dns/example-home.zone` and your proxy redirections at `./reverse-proxy/app.conf`. Open [http://test-server.example.home](http://test-server.example.home) with your browser to see and and already configured example.

<!-- MARKDOWN LINKS & IMAGES -->

[Nginx]: https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white
[Nginx-url]: https://www.nginx.com/

<!--  -->

[Bind9]: https://img.shields.io/badge/Bind_9-0081CB?style=for-the-badge
[Bind9-url]: https://www.isc.org/bind/
