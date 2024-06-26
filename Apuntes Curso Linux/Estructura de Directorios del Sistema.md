
# 📂 Descripción de las Rutas del Sistema en GNU/Linux

## 🌟 Directorio Raíz
**El directorio raíz**, simbolizado por el símbolo `/`, es el directorio principal a partir del cual se ramifican todo el resto de directorios.

## 🗂️ Directorios Principales

### 🛠️ Directorio `/bin`
**El directorio `/bin`** es un directorio estático y compartible en el que se almacenan archivos binarios/ejecutables necesarios para el funcionamiento del sistema. Estos archivos binarios pueden ser usados por todos los usuarios del sistema operativo.

### 🚀 Directorio `/boot`
**El directorio `/boot`** es un directorio estático no compartible que contiene todos los archivos necesarios para el arranque del ordenador, excepto los archivos de configuración. Algunos de los archivos indispensables que acostumbra a almacenar el directorio `/boot` son el **kernel** y el gestor de arranque **Grub**.

### 🖥️ Directorio `/dev`
**El sistema operativo GNU/Linux trata los dispositivos de hardware como si fueran archivos**. Estos archivos que representan nuestros dispositivos de hardware se hallan almacenados en el directorio `/dev`. Algunos ejemplos son:

- `cdrom`: representa el dispositivo de CDROM.
- `sda`: representa el disco duro SATA.
- `audio`: representa la tarjeta de sonido.
- `psaux`: representa el puerto PS/2.
- `lpx`: representa la impresora.
- `fd0`: representa la disquetera.

### ⚙️ Directorio `/etc`
**El directorio `/etc`** es un directorio estático que contiene los archivos de configuración del sistema operativo y de diversos programas. Algunos archivos de configuración en `/etc` pueden ser sustituidos o complementados por archivos en `/home`.

### 🏠 Directorio `/home`
**El directorio `/home`** es un directorio variable y compartible, destinado a alojar los archivos personales de los usuarios del sistema operativo, a excepción del usuario root. Aquí se almacenan fotografías, documentos, vídeos, etc.

### 📚 Directorio `/lib`
**El directorio `/lib`** es un directorio estático y compartible que contiene bibliotecas compartidas necesarias para arrancar los ejecutables de `/bin` y `/sbin`.

### 🔧 Directorio `/mnt`
**El directorio `/mnt`** alberga los puntos de montaje de distintos dispositivos de almacenamiento como discos duros externos y particiones de unidades externas.

### 💾 Directorio `/media`
**El directorio `/media`** contiene los puntos de montaje de medios extraíbles de almacenamiento como memorias USB, lectores de CD-ROM, unidades de disquete, etc.

### 📦 Directorio `/opt`
**El directorio `/opt`** es estático y compartible. Almacena programas que no vienen con el sistema operativo como **Spotify**, **Google Earth**, **Google Chrome**, **Teamviewer**, etc.

### 🔍 Directorio `/proc`
**El directorio `/proc`** es un sistema de archivos virtual que proporciona información acerca de los distintos procesos y aplicaciones que se están ejecutando en el sistema operativo.

### 🔐 Directorio `/root`
**El directorio `/root`** es el directorio `/home` del administrador del sistema (usuario root), siendo un directorio variable no compartible.

### 🛡️ Directorio `/sbin`
**El directorio `/sbin`** es estático y compartible. Almacena archivos binarios/ejecutables que solo pueden ser ejecutados por el usuario root o el administrador del sistema.

### 🌐 Directorio `/srv`
**El directorio `/srv`** se usa para almacenar directorios y datos que utilizan ciertos servidores instalados en el ordenador.

### 📄 Directorio `/tmp`
**El directorio `/tmp`** es donde se crean y almacenan archivos temporales y variables necesarios para el correcto funcionamiento de los programas.

### 💽 Directorio `/usr`
**El directorio `/usr`** es compartido y estático, conteniendo la mayoría de programas instalados en el sistema operativo. Todo el contenido de `/usr` es accesible para todos los usuarios y es de solo lectura.

### 📝 Directorio `/var`
**El directorio `/var`** contiene archivos de datos variables y temporales como registros del sistema (logs) y archivos spool. Su principal función es ayudar a detectar y solucionar problemas. Se recomienda ubicar `/var` en una partición propia o fuera de la partición raíz.

### 🔧 Directorio `/sys`
**El directorio `/sys`** contiene información similar a la del directorio `/proc`, con información estructurada y jerárquica acerca del kernel del equipo, particiones, sistemas de archivo, drivers, etc.

### 🛠️ Directorio `/lost+found`
**El directorio `/lost+found`** se crea en particiones de disco con un sistema de archivos ext después de ejecutar herramientas de restauración y recuperación como `fsck`. Si el sistema no ha tenido problemas, este directorio estará vacío. En caso de problemas, contendrá ficheros y directorios recuperados tras la caída del sistema operativo.

