Image bauen mit Dockerfile:

```docker build -t webserver .```

Container starten:

```docker run -d -p 8081:80 webserver```