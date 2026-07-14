


> ! Configuración del protocolo OSPF
router ospf 1
 network 10.0.0.0 0.0.0.3 area 0         ! Red del enlace hacia el router OSPF
 network 192.168.10.0 0.0.0.255 area 0    ! Redes LAN OSPF (si las tiene)
 redistribute eigrp 100 metric 100 subnets ! Redistribuye EIGRP 100 en OSPF
! Configuración del protocolo EIGRP
router eigrp 100
 network 10.0.0.4 0.0.0.3                 ! Red del enlace hacia el router EIGRP
 network 192.168.30.0 0.0.0.255           ! Redes LAN EIGRP (si las tiene)
 no auto-summary
 redistribute ospf 1 metric 1000000 100 255 1 1500 ! Redistribuye OSPF 1 en EIGRP


Lista de comandos a considerar para la configuración

### Averiguar
La siguiente lista de comandos:

> redistribute eigrp 100 metric 100 subnets

> redistribute ospf 1 metric 1000000 100 255 1 1500

De forma resumida se debe saber que significa cada valor 