# 🛡️ Arquitectura de Seguridad para la Infraestructura de Computación en la Nube del Grupo GRID

## 📖 Descripción

Este proyecto corresponde a una tesis de pregrado cuyo propósito es especificar una arquitectura de seguridad para la infraestructura de computación en la nube del Grupo de Investigación en Redes, Información y Distribución (GRID) de la Universidad del Quindío.

La propuesta busca fortalecer la protección de la infraestructura tecnológica del GRID mediante la implementación de una arquitectura basada en el modelo de Defensa en Profundidad (*Defense in Depth*), integrando herramientas de código abierto orientadas al monitoreo continuo, inspección de tráfico, correlación de eventos y respuesta activa frente a amenazas de ciberseguridad.

La arquitectura implementada incorpora tecnologías como OPNsense, Suricata y Wazuh, permitiendo centralizar eventos de seguridad, detectar actividades maliciosas y automatizar mecanismos de mitigación dentro de un laboratorio virtualizado que simula entornos reales de computación en la nube.

---

## 🎯 Objetivos

### Objetivo general

Especificar una arquitectura de seguridad para la infraestructura de computación en la nube del grupo de investigación GRID de la Universidad del Quindío.

### Objetivos específicos

- Determinar necesidades, problemas y oportunidades (NPO) relacionadas con la seguridad de la infraestructura de computación en la nube del GRID.
- Identificar, analizar y caracterizar arquitecturas, controles y tecnologías de seguridad mediante un Estudio de Mapeo Sistemático (SMS).
- Seleccionar tecnologías de seguridad apropiadas mediante un proceso de análisis y resolución de decisiones (DAR).
- Diseñar una arquitectura de seguridad basada en defensa en profundidad para la infraestructura del GRID.
- Implementar un prototipo funcional de la arquitectura de seguridad propuesta.
- Validar técnicamente la arquitectura implementada conforme a estándares y buenas prácticas internacionales de seguridad.

---

## 📚 Marco Conceptual

### Computación en la Nube

Modelo tecnológico que permite el acceso bajo demanda a recursos computacionales configurables como redes, servidores, almacenamiento y servicios mediante conectividad remota y esquemas de virtualización.

### Defensa en Profundidad (DiD)

Estrategia de ciberseguridad basada en la implementación de múltiples capas de protección distribuidas en diferentes niveles de la infraestructura para reducir el impacto de amenazas y ataques.

### SIEM (Security Information and Event Management)

Tecnología encargada de centralizar registros, correlacionar eventos de seguridad, generar alertas y facilitar procesos de monitoreo continuo y respuesta ante incidentes.

### IDPS (Intrusion Detection and Prevention System)

Sistema especializado en detectar y prevenir actividades maliciosas mediante inspección profunda del tráfico de red, análisis de firmas y comportamiento.

### Firewall de Nueva Generación (NGFW)

Dispositivo o software de seguridad encargado de controlar el tráfico de red mediante políticas de filtrado, segmentación y monitoreo avanzado.

---

## 🧪 Metodología

La metodología se desarrolló en fases sucesivas bajo un enfoque sistemático:

1. **Caracterización del contexto:** análisis de necesidades, problemas y oportunidades (NPO) del GRID.
2. **Estudio de Mapeo Sistemático (SMS):** identificación y clasificación de estudios relacionados con arquitecturas de seguridad en la nube.
3. **Análisis DAR:** evaluación y selección de tecnologías de seguridad según criterios técnicos y funcionales.
4. **Diseño arquitectónico:** especificación de la arquitectura de defensa en profundidad.
5. **Implementación del prototipo:** despliegue funcional del laboratorio virtual y las herramientas seleccionadas.
6. **Validación técnica:** verificación de capacidades de monitoreo, correlación de eventos y respuesta activa.

---

## ⚙️ Tecnologías Implementadas

Las herramientas seleccionadas e implementadas dentro de la arquitectura fueron:

- **OPNsense:** firewall perimetral y sistema de enrutamiento seguro.
- **Suricata:** sistema IDPS para inspección profunda de tráfico.
- **Wazuh:** plataforma SIEM para monitoreo continuo y correlación de eventos.
- **VMware Workstation:** plataforma de virtualización del laboratorio.
- **Debian Linux:** sistema operativo utilizado para servicios y monitoreo.

---

## 🏗️ Infraestructura del Laboratorio Virtual

### Segmentación de Red

La infraestructura virtual fue dividida en múltiples segmentos:

- **WAN:** acceso externo a Internet.
- **LAN:** red administrativa y de gestión.
- **SERVERS:** segmento de servicios y máquinas objetivo.
- **Mirror Port:** segmento destinado al *port mirroring* para Suricata.

### Direccionamiento

- **LAN:** 172.16.0.0/28
- **SERVERS:** 10.0.0.0/28

### Componentes Principales

- Firewall OPNsense configurado como perímetro principal.
- Suricata operando en modo promiscuo mediante *port mirroring*.
- Wazuh centralizando registros y eventos de seguridad.
- Máquinas objetivo monitorizadas mediante agentes Wazuh.

---

## 🚀 Impacto Esperado

### Para el Grupo GRID

- Fortalecimiento de la postura de seguridad institucional.
- Consolidación de capacidades de monitoreo continuo.
- Implementación de mecanismos automatizados de respuesta activa.
- Mejora en la visibilidad y trazabilidad de eventos de seguridad.

### Para la Comunidad Académica

- Escenario práctico para formación en ciberseguridad.
- Plataforma de experimentación en arquitecturas seguras en la nube.
- Apoyo a proyectos académicos relacionados con seguridad informática y computación distribuida.
- Fortalecimiento de capacidades investigativas en ciberseguridad.

### Capacidades Técnicas Alcanzadas

- Correlación centralizada de eventos de seguridad.
- Detección de amenazas mediante firmas y análisis heurístico.
- Bloqueo automático de IPs maliciosas.
- Monitoreo continuo bajo lineamientos NIST SP 800-53.
- Segmentación segura de tráfico y control de acceso.

---

## 📊 Beneficios de la Arquitectura Implementada

- **Centralización:** unificación de registros y eventos de seguridad.
- **Visibilidad:** monitoreo integral de tráfico y actividades sospechosas.
- **Automatización:** respuesta activa frente a incidentes detectados.
- **Escalabilidad:** arquitectura preparada para integrar nuevos servicios y controles.
- **Cumplimiento:** alineación con ISO/IEC 27001:2022 e ISO/IEC 27017:2015.
- **Disponibilidad:** infraestructura virtualizada accesible para pruebas y validación continua.
- **Auditoría:** facilita procesos de análisis forense y seguimiento de incidentes.