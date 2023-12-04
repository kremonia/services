# Services

## Introduction

Docker compose project to run required infrastructure including wiki.js as a main wiki and gogs as a git server

## TODO

- [x] Add docker volumes for `Wiki.js` and `Gogs`
- [x] Add `OpenProject` to manage projects.

## Usage

Clone this repo.

## Wiki.js

### Build and run

`Wiki.js` is running with it's own instance of `posgreSQL` for ease of future migrations.
To build a container go to `wikijs` folder

```bash
cd wikijs
```

...and execute:

```bash
docker compose up -d
```

It would build and run 2 containers in isolated network. Default external port is `3000`.

### Shutdown

To shutdown whole project just run within `wikijs` folder:

```bash
docker compose stop
```

### Removing

> ⚡ Important: running this command would destroy `Docker` containers and networks. Use volumes to keep your data.

```bash
docker compose down
```

## Gogs

### Build and run

`Gogs` is running with it's own instance of `posgreSQL` for ease of future migrations.
To build a container go to `gogs` folder

```bash
cd gogs
```

...and execute:

```bash
docker compose up -d
```

It would build and run 2 containers in isolated network. Default external port is `3001` for `http` and `3022` for `ssh`.

### Shutdown

To shutdown whole project just run within `gogs` folder:

```bash
docker compose stop
```

### Removing

> ⚡ Important: running this command would destroy `Docker` containers and networks. Use volumes to keep your data.

```bash
docker compose down
```

## OpenProject

### Build and run

`OpenProject` is running with it's own instance of `posgreSQL` for ease of future migrations.
To build a container go to `openproject` folder

```bash
cd openproject
```

...and execute:

```bash
docker compose up -d
```

It would build and run several containers in isolated networks. Default external port is `3002` for `http` (frontend).

### Shutdown

To shutdown whole project just run within `openproject` folder:

```bash
docker compose stop
```

### Removing

> ⚡ Important: running this command would destroy `Docker` containers and networks. Use volumes to keep your data.

```bash
docker compose down
```
