from pathlib import Path
import pypandoc

# Ruta de salida del resumen en formato Markdown
output_md = "/mnt/data/Resumen_Sistemas_y_Instalacion.md"

# Resumen general de ambos documentos
resumen = """
# 📘 Resumen de los Temas de DAM
## Unidad 1: Explotación de sistemas microinformáticos

### Introducción
Esta unidad trata sobre los **componentes del hardware** y su gestión. Se estudian las placas base, CPU, memoria, dispositivos de entrada/salida y periféricos. También aborda las **redes informáticas**, sus tipos (LAN, WLAN, PAN), componentes (nodos, protocolos, modelo OSI), y el **mantenimiento del sistema** junto con las **normas de seguridad laboral e informática** (ISO 27001).

### Contenidos principales
- **Placas base**: formatos (ATX, Mini ITX), conectores internos y externos, chipset, instalación y mantenimiento.  
- **Componentes del sistema**: CPU (ALU y Unidad de Control), memoria RAM/ROM y secundaria, buses de datos, entrada/salida y periféricos.  
- **Redes informáticas**: topologías, cableado, mapa físico y lógico, protocolos IP y subnetting.  
- **Seguridad y prevención**: medidas de seguridad, riesgos laborales, ciberseguridad, y normas ISO.

### Objetivos
- Identificar componentes físicos y lógicos de un sistema informático.  
- Conocer tipos de memoria y periféricos.  
- Comprender las redes de comunicación y sus elementos.  
- Aplicar normas de seguridad informática y laboral.

---

## Unidad 2: Instalación de sistemas operativos

### Introducción
Explica el proceso de **instalación, actualización y mantenimiento** de sistemas operativos, tanto libres como propietarios. Se estudian los tipos de sistemas, su evolución, licencias, virtualización y documentación técnica.

### Contenidos principales
- **Historia y clasificación**: desde MS-DOS hasta Windows 11 y Linux; tipos de SO (escritorio, servidor, red, tiempo real, embebidos).  
- **Funciones del sistema operativo**: gestión de procesos, memoria y recursos.  
- **Tipos de aplicaciones**: de sistema y de usuario.  
- **Licencias de software**: libre (GPL, Apache) y propietario (Windows, macOS).  
- **Instalación**: requisitos previos, gestores de arranque, instalación física o virtual, mantenimiento, recuperación y documentación.  
- **Virtualización**: uso de herramientas como VirtualBox, VMware o Hyper-V.  
- **Documentación**: registro de incidencias y mantenimiento del sistema.

### Objetivos
- Comparar y seleccionar sistemas operativos según necesidades y licencias.  
- Instalar y actualizar sistemas operativos en entornos físicos o virtuales.  
- Documentar procesos de instalación y mantenimiento.  
- Usar herramientas de virtualización para pruebas y aprendizaje.

---

## 🧠 Conclusión
Ambas unidades sientan las bases del **mantenimiento y explotación de sistemas informáticos**, desde el conocimiento del hardware y redes hasta la correcta instalación y gestión de sistemas operativos. Forman el fundamento para desarrollar y mantener entornos de software multiplataforma de forma segura y eficiente.
"""

# Convertir el texto a Markdown y guardar
pypandoc.convert_text(resumen, "md", format="md", outputfile=output_md, extra_args=['--standalone'])

output_md
