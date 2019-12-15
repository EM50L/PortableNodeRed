# PortableNodeRed
Prueba de Node-Red en un entorno portabilizado con el framework electron.

Es una Simplificacion del proyecto https://github.com/EM50L/ElectronArduinoNodeRed  
En esta version al quitar el Puerto Serie no es necesario compilar luego se obtienen algunas mejoras.  

Tambien se le a añadido La traduccion a español
https://github.com/EM50L/Traduccion_es_Node-Red


## Instalacion 
- Windows Descargar Github: 
    * [PortableNodeRed-win32-ia32.7z](https://github.com/EM50L/PortableNodeRed/releases/download/v1.0.0/PortableNodeRed-win32-ia32.7z) o [PortableNodeRed-win32-ia32.zip](https://github.com/EM50L/PortableNodeRed/releases/download/v1.0.0/PortableNodeRed-win32-ia32.zip)
    * Descomprimir y ejecutar. <!---->
- Linux Descargar Github: 
    * [PortableNodeRed-linux-x64.7z](https://github.com/EM50L/PortableNodeRed/releases/download/v1.0.0/PortableNodeRed-linux-x64.7z) 
    * descomprimir y ejecutar. <!---->

### nota: funcionabilidad.
Para poder gestionar la paleta. (posibilidad de añadir nodos)  
necesitas instalar npm (nodejs)  
- Windows instala node v8 desde aqui: 
    * https://nodejs.org/dist/latest-v8.x/    
    ej: https://nodejs.org/dist/latest-v8.x/node-v8.16.0-x86.msi (ultima version para 32bits en el momento en el que escribi el archivo.)  

- Linux preferiblemente instala node desde el gestor de paquetes. 
(para que las dependencias y librerias del sistema queden bien resueltas)
   * debian / ubuntu / Mint : `apt-get install nodejs` 
   * CentOS : `yum install nodejs`   
   * Fedora : `dsf install nodejs`
   * FreeBSD : `pkg install nodejs` 

<!-- https://www.digitalocean.com/community/tutorials/package-management-basics-apt-yum-dnf-pkg -->
 
## Compilacion 

```bash

# 1) Clonado del repositorio
git clone https://github.com/EM50L/PortableNodeRed.git
# Nota si no tienes git descarga y descomprime https://github.com/EM50L/PortableNodeRed/archive/master.zip

cd PortableNodeRed
npm install --unsafe-perm node-red



# 2) Fuerzo version de electron rama 2 (viene con nodev8 mejor para poder usar las apis nativas)
npm install electron@2.0.18
# Para mas info consulta: https://electronjs.org/docs/development/upgrading-node y https://github.com/electron/node


# 3) instalo y resuelvo dependencias.
npm install

# NOTA IMPORTANTE PARA QUE FUNCIONE TODO BIEN
# no deberia aparecer electron-rebuild
# si aparece es porque la version de nodejs que tienes es distinta a la de electron.

# Esta compilacion se ha pensado para electron 2.0.x y node 8.x
# Si no consigues compilarla bajate un paquete precompilado por el autor en "releases"

#Si no tampoco te preocupes solo perderas algunas caracteristicas como poder cambiar el app.asar a otro framework.

```

## prueba ejecucion
```bash
npm start
```


## Empaquetado de la aplicacion / Packaging your application
Hacer la aplicacion portable con electron. / making a portable app width Electron.
```
# https://github.com/Urucas/electron-packager-interactive

#Instalar epi / Install epi
npm install -g electron-packager-interactive

# ejecutar / Run it
epi

#ojo escoger la version de electron adecuada 2.0.18 (la misma con la que se ha compilado la aplicacion)

```

## License [CC0 (Public Domain)](LICENSE.md)

## Codigo de referencia / Reference Code (parts of code more explained)
 - **Node-RED Embedding into an existing app** https://nodered.org/docs/embedding
 - **Electron First App** https://electronjs.org/docs/tutorial/first-app 
 - **Electron Menus** https://www.christianengvall.se/electron-menu/ 
 
## Tablas comparativas (para cuadrar versiones entre electron , node-red y serialport ) 
 - https://electronjs.org/docs/development/upgrading-node   
 - https://github.com/electron/node  
 - https://nodered.org/docs/faq/node-versions  
 - https://nodejs.org/en/download/releases/
 - https://serialport.io/docs/guide-platform-support  
 Normalmente la version de node para no tener que compilar es la 57

## [pagina personal del autor: jejo.es](https://jejo.es/categories/node-red/)
