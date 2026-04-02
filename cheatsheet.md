# Docker
Docker Image bauen:
``` docker build -f dockerfile(.web) -t ghcr.io/jgruetter/<imagename>:v1 (Manifest)```

Auf Registry hochladen: ```docker push <tag>```

Neuer Tag bei Image setzen:
```docker tag <oldtag> <newtag>```

Image ausführen: ```docker run -d -p 8080:80 --name <name> <tag(ganzes image z.B. nginx:v1)>```

In Container rein:
```docker exec -it html-docker-app /bin/sh```

Logs anschauen:

```docker logs <name>```

Container stoppen:

```docker stop <name>```

Container löschen:

```docker rm <name>```

Image löschen:

```docker rmi <imagename>```

Ganze Docker umgebung wegmachen(images, containers, volumes etc.):

```docker system prune -a --volumes```

Alle laufenden Docker-Container anzeigen:

```docker ps```


Alle Docker-Container anzeigen:

```docker ps -a```

# Pod(Container) Aubfau:

Im Pod/Container hat es:

- App (wird im git ausgelagert)
- Middleware (z.b nginx) (im container-registry (cr) ausgelagert)
- Os (z.b alpine) (im container-registry (cr) ausgelagert)

Dockerfile führt es alles zusammen (Bauplan)