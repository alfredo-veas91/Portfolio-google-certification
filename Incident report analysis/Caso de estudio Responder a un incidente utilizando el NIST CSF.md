
Usted es un analista de ciberseguridad que trabaja para una empresa multimedia que ofrece servicios de diseño web, diseño gráfico y soluciones de marketing en redes sociales a pequeñas empresas. Su organización ha sufrido recientemente un ataque DoS, que comprometió la red interna durante dos horas hasta que se resolvió.

Durante el ataque, los servicios de red de su organización dejaron de responder repentinamente debido a una avalancha de paquetes ICMP entrantes. El tráfico normal de la red interna no pudo acceder a ningún recurso de la red. El equipo de gestión de incidentes respondió bloqueando los paquetes ICMP entrantes, deteniendo todos los servicios de red no críticos fuera de línea y restableciendo los servicios de red críticos.

A continuación, el equipo de ciberseguridad de la empresa investigó el incidente de seguridad. Descubrieron que un actor malicioso había enviado una avalancha de pings ICMP a la red de la empresa a través de un cortafuegos no configurado. Esta vulnerabilidad permitió al atacante malicioso saturar la red de la empresa mediante un ataque de denegación de servicio (DoS).

Para solucionar este problema de seguridad, el equipo de seguridad de la red implementó:

- Una nueva regla de cortafuegos para limitar la tasa de paquetes ICMP entrantes
    
- Verificación de la dirección IP de origen en el cortafuegos para comprobar si hay direcciones IP falsificadas en los paquetes ICMP entrantes
    
- Software de supervisión de red para detectar patrones de tráfico anómalos
    
- Un sistema IDS/IPS para filtrar parte del tráfico ICMP basado en características sospechosas


Como analista de ciberseguridad, tiene la tarea de utilizar este evento de seguridad para crear un plan para mejorar la seguridad de la red de su empresa, siguiendo el Marco de Ciberseguridad (CSF) del Instituto Nacional de Estándares y Tecnología (NIST). Utilizarás el CSF para ayudarte a navegar por los diferentes pasos del análisis de este evento de ciberseguridad e integrar tu análisis en una estrategia de seguridad general.