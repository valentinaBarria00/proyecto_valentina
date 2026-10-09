# Auditoría Programable de Redes con Python

**Wolf-Industries** · Desafío 03 · Proyecto Integrado de Título
Ingeniería en Telecomunicaciones y Servicios Digitales 

---

## Descripción general

Herramienta modular desarrollada en Python para la **recolección automatizada,
normalización y análisis de información** proveniente de equipos de red
heterogéneos. Opera por defecto en **modo de solo lectura**, permitiendo
construir inventario, evidencia, hallazgos y recomendaciones de mejora sin
aplicar cambios sobre la infraestructura productiva.

El diseño sigue una arquitectura de capas desacopladas que permite incorporar
nuevos fabricantes o protocolos mediante **adaptadores**, sin reescribir el
núcleo del sistema.

---

## Objetivo

Diseñar e implementar una aplicación extensible, segura por defecto y
reproducible, capaz de:

- Auditar al menos **cuatro dispositivos o instancias equivalentes**.
- Soportar al menos **dos adaptadores de laboratorio**.
- Normalizar interfaces, VLAN, rutas, vecinos, versión y utilización.
- Comparar ejecuciones o contrastar contra una línea base.
- Generar hallazgos explicables con evidencia exportable.

---

## Arquitectura

El sistema se organiza en capas funcionales independientes:

| Capa | Módulo | Responsabilidad |
|------|--------|-----------------|
| Adquisición | `collectors/` | Conexiones SSH/CLI, SNMP, NETCONF/RESTCONF |
| Adaptación | `parsers/` | Parsing específico por plataforma |
| Normalización | `models/` | Esquema común validado con Pydantic |
| Análisis | `analysis/` | Comparación y motor de reglas |
| Reporte | `reporting/` | Exportación JSON, CSV y Markdown |

### Flujo de trabajo