# Ansible

Ansible es la herramienta utilizada para poder manejar el estado del portal de corte dentro de los servidores Linux NAT Server

El mismo cuenta con multiples archivos de configuracion de extension yml

## Secciones:
 - Playbooks
   - Initial-Setup-Servers
   - Linux-Wispro-Manage-Cron
   - Login-Radius
   - Test-Ping
 - Roles
 - hosts-1.yml

## Playbooks
### Initial Steup Servers
Prepara cada uno de los hosts para que tengan usuario "wheel", el cual tendra privilegios de sudo, ademas setea y autoriza las keys ssh en cada uno y actualiza los paquetes del linux necesarios

### Linux Wispro Manage Cron
Posee dos playbooks, uno encargado de activar y otro de desactivar el portal de corte en cada servidor. Esto consta de comentar o descomentar el cron necesario para ejecutar la tarea de escritura de datos. Ademas de limpiar el ipset o ejecutar el script necesario para llenar el ipset

### Login Radius
Setea los comandos necesarios para poder realizar el login a traves de radius

### Test Ping
Realiza un ping a cada uno de los servidores para verificar disponibilidad


## Roles
Consta de dos directorios encargados de agregar los nas al radius para poder ser administrados, junto con varios chequeos para garantizar el funcionamiento. Asi como tambien establece los usuarios que seran necesarios que existan para poder ser logueados

## hosts-1.yml
Listado de servidores asociados al portal de cortes, es un archivo que debe ser administrado constantemente para que refleje la realidad
