# VPN Site-to-Site Lab con WireGuard

**Autor:** Mauricio Teliz Duche  

## Descripción
Este laboratorio documenta la configuración de una **VPN Site-to-Site** utilizando **WireGuard** para conectar una máquina local Ubuntu con una instancia remota en AWS.  
Se incluyen generación de claves, configuración de interfaces, AllowedIPs, rutas, verificación de conectividad y pruebas de ping.  

## Objetivo
- Conectar de forma segura dos redes mediante un túnel VPN cifrado.  
- Configurar WireGuard en ambos extremos (local y AWS).  
- Practicar generación de claves públicas/privadas y configuración de AllowedIPs.  
- Verificar conectividad y flujo de tráfico cifrado entre extremos.  

## Detalles de la configuración
- Configuración de la interfaz `wg0.conf` en ambos extremos.  
- Explicación de cada parámetro: `PrivateKey`, `Address`, `ListenPort`, `PublicKey`, `AllowedIPs`, `Endpoint`, `PersistentKeepalive`.  
- Verificación del estado de la VPN con `wg show`.  
- Pruebas de conectividad con `ping` entre las IPs internas del túnel.  
- Seguridad: uso de UDP `51820`, configuración de firewall y security groups en AWS.

## Conclusión
El túnel VPN Site-to-Site funciona correctamente, garantizando tráfico cifrado entre la máquina local y la instancia AWS, con conectividad bidireccional confirmada mediante pruebas de ping.