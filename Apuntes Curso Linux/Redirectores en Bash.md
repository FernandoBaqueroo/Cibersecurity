# 📄 Redirecciones en Bash

| **Redirección**           | **Descripción**                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `cmd > archivo`           | 🔄 **Redirige** la salida estándar (stdout) de `cmd` a un archivo.                                                                               |
| `cmd 1> archivo`          | 🔄 **Igual** que `cmd > archivo`. `1` es el descriptor de archivo predeterminado para stdout.                                                     |
| `cmd 2> archivo`          | ❗ **Redirige** el error estándar (stderr) de `cmd` a un archivo. `2` es el descriptor de archivo predeterminado para stderr.                      |
| `cmd >> archivo`          | ➕ **Añade** stdout de `cmd` a un archivo.                                                                                                        |
| `cmd 2>> archivo`         | ➕ **Añade** stderr de `cmd` a un archivo.                                                                                                        |
| `cmd &> archivo`          | 🔄 **Redirige** stdout y stderr de `cmd` a un archivo.                                                                                            |
| `cmd > archivo 2>&1`      | 🔄 **Otra forma** de redirigir tanto stdout como stderr de `cmd` a un archivo. **¡El orden de la redirección importa!**                           |
| `cmd > /dev/null`         | 🗑️ **Descarta** stdout de `cmd`.                                                                                                                 |
| `cmd 2> /dev/null`        | 🗑️ **Descarta** stderr de `cmd`.                                                                                                                 |
| `cmd &> /dev/null`        | 🗑️ **Descarta** stdout y stderr de `cmd`.                                                                                                        |
| `cmd < archivo`           | 🔄 **Redirige** el contenido del archivo a la entrada estándar (stdin) de `cmd`.                                                                 |
| `cmd << FIN`              | 🔄 **Redirige** varias líneas a la entrada estándar (stdin). Si 'FIN' está entre comillas, el texto se trata literalmente. Esto se llama *here-document*. |
| `cmd <<- FIN`             | 🔄 **Redirige** varias líneas a la entrada estándar (stdin) y elimina las tabulaciones iniciales.                                                |
| `cmd <<< "cadena"`        | 🔄 **Redirige** una sola línea de texto a la entrada estándar (stdin) de `cmd`. Esto se llama *here-string*.                                      |
| `exec 2> archivo`         | ❗ **Redirige** stderr de todos los comandos a un archivo permanentemente.                                                                        |
| `exec 3< archivo`         | 📖 **Abre** un archivo para lectura usando un descriptor de archivo personalizado.                                                               |
| `exec 3> archivo`         | ✏️ **Abre** un archivo para escritura usando un descriptor de archivo personalizado.                                                             |
| `exec 3<> archivo`        | 🔄 **Abre** un archivo para lectura y escritura usando un descriptor de archivo personalizado.                                                   |
| `exec 3>&-`               | ❌ **Cierra** un descriptor de archivo.                                                                                                          |
| `exec 4>&3`               | 🔄 **Copia** el descriptor de archivo 3 a 4.                                                                                                     |
| `exec 4>&3-`              | 🔄 **Copia** el descriptor de archivo 3 a 4 y cierra el descriptor de archivo 3.                                                                |
| `echo "foo" >&3`          | ✏️ **Escribe** en un descriptor de archivo personalizado.                                                                                        |
| `cat <&3`                 | 📖 **Lee** desde un descriptor de archivo personalizado.                                                                                         |
| `(cmd1; cmd2) > archivo`  | 🔄 **Redirige** stdout de múltiples comandos a un archivo (usando un sub-shell).                                                                 |
| `{ cmd1; cmd2; } > archivo`| 🔄 **Redirige** stdout de múltiples comandos a un archivo (más rápido; no usa un sub-shell).                                                    |
| `exec 3<> /dev/tcp/host/puerto` | 🌐 **Abre** una conexión TCP a host:puerto. (Esto es una característica de bash, no de Linux).                                              |
| `exec 3<> /dev/udp/host/puerto` | 🌐 **Abre** una conexión UDP a host:puerto. (Esto es una característica de bash, no de Linux).                                              |
| `cmd <(cmd1)`             | 🔄 **Redirige** stdout de `cmd1` a un fifo anónimo, luego pasa el fifo a `cmd` como un argumento.                                                |
| `cmd < <(cmd1)`           | 🔄 **Redirige** stdout de `cmd1` a un fifo anónimo, luego redirige el fifo a stdin de `cmd`. Mejor ejemplo: `diff <(find /path1 \| sort) <(find /path2 \| sort)`.|
| `cmd <(cmd1) <(cmd2)`     | 🔄 **Redirige** stdout de `cmd1` y `cmd2` a dos fifos anónimos, luego pasa ambos fifos como argumentos a `cmd`.                                  |
| `cmd1 >(cmd2)`            | 🚀 **Ejecuta** `cmd2` con su stdin conectado a un fifo anónimo, y pasa el nombre del pipe como un argumento a `cmd1`.                            |
| `cmd1 > >(cmd2)`          | 🚀 **Ejecuta** `cmd2` con su stdin conectado a un fifo anónimo, luego redirige stdout de `cmd` a este pipe anónimo.                              |
| `cmd1 \| cmd2`             | 🔄 **Redirige** stdout de `cmd1` a stdin de `cmd2`. **Tip:** Esto es igual a `cmd1 > >(cmd2)`, igual a `cmd2 < <(cmd1)`, igual a `> >(cmd2) cmd1`, igual a `< <(cmd1) cmd2`.|
| `cmd1 \|& cmd2`            | 🔄 **Redirige** stdout y stderr de `cmd1` a stdin de `cmd2` (solo en bash 4.0+). Usa `cmd1 2>&1 \| cmd2` para versiones más antiguas de bash.   |
| `cmd \| tee archivo`       | 🔄 **Redirige** stdout de `cmd` a un archivo y lo imprime en pantalla.                                                                         |
| `exec {filew}> archivo`   | ✏️ **Abre** un archivo para escritura usando un descriptor de archivo nombrado `{filew}` (solo en bash 4.1+).                                    |
| `cmd 3>&1 1>&2 2>&3`      | 🔄 **Intercambia** stdout y stderr de `cmd`.                                                                                                    |
| `cmd > >(cmd1) 2> >(cmd2)`| 🔄 **Envía** stdout de `cmd` a `cmd1` y stderr de `cmd` a `cmd2`.                                                                                |
| `cmd1 \| cmd2 \| cmd3 \| cmd4 \| echo ${PIPESTATUS[@]}` | 🔄 **Encuentra** los códigos de salida de todos los comandos encadenados.                                      |

---

**Nota:** Para conocer más detalles sobre las redirecciones en bash, puedes consultar el artículo completo [aquí](http://www.catonmat.net/blog/bash-one-liners-explained-part-three/).

---

¡Espero que esta tabla te sea útil y más fácil de entender! 😊

