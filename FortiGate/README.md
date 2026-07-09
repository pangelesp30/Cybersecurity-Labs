# VPN Site-to-Site con FortiGate

## Objetivo

Implementar una VPN IPsec Site-to-Site entre dos sedes utilizando FortiGate, permitiendo únicamente el acceso a servicios web (HTTP y HTTPS) entre ambas redes.

## Topología

![Topología](Topologia.png)

## Tecnologías utilizadas

- FortiGate
- FortiOS CLI
- PnetLab
- VPN IPsec
- Firewall Policies

## Configuración realizada

- Configuración de la VPN IPsec entre ambas sedes.
- Creación de las políticas de firewall necesarias para permitir el tráfico.
- Configuración de las rutas para el envío del tráfico a través del túnel VPN.
- Restricción del acceso únicamente a los servicios HTTP y HTTPS.

## Validación

Se verificó que la comunicación entre las sedes se realizara correctamente mediante acceso web (HTTP y HTTPS).

Las pruebas de **ping (ICMP)** fallaron de forma intencional, ya que este protocolo no fue incluido en las políticas de firewall configuradas para la VPN. Esto demuestra que únicamente se permitió el tráfico definido en las reglas de seguridad, cumpliendo con el principio de mínimo privilegio.

## Resultado

Acceso web (HTTP/HTTPS): Permitido.

Ping (ICMP): Bloqueado por las políticas de firewall.

El laboratorio cumplió con el objetivo de establecer una comunicación segura entre ambas redes, permitiendo únicamente los servicios autorizados a través del túnel VPN.
