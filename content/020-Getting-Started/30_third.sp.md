---
title: "Integrar la aplicación"
chapter: false
weight: 30
---

## Publicación de la aplicación

La aplicación ya está lista para ser utilizada en Genesys Cloud. Hay varias formas de utilizarla:

### Usando localhost

Esto es lo que ha estado haciendo hasta ahora. Puede mantener la aplicación ejecutándose localmente y utilizarla en su organización de Genesys Cloud, sin embargo **sólo funcionará desde su propio ordenador**.

### Usando su propio dominio

Puede copiar el código fuente en su(s) propio(s) servidor(es) web. Asegúrese de que se pueda acceder a la aplicación a través de una URL de acceso público (e.g. `https://mydomain.com/gdpr-requests`).

### Páginas de Github

Puede alojar este sitio web estático utilizando las páginas de Github si tiene una cuenta de Github. Esto es práctico porque le dará una URL `https` gratuita. Las credenciales en `static/js/genesyscloud.js` no son críticas, ya que requiere que cualquiera que lo use también ingrese su nombre de usuario y contraseña para autenticarse.

Una página de muestra está disponible [aquí] (https://github.com/purecloudgdprrequests/purecloudgdprrequests.github.io). En este caso, la 'URI de redirección autorizada' es 'https://purecloudgdprrequests.github.io/index.html'

## Incruste la aplicación en su organización

Para incrustar su sitio web directamente dentro de Genesys Cloud, necesita crear una nueva `Integración`

- Vaya a `Admin/Integrations` y haga clic en `+Integrations` en la parte superior derecha para añadir una nueva aplicación cliente.
- En la pestaña "Detalles":
  - Introduzca un nombre para la nueva aplicación cliente
- En la pestaña "Configuración", introduzca lo siguiente:
  - URL de la aplicación: La ruta completa a la página de inicio de su sitio (por ejemplo, [https://purecloudgdprrequests.github.io](https://purecloudgdprrequests.github.io))
  - Tipo de aplicación: widget
  - Categoría de la aplicación: (dejar vacío)
  - Opciones de Iframe Sandbox: allow-scripts,allow-same-origin,allow-forms,allow-modals (valor por defecto)
  - Filtrado por grupos: Seleccione un grupo de usuarios que puedan acceder a esta aplicación cliente. Puede que tenga que crear un nuevo grupo primero en `Admin/Grupos`.
  - Haga clic en `Guardar`.
- Vuelva a la pestaña `Detalles` y haga clic en `Activo` para activar esta aplicación.

Es posible que tengas que cerrar la sesión y volver a iniciarla para ver la aplicación en la sección `Apps` de la izquierda.

![Embedded app](../images/app_icons.jpg)

Salta a la sección [Conclusión](../090-Conclution/_index.html) para leer lo que has conseguido.
