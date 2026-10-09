> [!NOTE]
> ### Librerías Utilizadas


> ** Capa de Adquisición (Conectores)**
> - `netmiko` — Conexión SSH multi-proveedor para equipos de red.
> - `paramiko` — Cliente SSH de bajo nivel.
> - `pysnmp` — Recolección de datos mediante SNMP.
> - `ncclient` — Cliente NETCONF para datos estructurados XML.
> - `requests` — Consumo de APIs REST / RESTCONF.


> ** Capa de Análisis (Parsers y Validación)**
> - `pydantic` — Definición y validación de esquemas de datos.
> - `deepdiff` — Comparación de estados y detección de diferencias entre ejecuciones.
> - `pandas` — Procesamiento y estructuración de tablas de inventario.
> - `textfsm` — Parsing de salidas de texto CLI a formato JSON.
> - `xmltodict` — Conversión de respuestas XML a diccionarios de Python.




> ** Capa de Reporte**
> - `jinja2` — Plantillas para la generación de reportes HTML/Markdown.
> - `tabulate` — Formateo de tablas de evidencia en consola y texto plano.



> ** Utilidades Generales**
> - `pyyaml` — Lectura y manipulación del archivo de configuración `config.yaml`.
> - `python-dotenv` — Gestión segura de variables de entorno y credenciales.