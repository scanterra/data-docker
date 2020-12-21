# Geoserver Data Docker

[![Actions Status](https://github.com/scanterra/data-docker/workflows/build/badge.svg)](https://github.com/scanterra/data-docker/actions)

## Contenido

* [Informacion general](#informacion-general)
* [Tecnologias](#tecnologias)
* [Setup](#setup)
* [CI/CD](#ci/cd)
* [Referencias](#referencias)

## Informacion General

Este repositorio es un fork del repositorio [data-docker](https://github.com/GeoNode/data-docker).  
Actualmente estamos usando la versión desde el commit: `f9dbe4944981e617c5ce6de23c4753095c73344e`.
Su principal función es descargar y asignar el directorio `/geoserver_data/data/` en un volumen, para luego ser usado por el contenedor **geoserver**.

Scanterra no realizó cambios en este repositorio.
	
## Tecnologias

Las mismas utilizadas en [data-docker](https://github.com/GeoNode/data-docker).

* Utiliza:
* Imagenes: 
    - [alpine](https://hub.docker.com/_/alpine)

## Setup

La generación de imágenes solo utiliza el Dockerfile local del repositorio.

- Requerimientos:
    - [`Docker`](https://docs.docker.com/)
- Generar imágen `scanterra/data-docker:latest`
    - `docker build -t scanterra/data-docker:latest .`

### CI/CD

Se deben configurar los siguientes secrets en este repositorio:
- **Docker Hub**, credenciales con los permisos necesarios para acceder, pullear y pushear a la organización [**Scanterra**](https://hub.docker.com/orgs/scanterra).
  - **DOCKERHUB_USERNAME:** nombre del usuario
  - **DOCKERHUB_PASSWORD:** contraseña del usuario

Ver este [documento](https://github.com/scanterra/scanterra_quickstart) con la información del flujo de CI/CD.

## Referencias

- [Readme Anterior](/README_OLD.rst)
