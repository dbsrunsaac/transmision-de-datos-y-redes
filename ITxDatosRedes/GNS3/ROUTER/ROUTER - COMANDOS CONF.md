## Lista de comandos

### enable
	en
Permite acceder al modo administrador del router

### configure terminal
	conf t
Acceder al modo configuración

### interface fastethernet0/0:
	int f0/0
Permite seleccionar una interfaz (puerto) para su configuración.
### ip address: 
Establece una dirección ip a un puerto seleccionado, según el formato:
dirección ip Máscara
Ejemplo:
ip address 192.168.1.1 255.255.255.0

### no shutdown
Habilita/enciende el puerto configurado permitiendo la conectividad o uso del mismo para la interconexión de diferentes redes.
### show ip interface brief
Mostrar en pantalla el estado actual de los puertos mediante una lista (muestra la ip, máscara y si el puerto se encuentra activo o no).

### copy running-config startup-config
Permite copiar la configuración que se esta ejecutando (almacenada en la memoria RAM) en la configuración inicial almacenada memoria NVRAM del router (no volátil), permitiendo guardar las configuraciones realizadas para no perderlas en caso del reinicio o apagado del router.
### wr
Guardar la configuración
### end
Permite regresar al punto de inicio (modo administrador #)
### exit
Permite salir de la interfaz de configuración actual a la previa

### show ip route
La re

### do show ip route
Ejecuta el comando **show ip route** sin la necesidad de ubicarse en la raíz de la configuración (#)

### show ip protocol
Muestra los protocolos ip configurados en el router

## Ejemplo 

R1: network 198.155.10.0
R2: network 198.155.10.0
R2: network 172.16.1.0
R2: network 172.16.2.0
R2: network 172.16.3.0
