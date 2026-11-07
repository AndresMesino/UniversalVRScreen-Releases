# Seguridad

## Versiones oficiales

Las únicas versiones oficiales de Universal VR Screen son las publicadas en
[Releases](https://github.com/AndresMesino/UniversalVRScreen-Releases/releases) de este repositorio.
Un fork o una copia de este repositorio no es oficial aunque contenga los mismos archivos.

Desarrollador: **Andrés Mesino**.

Cada APK oficial:

- es del paquete `com.universalvr.screen`;
- está firmado con el certificado oficial (CN=Universal VR Screen), cuya huella SHA-256 es
  `B4:71:47:78:94:8B:AA:B5:CA:E7:29:9C:0D:F7:75:48:F7:99:6E:F9:05:8A:66:51:D6:1B:C1:FF:5A:F3:B5:CF`;
- tiene su huella SHA-256 publicada en `SHA256SUMS` y en la propia release.

Lo que prueba la autenticidad es la **firma**: solo quien tiene la clave privada (que no está en
este repositorio ni en la app) puede producir un APK firmado con ese certificado, y Android no
permite actualizar la app con un APK firmado por otro. La huella SHA-256 prueba que el archivo
no se dañó ni cambió.

La app hace estas comprobaciones sola antes de ofrecer una actualización: paquete, versión más
nueva, huella del archivo y firma. La huella del certificado oficial está incorporada en la app:
si el certificado del APK descargado no coincide con ella, muestra una alerta de seguridad,
cancela la instalación y borra el archivo. La clave privada no está en este repositorio ni en la
app. Para comprobarlo a mano:

```bash
apksigner verify --print-certs UniversalVRScreen-<versión>.apk
sha256sum -c SHA256SUMS
```

## Informar de un problema de seguridad

Usa la opción privada de GitHub: pestaña **Security › Report a vulnerability** de este repositorio.
No publiques detalles de una vulnerabilidad en lugares públicos antes de que se corrija.
