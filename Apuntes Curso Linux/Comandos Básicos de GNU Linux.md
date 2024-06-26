
# 📜 Comandos Básicos de GNU/Linux

## 🔍 Navegación y Visualización

### 🌐 Zoom
- **Acercar** ➜ `[CTRL] + [+]`
- **Alejar** ➜ `[CTRL] + [-]`

### 📁 Directorio de Trabajo
- **Imprimir directorio de trabajo** ➜ `pwd`
- **Borrar el terminal** ➜ `[CTRL] + [l]` o `clear`

### 📂 Directorios
- **Moverse a un directorio específico** ➜ `cd [name-of-your-directory]`
- **Moverse al directorio principal** ➜ `cd ..`
- **Ir al directorio de inicio** ➜ `cd ~`
- **Moverse al último directorio en el que estaba** ➜ `cd -`

### 📜 Listar Archivos y Directorios
- **Enumerar archivos y directorios visibles** ➜ `ls`
- **Incluir archivos ocultos** ➜ `ls -a`
- **Formato de lista larga** ➜ `ls -l`
- **Formato legible por humanos** ➜ `ls -lh`
- **Combinando argumentos** ➜ `ls -lah`
- **Más información sobre `ls`** ➜ `man ls`

## 🔎 Búsqueda

- **Buscar el binario de un programa** ➜ `which [name-of-the-program]`
- **Buscar manual, binario y fuente de un programa** ➜ `whereis [name-of-the-program]`
- **Buscar archivos y directorios por nombre** ➜ `find [path-to-search] -iname [name-of-the-file-you-want-to-search]`
- **Más información sobre `find`** ➜ `man find`
- **Breve descripción de un comando** ➜ `whatis [command-name]`

## 📖 Historial de Comandos

- **Obtener comandos anteriores (uno por uno)** ➜ `[Up Arrow]`
- **Obtener comandos anteriores (lista completa)** ➜ `history`
- **Repetir un comando específico** ➜ `![number-of-the-command-to-repeat]`
- **Repetir el último comando** ➜ `!!`

## 🛠️ Trabajar con Archivos y Directorios

### 📝 Creación
- **Crear un nuevo archivo (sin abrirlo)** ➜ `touch [name-of-your-file]`
- **Crear un nuevo archivo usando un editor de texto** ➜ `vim [name-of-your-file]` o `nano [name-of-your-file]`
- **Crear un nuevo directorio** ➜ `mkdir [new-directory-name]`

### 🗑️ Eliminación
- **Eliminar un archivo** ➜ `rm [name-of-your-file]`
- **Eliminar un directorio vacío** ➜ `rmdir [name-of-the-directory]`
- **Eliminar un directorio recursivamente** ➜ `rm -rf [name-of-your-directory]`

### 📄 Manipulación
- **Copiar un archivo** ➜ `cp [source-path] [destination-path]`
- **Mover un archivo** ➜ `mv [source-path] [destination-path]`
- **Cambiar el nombre de un archivo** ➜ `mv [old-name] [new-name]`

### 📜 Concatenación
- **Ver un archivo** ➜ `cat [name-of-your-file]`
- **Ver un archivo con números de línea** ➜ `cat -n [name-of-your-file]`
- **Copiar contenido de un archivo a otro** ➜ `cat [source-file] > [destination-file]`
- **Más información sobre `cat`** ➜ `man cat`

### 🔍 Buscar en Archivos (Grep)
- **Buscar una cadena dentro de un archivo** ➜ `grep [term] [file]`
- **Búsqueda sin distinguir mayúsculas/minúsculas** ➜ `grep -i [term] [file]`
- **Buscar líneas que no coincidan** ➜ `grep -v [term] [file]`
- **Búsqueda recursiva en directorios** ➜ `grep -r [term] [path]`
- **Buscar múltiples términos** ➜ `grep -E "[term1|term2]" [file]`
- **Contar resultados** ➜ `grep -c [term] [file]`
- **Mostrar archivos coincidentes** ➜ `grep -l [term] [files]`
- **Más información sobre `grep`** ➜ `man grep`

## 🚀 Atajos de Teclado

- **Buscar en el historial de comandos** ➜ `[CTRL] + r`
- **Pegar líneas anteriores** ➜ `[CTRL] + p`
- **Mover el cursor al principio de la línea** ➜ `[CTRL] + a`
- **Mover el cursor al final de la línea** ➜ `[CTRL] + e`
- **Mover el cursor un carácter adelante** ➜ `[CTRL] + f`
- **Mover el cursor un carácter atrás** ➜ `[CTRL] + b`
- **Borrar la línea completa** ➜ `[CTRL] + u`
- **Borrar la última palabra escrita** ➜ `[CTRL] + w`

## 📚 Trabajar con Archivos Largos

- **Imprimir las últimas líneas de un archivo** ➜ `tail [file]`
- **Imprimir las últimas n líneas de un archivo** ➜ `tail -n [number] [file]`
- **Imprimir las primeras líneas de un archivo** ➜ `head [file]`
- **Imprimir las primeras n líneas de un archivo** ➜ `head -n [number] [file]`
- **Ojear un archivo** ➜ `less [file]`

## 🔄 Permisos y Propiedades

### 🔐 Cambiar Permisos (chmod)
- **Agregar permiso de ejecución a todos** ➜ `chmod a+x [file]`
- **Quitar permiso de ejecución a todos** ➜ `chmod a-x [file]`
- **Agregar permiso de ejecución al propietario** ➜ `chmod u+x [file]`
- **Eliminar permiso de escritura a otros usuarios** ➜ `chmod o-w [file]`
- **Agregar permiso de lectura al grupo** ➜ `chmod g+r [file]`
- **Quitar permiso de escritura y lectura a todos** ➜ `chmod a-wr [file]`
- **Quitar permisos de escritura y lectura a todos los archivos en el directorio actual** ➜ `chmod a-wr *.*`

### 🔧 Trabajar con Grupos
- **Listar todos los grupos disponibles** ➜ `getent group`
- **Listar todos los grupos a los que pertenece una cuenta** ➜ `groups`
- **Buscar un grupo específico** ➜ `getent group | grep [group-name]`
- **Crear un nuevo grupo** ➜ `sudo groupadd [new-group]`
- **Agregar un usuario a un grupo secundario** ➜ `usermod -a -G [group] [user]`

### 👥 Cambiar Propietario (chown)
- **Cambiar propietario de un archivo** ➜ `sudo chown [new-owner] [file]`
- **Cambiar propietario de varios archivos** ➜ `sudo chown [new-owner] [file1] [fileN]`
- **Cambiar propietario de un directorio** ➜ `sudo chown [new-owner] [directory]`
- **Cambiar recursivamente propietario de un directorio y sus archivos** ➜ `sudo chown -R [new-owner] [directory]`
- **Cambiar grupo propietario de un archivo** ➜ `sudo chown :[new-group] [file]`
- **Cambiar propietario y grupo de un archivo** ➜ `sudo chown [new-owner]:[new-group] [file]`

