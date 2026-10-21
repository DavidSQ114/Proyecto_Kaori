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

## Kaori 2

La nueva versión de Kaori (más rápida y con más funciones). Se instala **junto a tu Kaori** y usa tu misma
biblioteca, tus descargas y tus lecturas; Kaori no cambia y puedes seguir usándolo.

1. Descarga **`Instalar-Kaori2.exe`** desde [Releases](https://github.com/DavidSQ114/Proyecto_Kaori/releases/latest).
2. Ábrelo. Si Windows avisa «Windows protegió tu PC», pulsa **Más información › Ejecutar de todas formas**
   (el instalador no está firmado).
3. Confirma la carpeta de tu Kaori (la encuentra solo) y listo: aparece **Kaori 2** en el escritorio y en el menú Inicio.

Kaori 2 se actualiza solo: busca actualizaciones al abrirse y una vez al día, y las instala al cerrarlo
(o desde **Apariencia › Actualizaciones**). Las consulta en la carpeta
[`actualizaciones-kaori2/`](actualizaciones-kaori2): `latest.json` y `kaori2-N.zip` (solo los archivos que cambian;
la app comprueba su huella SHA-256 antes de instalar nada).
