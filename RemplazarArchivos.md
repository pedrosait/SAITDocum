# Como Remplazar archivos desde FoxPro
### 29 de Octubre del 2022
#### Hugo Sicairos Molina

En FoxPro, hay una manera facil de remplazar archivos desde el archivo con el que se está trabajando, hacía la ruta a la cual se hara la prueba de dicha ventana

Para ello, en la ventana de comando escribimos ``` modi comm ``` + el nombre que deseemos dar a ese archivo de comandos
```vfp
modi comm make
```
Se abrira una nueva ventana de comando con extensión .prg

En ella escribiremos varias lineas
``` set safety off ``` permite que Foxpro no muestre un cuadro de dialogo preguntando si deseamos sobreescribir los archivos
``` copy file ``` + la ruta del archivo con el que se esta trabajando
``` to ``` + la ruta hacía donde se pegaran los archivos

```vfp
set safety off

copy file C:\\ejercicios\catLinea.* to C:\\sait\empresa\catLinea.*  
```

