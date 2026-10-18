# Proyecto Kaori

Lector de manga, manhwa y cómics para Windows, basado en [Kaori de riyaniii](https://github.com/riyaniii/Kaori)
(GPL v3) y en el servidor [Suwayomi](https://github.com/Suwayomi/Suwayomi-Server).

## Actualizaciones

La carpeta [`actualizaciones/`](actualizaciones) es la que consulta Kaori al abrirse y desde
**Menú > Buscar actualizaciones**:

- `latest.json`: número de versión, novedades y la huella SHA-256 del zip.
- `kaori-N.zip`: los archivos de Kaori que cambian (sin el servidor ni Java). Kaori comprueba la
  huella antes de instalar nada y lo instala al reiniciar.

Se publica desde la PC de desarrollo con:

```powershell
.\scripts\publicar-actualizacion.ps1 -Notas "Qué trae esta versión"
```
