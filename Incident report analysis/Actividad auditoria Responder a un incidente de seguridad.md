[[Caso de estudio Responder a un incidente utilizando el NIST CSF]]


|   |   |   |   |
|---|---|---|---|
|Summary|Este día, la página de la organización sufrió un ataque DoS con paquetes ICMP dejando la red bloqueada ante la cantidad de peticiones hechas. El equipo de seguridad respondió bloqueando todos los paquetes entrantes dejando funcionando solo los servicios críticos. Los servicios estuvieron paralizados durante 2 horas hasta poder restaurar los servicios normalmente. El equipo de seguridad detectó deficiencias en la configuración del firewall permitiendo al atacante inundar con paquetes ICMP|   |   |
|Identify|En la investigación el equipo de seguridad ha detectado una mala configuración en las reglas del firewall, no controlando el volumen de paquetes ICMP.|   |   |
|Protect|Como medidas, el equipo de seguridad ha implementado como inmediatas nuevas reglas para el firewall que limiten el volumen de paquetes ICMP entrantes, además de la verificación de Ip de origen que comprueben Ip falsificadas. También se implementaran software de prevención de red para detectar patrones sospechosos así como sistemas IDS/IPS para filtrar el tráfico de paquetes ICMP|   |   |
|Detect|Como parte de la configuración del firewall, el equipo implementó como regla la verificación de Ip de origen de cualquier paquete ICMP entrante|   |   |
|Respond|Durante la crisis, el equipo de seguridad ejecutó el plan de acción bloqueando los paquetes ICMP entrantes, deteniendo todos los servicios de red no críticos y solo dejando funcionando los servicios críticos conteniendo la amenaza. A futuro, se implementaron medidas de aislamiento a sistemas afectados para impedir que toda la red caiga|   |   |
|Recover|Como parte del plan de acción, el equipo dejó primero funcionando solo los servicios críticos de la organización, eliminado todos los paquetes ICMP que aun quedaran en los registros en aquellos servicios no esenciales antes de poder volver a levantar todos los servicios.|   |   |

  
|                                                                                                                                                                                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Reflections/Notes: El equipo se dio cuenta de la vulnerabilidad de tener un firewall mal configurado permitiendo a un atacante realizar un ataque DoS, el equipo pudo responder bien a la amenaza y tomo las decisiones adecuadas para parchear esa vulnerabilidad. |



