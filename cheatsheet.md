# Befehle

## Docker
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

## OpenShift Befehle:

Alle Projekte anzeigen:
```oc projects```

Projekt wechseln:
```oc project <name>```

# Quizfragen

## Unterschied Monitoring / Logging:

Monitoring ist echtzeit Metriken
Logging fehleranalyse (vergangenheit)

## Pod(Container) Aubfau:

Im Pod/Container hat es:

- App (wird im git ausgelagert)
- Middleware (z.b nginx) (im container-registry (cr) ausgelagert)
- Os (z.b alpine) (im container-registry (cr) ausgelagert)

Dockerfile führt es alles zusammen (Bauplan)

## 3 Layers von Kubernetes (Container Runtime Engine, Container Orchestry, Orchestry enhancment)

- CE (Container Engine) Aufg. 3.2
    - containerd
    - docker
    - podman
    - CRI-O (OpenShift)
- CO (Container Orchestry) Aufg. 4.2
    - Kubernetes (K8s, K3s, MiniKube etc.)
    - Docker Compose
    - Swarm
- COE (Container Orcherstry enhancment) (basiert immer auf Kubernetes) Aufg. 6.2
    - OpenShift
    - OKD (OpenShift open-source)
    - Ranger
    - Tanzu

Ist Kubernetes eine Container Engine? -> Nein, es ist eine Conteiner Ocherstrierung

## Horizontale/ Vertikale Skaliereung

Horizontale: Mehr maschienen aufbauen (Container)

Vertikale: Mehr Rechenleistung auf host nehmen/machen (VM's)


## 5 Merkmale der Cloud nach NIST

- On-Demand Self service
    - API
    - CLI
    - Web-Gui
- Broad Network Access
- Recource Pooling
    - Wirtschaftsbegriff: Economy of Scale
- Rapid Elasticity
    - Hoch/Runter skalieren
    - Container -> Horizintal
    - VM's -> Vertikal
- Measured Service


Wie heisst der Wirtschaftsbegriff, welche sich Cloud-Anbieter zum Geld machen brauchen: economies of scale

## Cloud Service Modelle (Wo liegt die Verantwortung)

![image](images/service_models.png)

- FaaS
- SaaS
- PaaS
- IaaS
- On-Prem
  
## Deployment-Modelle

- Public Cloud
- Private Cloud
- Community Cloud (wird geteilt von der Interessensgemeinschaft)
- Hybrid Cloud

## Shared Responsibility:

Für wer Cloud Anbieter zuständig?
SLA

## Was ist Dockerfile?
Baupläne für Images

## Zentrale Technische Grundlage für Cloud Computing:
- Virtualisierung


## Container Runtime Engines:


# Kubernetes

## Cheatsheet:
![image](images\kubernetes_cheatsheet.png)

## Alle .yaml Dateien in Verzeichnis applyen:
```kubectl apply -f .```

