Image bauen mit Dockerfile:

```docker build -t webserver .```

Auf Registry Pushen

Container starten:

```docker run -d -p 8081:80 webserver```