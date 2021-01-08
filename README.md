# Instalar fuente en servidores AWS
Primero se debe descar la fuente y copiar al servidor  
Crear una una carpeta **local** la ruta **/usr/share/fonts/**  
Dentro de la carpera **local** crear la carpeta que contendrá la familia de fuentes(tipografia) por ejemplo **Roboto**  
   
    [root@ip-172-31-44-28 Roboto]# ls -ltr
    total 2064
    -rw-r--r--. 1 root root 175872 Jan  8 03:38 Roboto-ThinItalic.ttf
    -rw-r--r--. 1 root root 171272 Jan  8 03:38 Roboto-Regular.ttf
    -rw-r--r--. 1 root root 176428 Jan  8 03:38 Roboto-MediumItalic.ttf
    -rw-r--r--. 1 root root 171656 Jan  8 03:38 Roboto-Medium.ttf
    -rw-r--r--. 1 root root 170012 Jan  8 03:38 Roboto-Light.ttf
    -rw-r--r--. 1 root root 171500 Jan  8 03:38 Roboto-Thin.ttf
    -rw-r--r--. 1 root root 176184 Jan  8 03:38 Roboto-LightItalic.ttf
    -rw-r--r--. 1 root root 173516 Jan  8 03:38 Roboto-Italic.ttf
    -rw-r--r--. 1 root root 174520 Jan  8 03:38 Roboto-BoldItalic.ttf
    -rw-r--r--. 1 root root 170348 Jan  8 03:38 Roboto-Bold.ttf
    -rw-r--r--. 1 root root 177120 Jan  8 03:38 Roboto-BlackItalic.ttf
    -rw-r--r--. 1 root root 171072 Jan  8 03:38 Roboto-Black.ttf
    -rw-r--r--. 1 root root  11560 Jan  8 03:38 LICENSE.txt
    
Dentro de esta carpeta copiar todos las fuentes(tipografias)  
Una vez copiado las tipografias se debe ejecutar el comando 

    # fc-cache -fv /usr/share/fonts/local/   
        
Si la herramienta no se encuentra instalafo y el servidor es un red hat ejecutar el siguiente comando  

    # yum install fontconfig 
     
Al ejecutar el comando `# fc-cache -fv /usr/share/fonts/local/` debe aparecer el siguiente mensaje 
    
    [root@ip-172-31-44-28 opt]# fc-cache -fv /usr/share/fonts/local/
    /usr/share/fonts/local: caching, new cache contents: 0 fonts, 1 dirs
    /usr/share/fonts/local/Roboto: caching, new cache contents: 12 fonts, 0 dirs
    /usr/lib/fontconfig/cache: cleaning cache directory
    /root/.cache/fontconfig: not cleaning non-existent cache directory
    /root/.fontconfig: not cleaning non-existent cache directory
    /usr/bin/fc-cache-64: succeeded

