---
title: "Primeros pasos"
chapter: false
weight: 10
---

## Requirimientos

- [Visual Studio Code](https://code.visualstudio.com/)
- Git
- Genesys Cloud organization

## Crear un cliente OAuth

El sitio web utilizará Genesys Cloud OAuth para autenticar a los usuarios, por lo que primero deberá crear un nuevo id/secreto de cliente OAuth `implicit grant` en su organización Genesys Cloud.

- Abra Genesys Cloud, vaya a `Admin` y haga clic en `OAuth` (en `Integrations`)
- Haga clic en "Añadir cliente
- Dé un nombre a su aplicación (por ejemplo, "Solicitudes GDPR"). La descripción es opcional.
- Seleccione `Token Implicit Grant (Browser)`.
- Introduzca `http://localhost:3000` como `Redirect URI`.
- En la sección `Scope`, seleccione `gdpr` y `gdpr:readonly`.
- Haga clic en `Guardar` y anote el valor de la cadena `Client ID`.

## Descargar el código fuente

- Ejecute `git clone https://github.com/PierrickI3/genesyscloud-gdpr-requests` para obtener el último código
- Use vscode para abrir los archivos:
  - `cd genesyscloud-gdpr-requests`
  - `code .`

A continuación, vaya a [Actualizar el código y lanzar la aplicación](20_second.html) para lanzar la aplicación localmente.
