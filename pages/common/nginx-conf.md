# nginx

> Nginx web server.
> More information: <https://nginx.org/en/>.

- Start server with the default configuration file:

`nginx`

- Start server with a custom configuration file:

`nginx -c {{configuration_file}}`

- Stop a server running a custom configuration file:

`nginx -c {{configuration_file}} -s stop`

- Test the configuration without affecting the running server:

`nginx -t`

- Reload the configuration by sending a signal with no downtime:

`nginx -s reload`

- This example shows a group of three servers, two of them running instances of the same application while the third is a backup server:

http {
    upstream backend {
        server backend1.example.com;
        server backend2.example.com;
        server 192.0.0.1 backup;
    }

    server {
        location / {
            proxy_pass http://backend;
        }
    }
}

- This example shows minimal config for a reverse proxy:

server {
        listen  80;
        server_name some.domain.org;
        location / {
            proxy_set_header    Host $host;
            proxy_set_header    X-Real-IP   $remote_addr;
            proxy_set_header    X-Forwarded-For $proxy_add_x_forwarded_for;
            proxy_pass  http://127.0.0.1:8081;
        }
}

- This example shows minimal config for a webserver:

server {
    root /www/data;

    location / {
    index index.$geo.html index.htm index.html;
    }

    location /images/ {
    }

    location ~ \.(mp3|mp4) {
        root /www/media;
    }
}
