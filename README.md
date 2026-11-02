# CoverAO

Descargas oficiales de CoverAO para Windows y Linux.

[Descargar la última versión](https://github.com/Ayrton09/CoverAO/releases/latest)

- **Windows:** descargar y ejecutar `CoverAO-Setup.exe`.
- **Linux:** descargar `CoverAO-x86_64.AppImage`, darle permiso de ejecución y abrirlo.
- **Para alojar un servidor:** elegir `CoverAO-servidor-win-x64.zip` o `CoverAO-servidor-linux-x64.tar.gz`.

La app busca actualizaciones al abrir y comprueba la firma del autor antes de instalarlas.
Los archivos `actualizacion.json`, `actualizacion-linux.json` y `servidor.json` son avisos para los actualizadores.

Este repositorio distribuye los paquetes. El desarrollo se mantiene en un repositorio privado.

Después de un período de pruebas, cuando el juego pase a su lanzamiento público, el código fuente también se hará público.

## Servidor en Docker

El paquete de Linux incluye `Dockerfile` y `docker-compose.yml`, junto con el servidor y el cliente web firmados.
Para actualizarlo, descargar el paquete nuevo y reconstruir la imagen desde su contenido con
`docker compose up -d --build`, conservando el mismo proyecto de Compose y el volumen de partidas.
Eso renueva juntos el servidor y el cliente web. El contenedor no se actualiza por sí solo;
la actualización automática de la app de escritorio funciona por separado.
