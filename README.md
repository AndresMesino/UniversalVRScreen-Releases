# Universal VR Screen

**Canal oficial de distribución.** Aquí se publican las versiones de Universal VR Screen para Android: el APK de cada versión, sus novedades y la información para verificar que es auténtico.

Desarrollador: **Andrés Mesino**.

Universal VR Screen convierte tu teléfono en una pantalla para gafas VR tipo Cardboard o VR Box: muestra cualquier app instalada (videos, navegador, juegos sencillos) duplicada para cada ojo en formato Side-by-Side, con corrección de lente, pantalla fija en el espacio y escenarios como un cine o el espacio.

## Descargar

➡️ **[Última versión](https://github.com/AndresMesino/UniversalVRScreen-Releases/releases/latest)**: en *Assets*, descarga el archivo `UniversalVRScreen-<versión>.apk`.

Descarga el APK solo desde esta página. Las copias publicadas en otros sitios o en forks de este repositorio no son oficiales.

## Instalar por primera vez

1. Abre en el teléfono la página de la última versión y descarga el `.apk`.
2. Ábrelo. Si Android lo pide, permite **instalar apps desconocidas** para tu navegador o gestor de archivos, solo para esta instalación.
3. Instala **[Shizuku](https://play.google.com/store/apps/details?id=moe.shizuku.privileged.api)** (gratuita). Universal VR la usa para abrir otras apps dentro de la vista VR.
4. Abre Universal VR Screen y sigue la pantalla principal: te indica paso a paso cómo iniciar Shizuku (necesitas activar las Opciones de desarrollador y estar en una red Wi-Fi solo para iniciarlo).

## Actualizaciones

No hace falta volver a esta página: al abrir la app, si hay una versión nueva, aparece un aviso con sus novedades y el botón **Actualizar ahora**. También puedes buscarla en *Configuración › Buscar actualizaciones*.

Antes de instalar, la app verifica la descarga: que sea de Universal VR Screen, que sea más nueva, que coincida su huella SHA-256 y que esté firmada con el certificado oficial. Android siempre pide tu confirmación; nada se instala solo.

## Verificar la autenticidad

Cada APK oficial está firmado con el certificado de **Andrés Mesino** (CN=Universal VR Screen), cuya huella SHA-256 es:

```text
B4:71:47:78:94:8B:AA:B5:CA:E7:29:9C:0D:F7:75:48:F7:99:6E:F9:05:8A:66:51:D6:1B:C1:FF:5A:F3:B5:CF
```

Con las herramientas de Android (`apksigner`) puedes comprobarlo:

```bash
apksigner verify --print-certs UniversalVRScreen-<versión>.apk
```

La app trae esta huella incorporada: antes de instalar una actualización compara el certificado del APK descargado con ella y, si no coincide, cancela la instalación y borra el archivo. Cada versión incluye también `SHA256SUMS` con la huella del archivo (integridad); la autenticidad la da la firma. Ver [SECURITY.md](SECURITY.md).

## Requisitos

- Android 10 o superior.
- [Shizuku](https://github.com/RikkaApps/Shizuku) instalado.
- Gafas VR compatibles con formato Side-by-Side (Cardboard, VR Box o similares).

Las apps protegidas (contenido con DRM, apps de bancos) se ven en negro: Android no permite mostrarlas fuera de su pantalla.

## Privacidad

Universal VR Screen no recopila ni envía datos personales. Solo se conecta a internet para consultar este repositorio en busca de actualizaciones.

## Sobre este repositorio

Este repositorio contiene únicamente versiones publicadas y su documentación; el código fuente no es público. Solo el propietario puede publicar versiones, la rama principal y las etiquetas de versión están protegidas, y las versiones publicadas no se pueden modificar.

Historial de cambios: [CHANGELOG.md](CHANGELOG.md).

© Andrés Mesino. Todos los derechos reservados.
