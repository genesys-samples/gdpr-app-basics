---
title: "Actualiza el código e inicia la aplicación"
chapter: false
weight: 20
---

## Actualizar la configuración de la aplicación

- Abra el archivo `/static/js/genesyscloud.js`.
- Establezca las constantes `clientId`, `redirectUrl` y `environment` a los valores que obtuvo de Genesys Cloud anteriormente, por ejemplo:

```js
const clientId = "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx";
const redirectUrl = "http://localhost";
const environment = "mypurecloud.ie"; // Su entorno Genesys Cloud (por ejemplo, mypurecloud.com, mypurecloud.de)
```

Encuentre su entorno [aquí](https://developer.genesys.cloud/platform/api/)

## Iniciar la aplicación

- Instalar la extensión [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) en Visual Studio Code
- Asegúrese de que el archivo `index.html` está abierto en el editor
- Haga clic en `Go Live` para iniciar un servidor web local

Debería poder ver la siguiente página:

![First launch](../images/app_first_launch.jpg)

## ¿Cómo utilizar la aplicación?

### Iniciar una nueva solicitud

- Haga clic en el botón `New Request` (Nueva solicitud)
- Seleccione el tipo de solicitud
  - `Delete` anonimizará los datos de un usuario [PII](https://en.wikipedia.org/wiki/Personal_data)
  - `Export` exportará las actividades de un usuario dentro de Genesys Cloud. El archivo exportado es un conjunto de archivos CSV y JSON.
  - `Update` actualizará los datos de un usuario en todo Genesys Cloud.
- Introduzca un nombre, una dirección, un número de teléfono o una dirección de correo electrónico. Sólo uno de estos campos es obligatorio, pero puedes introducir tantos como quieras para encontrar a la persona adecuada.
- Haga clic en `Search`
- Haga clic en  `Select and Submit` después de haber identificado a la persona correcta

![Search Subject](../images/app_search_subject.jpg)

- Si la solicitud tiene éxito, debería ver lo siguiente:

![Searching](../images/app_searching.jpg)

- Las solicitudes suelen tardar entre 24 y 48 horas en tramitarse. Puede comprobar el estado de su solicitud actualizando la página.

A continuación vaya a [Embedding the app](30_third.html) para integrar esta aplicación en su propia organización de Genesys Cloud.
