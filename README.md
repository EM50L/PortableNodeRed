# PortableNodeRed
Prueba de Node-Red en un entorno portabilizado con el framework electron.

Es una Simplificacion del proyecto https://github.com/EM50L/ElectronArduinoNodeRed  
En esta version al quitar el Puerto Serie no es necesario compilar luego se obtienen algunas mejoras.  

Tambien se le a añadido La traduccion a español
https://github.com/EM50L/Traduccion_es_Node-Red


## Instalacion 
- Windows Descargar 7Z [Github: PortableNodeRed-win32-ia32.7z](https://github.com/EM50L/PortableNodeRed/releases/download/v1.0.0/PortableNodeRed-win32-ia32.7z) 
 (descomprimir y ejecutar.) <!---->
- Linux Descargar 7z [Github: PortableNodeRed-linux-x64.7z](https://github.com/EM50L/PortableNodeRed/releases/download/v1.0.0/PortableNodeRed-linux-x64.7z) 
 (descomprimir y ejecutar.) <!---->

## Compilacion 
```bash
# 1) Clonado del repositorio
git clone https://github.com/EM50L/PortableNodeRed.git
cd PortableNodeRed
npm install --unsafe-perm node-red@next

# 2) Fuerzo version de electron rama 2 (viene con nodev8 mejor para poder usar las apis nativas)
npm install electron@2.0.18

# 3) instalo y resuelvo dependencias.
npm install

# NOTA IMPORTANTE PARA QUE FUNCIONE TODO BIEN
# no deberia aparecer electron-rebuild
# si aparece es porque la version de nodejs que tienes es distinta a la de electron.

# Esta compilacion se ha pensado para electron 2.0.x y node 8.x
# Si no consigues compilarla bajate un paquete precompilado por el autor en "releases"

#Si no tampoco te preocupes solo perderas algunas caracteristicas como posibilidad de gestionar la paleta.

```
