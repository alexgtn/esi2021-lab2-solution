# ESI2021 Lab 2 solution

1. Run `docker-compose up` to start the services (use `-d` flag optionally to start in background)
2. Observe the output of the `frontend` container.
```
frontend_1  | User-Agent: curl/7.64.0
frontend_1  | X-Forwarded-Host: localhost:8090
frontend_1  | X-Forwarded-Port: 8090
frontend_1  | X-Forwarded-Server: cf7e90c3adbf
frontend_1  | X-Real-Ip: 10.10.1.1
frontend_1  | Accept-Encoding: gzip
frontend_1  | Accept: */*
frontend_1  | X-Forwarded-For: 10.10.1.1
frontend_1  | X-Forwarded-Prefix: /v1
frontend_1  | X-Forwarded-Proto: http
frontend_1  | hello
frontend_1  |   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
frontend_1  |                                  Dload  Upload   Total   Spent    Left  Speed
100   249  100   249    0     0   243k      0 --:--:-- --:--:-- --:--:--  243k
frontend_1  | Accept: */*
frontend_1  | X-Forwarded-For: 10.10.1.1
frontend_1  | X-Forwarded-Host: localhost:8090
frontend_1  | X-Forwarded-Port: 8090
frontend_1  | X-Forwarded-Prefix: /v2
frontend_1  | X-Forwarded-Server: cf7e90c3adbf
frontend_1  | User-Agent: curl/7.64.0
frontend_1  | X-Real-Ip: 10.10.1.1
frontend_1  | X-Forwarded-Proto: http
frontend_1  | Accept-Encoding: gzip
frontend_1  | hello
simple_frontend_1 exited with code 0
```
3. You should be able to observe the `X-Forwarded-Prefix` header in the responses. This header is added by the proxy to inform about the path prefix that was removed.
4. Go to `localhost:8080` and explore the Traefik Dashboard.
