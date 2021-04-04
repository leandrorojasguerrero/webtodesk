![loading](https://user-images.githubusercontent.com/51413896/113513532-d7b69200-952f-11eb-9c2d-e9fb455a53a6.png)
# webtodesk
WebToDesk convierte su sitio web en una aplicación de escritorio nativa basada en el marco Electron . Sin aprender ningún lenguaje de programación, puede crear su aplicación macOS, Windows y Linux.

#Estructura de archivos

node_modules: todas las dependencias incluidas en esta carpeta (Electron).
Carpeta pública: todas las imágenes utilizadas, archivos de hoja de estilo incluidos en esta carpeta.
Carpeta de compilación: incluye todos los iconos de aplicaciones.
carpeta dist Archivos de paquetes construidos, las aplicaciones están aquí
config.js: archivo de configuración de la aplicación. (Nombre de la aplicación, URL, tamaños de ventana de la aplicación y más).
package.json: aplicación NodeJS y detalles del paquete.
menu-config.js - Plantilla de menú principal

#Personalización y configuraciones

Cambiar la URL de la aplicación
En la carpeta de su proyecto, abra el archivo config.js. Cambiar el valor de websiteUrl.

//Main Application URL
'websiteUrl' : 'http://example.com',

#Cambiar el nombre de la aplicación
Primero, debe cambiar el atributo de nombre del archivo package.json en el directorio raíz de la aplicación.

"name": "New_App_Name",

Siguiente, modify config.js archivo appName.


'appName' : 'WebToDesk',
#Cambiar la descripción de la aplicación
Primero debe cambiar el atributo de descripción package.json del directorio raíz de la aplicación.


"description": "Convertir un sitio web en una aplicación de escritorio",
#Cambiar el ancho y el alto
Abra el archivo config.js de su aplicación, luego cambie los valores de altura, ancho, minHeight y minWidth.


// Ancho y alto de la ventana de la aplicación
'ancho': Reemplazar_Valor,
'altura': Reemplazar_Valor,
'minWidth': Reemplazar_Valor,
'minHeight': Reemplazar_Valor,


Importante: valores predeterminados
Alto: 800px
Ancho: 600px
minAltura: 0
minWidth: 0

#Ejecutar Aplicación localmente
En la carpeta de su proyecto, simplemente abra las herramientas de la línea de comandos / terminal e instale todas las dependencias.

Primero debe instalar la versión más reciente de Node.js de su computadora


Ejecute el siguiente comando.

$ npm install

Después de instalar con éxito todas las dependencias, ejecute el siguiente comando.


$ npm start

Cree la aplicación para plataformas
Ahora puede utilizar esta aplicación personalizada para crear aplicaciones plataformas macOS, Windows y Linux.


Importante
Usuario de macOS: puede crear la versión macOS, Windows y Linux de su aplicación
Usuario de Windows: solo puede compilar versiones de Windows y Linux únicamente



Plataformas compatibles
Mac OS
Solo se proporcionan archivos binarios de 64 bits para macOS. La versión mínima de macOS admitida es macOS 10.10 (Yosemite).
Ventanas
Se admiten Windows 7 y posteriores. Los sistemas operativos más antiguos no son compatibles (no funcionan).
Linux
Los binarios precompilados ia32 (i686) y x64 (amd64) de Electron están construidos en Ubuntu 12.04, el binario armv7l está construido contra ARM v7 con hard-float ABI y NEON para Debian Wheezy.
