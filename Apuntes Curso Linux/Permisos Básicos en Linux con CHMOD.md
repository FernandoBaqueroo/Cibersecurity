
# 🛡️ Permisos Básicos en Linux con CHMOD

Manipular los permisos en Linux es esencial para asegurar la integridad y seguridad de archivos y directorios. Los permisos se dividen en cuatro partes: tipo, propietario, grupo y otros.

---

## 📋 Descripción de Permisos

- **`drwx——`**: Ejemplo de permisos de un directorio.
- **`-rw-rw-r–`**: Ejemplo de permisos de un archivo.

El primer carácter indica el tipo de archivo (`d` para directorio, `-` para archivo). Los siguientes nueve caracteres se dividen en tres grupos de tres:

- **Propietario**: `rw-` (lectura, escritura, sin ejecución).
- **Grupo**: `rw-` (igual que propietario).
- **Otros**: `r–` (lectura, sin escritura ni ejecución).

---

## 🚀 Significado de Permisos

- **`r`**: Lectura (read).
- **`w`**: Escritura (write).
- **`x`**: Ejecución (execute).
- **`–`**: Permiso deshabilitado.

---

## 🛠️ Configuración de Permisos con CHMOD

### Método Simbólico

- `chmod u+w prueba.txt`: Agrega permiso de escritura al usuario.
- `chmod g+rw prueba.txt`: Da permisos de lectura y escritura al grupo.
- `chmod g=rwx prueba.txt`: Establece todos los permisos para el grupo.

### Método Numérico

- Los permisos se representan con números del 0 al 7.
- Ejemplo: `chmod 755 prueba.txt` asigna permisos específicos a propietario, grupo y otros.

### Ejemplos Comunes

- `chmod 600 notas.txt`: `rw-------` (permisos solo para el propietario).
- `chmod 644 prueba.txt`: `rw-r--r--` (lectura y escritura para el propietario, solo lectura para grupo y otros).
- `chmod 777 archivo`: `rwxrwxrwx` (permisos completos para todos los usuarios).

---

## 🌟 Últimos Detalles

Los permisos son fundamentales para la seguridad en sistemas Unix. La práctica y la experimentación ayudan a comprender mejor su funcionamiento.

---

Este texto proporciona una guía clara y estilizada sobre cómo gestionar los permisos en Linux usando el comando `chmod`, con ejemplos prácticos y una estructura organizada para facilitar su comprensión.

