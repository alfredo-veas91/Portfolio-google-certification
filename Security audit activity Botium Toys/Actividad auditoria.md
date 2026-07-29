
# Caso de estudio 

[[Caso de estudio Botium toys - Case study Botium toys]]


# Botium Toys report

[[Botium Toys_ Scope, goals, and risk assessment report]]

# Controls and compliance checklist

  
# Botium Toys: Controls and Compliance Checklist Audit

Este documento contiene la auditoría interna de controles y cumplimiento normativo realizada para **Botium Toys**, basada en la evaluación de riesgos e infraestructura actual de la organización.

---

## 1. Checklist de Evaluación de Controles (Controls Assessment Checklist)

¿Cuenta Botium Toys actualmente con este control implementado?

| Control | Implementado (YES) | No Implementado (NO) | Descripción / Estado Actual |
| :--- | :---: | :---: | :--- |
| **Least Privilege** | | **[X]** | No existen controles de acceso basados en mínimo privilegio; todos los empleados acceden a datos internos. |
| **Disaster recovery plans** | | **[X]** | No existen planes de recuperación ante desastres en caso de incidentes críticos. |
| **Password policies** | **[X]** | | Existe una política de contraseñas, aunque sus requisitos son mínimos e insuficientes. |
| **Separation of duties** | | **[X]** | No se ha implementado la separación de funciones en los accesos a datos sensibles. |
| **Firewall** | **[X]** | | Cuentan con un firewall con reglas de seguridad adecuadamente definidas. |
| **Intrusion detection system (IDS)** | | **[X]** | El departamento de TI no ha instalado un sistema de detección de intrusiones. |
| **Backups** | | **[X]** | La empresa no realiza copias de seguridad de sus datos críticos. |
| **Antivirus software** | **[X]** | | Antivirus instalado y monitoreado regularmente por el equipo de TI. |
| **Manual monitoring (Legacy systems)** | **[X]** | | Se realiza monitoreo y mantenimiento manual de los sistemas heredados (legacy). |
| **Encryption** | | **[X]** | No se utiliza cifrado para proteger la información de tarjetas ni datos de clientes. |
| **Password management system** | | **[X]** | No existe un sistema centralizado para la gestión y restablecimiento de contraseñas. |
| **Locks (Offices, Storefront, Warehouse)** | **[X]** | | Las instalaciones físicas cuentan con cerraduras suficientes y funcionales. |
| **CCTV surveillance** | **[X]** | | Sistema de videovigilancia por circuito cerrado actualizado y operativo. |
| **Fire detection/prevention** | **[X]** | | Sistemas de detección y prevención de incendios operativos (alarmas, rociadores). |

---

## 2. Checklist de Cumplimiento Normativo (Compliance Checklist)

### Payment Card Industry Data Security Standard (PCI DSS)

| Buenas Prácticas | Cumple (YES) | No Cumple (NO) | Estado Actual |
| :--- | :---: | :---: | :--- |
| **Only authorized users have access to credit card info** | | **[X]** | Todos los empleados tienen acceso potencial a datos de tarjetahabientes. |
| **Credit card info stored/processed in a secure environment** | | **[X]** | La información se almacena localmente sin las salvaguardas requeridas. |
| **Implement data encryption procedures** | | **[X]** | No existe cifrado en la transmisión ni almacenamiento de datos financieros. |
| **Adopt secure password management policies** | | **[X]** | La política de contraseñas es débil y no hay gestión centralizada. |

### General Data Protection Regulation (GDPR)

| Buenas Prácticas | Cumple (YES) | No Cumple (NO) | Estado Actual |
| :--- | :---: | :---: | :--- |
| **E.U. customers' data is kept private/secured** | | **[X]** | Faltan controles de acceso y cifrado para proteger la PII/SPII. |
| **72-hour breach notification plan in place** | **[X]** | | Existe un plan establecido para notificar incidentes a clientes de la UE en 72h. |
| **Ensure data is properly classified and inventoried** | **[X]** | | Se ha determinado la necesidad de clasificar los activos e inventariarlos. |
| **Enforce privacy policies, procedures, and processes** | **[X]** | | Existen políticas de privacidad desarrolladas y aplicadas en el departamento de TI. |

