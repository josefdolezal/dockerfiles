# Data StewardShip Wizard

This image contains environment for local DSW local development.

Create container using following command:

```bash
$ docker run --name dsw -v"/Development/dsw-server:/src/backend" -v"/Development/dsw-client:/src/frontend" -p8080:80 -it josefdolezal/dsw-local
```

The frontend application is expected to run on port `80` (in container) and is accessible on `localhost:8080` on host.
Both shared volumens are used for demonstration, container the does not run/builds source itself.
To build the application inside the container, run:

```
$ docker exec -it dsw bash
$ <your build command>
```
