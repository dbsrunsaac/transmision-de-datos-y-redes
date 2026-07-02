# Lista de comandos en el router para habilitar el DHCP

DHCP es un protocolo que permite automatizar la asignación de dirección IP, considerando la dirección IP, máscara y puerta de enlace

## Configuración
conf t
int f0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit

> En la sección (config) en la terminal del router, se asigna

### ip dhcp excluded-address 192.168.1.1
Esta permite excluir la dirección IP del router para que otro dispositivo no la tome, evitando cortes en la conexión
### ip dhcp pool BRED1
Establece un nombre para la configuración y permite acceder al modo de configuración **dhcp-config**

### network 192.168.1.0 255.255.255.0
Se establece la red con la cual se realizará la asignación automática, para este caso el 192.168.1.0 255.255.255.0 (en conjunto a su máscara)

### default-router 192.168.1.1
Establece la dirección IP por defecto para el router (esta es la misma dirección que se asigno a la interfaz) y también se considera como el equivalente a la puerta de enlace

### dns-server 8.8.8.8 8.8.4.4

Asigna una dns principal (8.8.8.8) y una secundaria 8.8.4.4 en la red y evita la navegación con valores números de ip en nombres de dominio facilitando la navegación en internet.

### end
Permite regresar a la nivel de configuración principal (#)

## configuración en la PC - GNS3
Para indicar a la PC que debe asignar una dirección IP de forma dinámica, se usa:
### ip dhcp
Habilita la configuración DHCP automática en la computadora


*Si no hubo problemas en la configuración cada pc configurada se le debe asignar una IP automaticamente para realizar la conexión a internet o al router*