### System and Organizations Controls (SOC 1 / SOC 2)

| Buenas Prácticas | Cumple (YES) | No Cumple (NO) | Estado Actual |
| :--- | :---: | :---: | :--- |
| **User access policies are established** | | **[X]** | No hay políticas de acceso de usuarios basadas en el principio de menor privilegio. |
| **Sensitive data (PII/SPII) is confidential/private** | | **[X]** | Los datos sensibles están expuestos a acceso no autorizado por falta de cifrado. |
| **Data integrity ensures consistency and accuracy** | **[X]** | | El departamento de TI ha integrado controles para asegurar la integridad de datos. |
| **Data is available to authorized individuals** | **[X]** | | El equipo de TI ha garantizado la disponibilidad de los datos. |

---

> [!NOTE] Spanish version 


## 3. Resumen de Recomendaciones

### 🚨 Recomendaciones Críticas (Prioridad Alta - Riesgo Operativo y de Multas Legal)
1. **Cifrado de Datos Transmitidos y Almacenados (PCI DSS / GDPR / SOC2):** Implementar mecanismos de cifrado para la información de tarjetas de crédito de clientes y datos personales sensibles (PII/SPII) tanto en tránsito como en reposo.
2. **Control de Acceso (Mínimo Privilegio y Separación de Funciones):** Configurar políticas de acceso restrictivas de modo que los empleados solo accedan a los datos estrictamente necesarios para sus funciones.
3. **Plan de Recuperación ante Desastres (DRP) y Copias de Seguridad:** Implementar un sistema automatizado de respaldos (backups) periódicos de datos críticos y formalizar un plan de recuperación ante desastres.
4. **Gestión Centralizada y Política Estricta de Contraseñas:** Adoptar un gestor de contraseñas institucional y aumentar los requisitos mínimos de complejidad para reducir el riesgo de vulneración de cuentas.

### ⚠️ Recomendaciones Importantes (Prioridad Media - Fortalecimiento Defensivo)
1. **Sistema de Detección de Intrusiones (IDS):** Desplegar un IDS para monitorear el tráfico de la red interna y detectar actividades sospechosas que sobrepasen la barrera del firewall.
2. **Calendarización del Mantenimiento de Sistemas Heredados (Legacy):** Establecer un cronograma formal para el monitoreo, aplicación de parches y procedimientos de intervención en los sistemas *legacy*.


---


> [!NOTE] ENGLISH VERSION
## 3. Summary of Recommendations

### 🚨 Critical Recommendations (High Priority - Operational Risk & Legal Fines)
1. **Encryption of Transmitted and Stored Data (PCI DSS / GDPR / SOC2):** Implement encryption mechanisms for customer credit card information and sensitive personal data (PII/SPII) both in transit and at rest.
2. **Access Control (Least Privilege and Separation of Duties):** Configure restrictive access policies so that employees only access the data strictly necessary for their job functions.
3. **Disaster Recovery Plan (DRP) and Backups:** Implement an automated system for periodic backups of critical data and formalize a disaster recovery plan.
4. **Centralized Password Management and Strict Password Policy:** Adopt an institutional password manager and increase minimum complexity requirements to reduce the risk of account compromise.

### ⚠️ Important Recommendations (Medium Priority - Defensive Strengthening)
1. **Intrusion Detection System (IDS):** Deploy an IDS to monitor internal network traffic and detect suspicious activity that bypasses the firewall.
2. **Scheduled Maintenance for Legacy Systems:** Establish a formal schedule for monitoring, patching, and intervention procedures on legacy systems.

[^1]: English version 
