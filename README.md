# Radio++ para Windows

Aplicación de radio para Windows con interfaz **Qt/PySide6**, reproducción mediante **libmpv** y búsqueda en el directorio público [Radio Browser](https://www.radio-browser.info/).

## Funciones

- Buscar y escuchar radios antes de guardarlas.
- Añadir estaciones del catálogo con `+`, introducir emisoras propias con nombre y URL y eliminarlas con `−`.
- Reproductor emergente desde el icono de la bandeja: reproducir, pausar, detener y ajustar el volumen.
- Personalizar fuentes, tamaños y colores desde el botón ⚙ del reproductor.
- Preferencias y emisoras guardadas entre ejecuciones en `%APPDATA%\RadioPlusPlusQt\settings.json`. La primera vez se importan los ajustes de una versión anterior de Radio++ si existen.

## Compilar en Windows

Requiere **Python 3.13**, Windows de 64 bits y conexión a Internet durante la compilación:

```powershell
python -m pip install -r requirements.txt
powershell -ExecutionPolicy Bypass -File .\build.ps1
```

El script descarga una versión fija de libmpv de NuGet y comprueba su SHA-256; después genera `dist\RadioPlusPlus-Qt.exe`. El ejecutable es independiente de Python y extrae temporalmente sus componentes al abrirlo.

Para ejecutarlo desde el código fuente, compila primero para obtener libmpv o coloca `libmpv-2.dll` junto a `app.py`, y usa `python app.py`.

El icono `radio-original.png` procede del [applet Radio++ de Cinnamon](https://github.com/linuxmint/cinnamon-spices-applets/tree/092e3f889e27dc98ee3734651bd777efb286c95d/radio%40driglu4it); `radio-original.ico` es una conversión del mismo icono. Respeta las condiciones de licencia del proyecto original al redistribuir sus recursos.

## Note
> This project was "vibecoded" Inspired by the Radio++ Applet For Cinnamon By jonath92. 
