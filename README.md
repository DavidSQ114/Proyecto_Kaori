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

La nueva versión de Kaori (más rápida y con más funciones). Lleva todo lo que necesita: **no hace falta tener
Kaori 1 ni Java**, y no pide permisos de administrador.

1. Descarga **`Instalar-Kaori2.exe`** desde [Releases](https://github.com/DavidSQ114/Proyecto_Kaori/releases/latest).
2. Ábrelo y sigue el asistente. Si Windows muestra «Windows protegió tu PC» (pasa con programas nuevos que aún no
   tienen firma digital; no es un aviso de virus), pulsa **Más información › Ejecutar de todas formas**.
3. Listo: aparece **Kaori 2** en el menú Inicio (y en el escritorio, si lo marcaste). La primera vez tarda un poco más
   en abrir: prepara su servidor y descarga su navegador para las fuentes protegidas.

Se instala en `%LOCALAPPDATA%\Programs\Kaori 2` y guarda tus datos en `%LOCALAPPDATA%\Kaori2` (al desinstalar te
pregunta si borrarlos). Quien ya tenía Kaori 2 instalado junto a Kaori 1 puede seguir así: se actualiza igual.

Kaori 2 se actualiza solo: busca actualizaciones al abrirse y una vez al día, y las instala al cerrarlo
(o desde **Apariencia › Actualizaciones**). Las consulta en la carpeta
[`actualizaciones-kaori2/`](actualizaciones-kaori2): `latest.json` y `kaori2-N.zip` (solo los archivos que cambian;
la app comprueba su huella SHA-256 antes de instalar nada).
