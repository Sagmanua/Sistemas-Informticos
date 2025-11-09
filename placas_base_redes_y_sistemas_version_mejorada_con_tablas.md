# Placas base, redes y sistemas — Versión mejorada

Este documento reorganiza y mejora el contenido original, añadiendo tablas, secciones claras y bullets para facilitar su lectura y uso docente.

---

## 1. Formatos de placas base

Descripción general de los factores de forma más comunes y sus usos.

| Formato | Dimensiones aproximadas | Ventajas | Uso habitual |
|---|---:|---|---|
| ATX | 305 × 244 mm | Gran número de ranuras y puertos; buena refrigeración | PCs de sobremesa y gaming
| microATX | 244 × 244 mm | Menor tamaño manteniendo muchas prestaciones | PCs compactos y económicos
| FlexATX | 230 × 190 mm | Tamaño reducido, diseñado por Intel (1999) | Mini-ITX intermedio, equipos compactos
| Mini‑ITX | 170 × 170 mm (6.7" × 6.7") | Muy compacto, bajo consumo | Mini PCs, sistemas embebidos e industriales
| NLX / LPX | Varía (slim) | Diseños slim para ahorro de espacio | Equipo de sobremesa slim y barebones

**Nota:** La reducción de tamaño no implica necesariamente pérdida de prestaciones; muchos formatos compactos integran lo necesario para tareas específicas.

---

## 2. Conexiones de la placa base

### 2.1 Conexiones internas
- Alimentación (conectores ATX 24 pines, EPS 8 pines).
- Conectores SATA (almacenamiento moderno) y puertos legacy: EIDE, FDD (en desuso).
- Conectores de ventiladores: CPU_FAN, SYS_FAN.
- Conexiones frontales: Power On, Power LED, HD LED, Reset, Speaker.
- Puentes (jumpers) y switches para configuraciones específicas.

### 2.2 Conexiones externas
- Teclado y ratón: PS/2 (legacy) y USB.
- USB (múltiples versiones), FireWire (menos común hoy).
- Ethernet (RJ‑45), puertos serie y paralelo (obsoletos en la práctica).
- Salidas de audio, conectores para gamepad y salidas de vídeo (HDMI, DisplayPort en placas modernas).
- Interfaces SCSI y docking/backplane en equipos de gama alta/servidores.

---

## 3. Chipset

- **Northbridge:** comunica CPU ↔ RAM y controladores de alta velocidad; históricamente disipador por el calor generado. (Hoy muchas funciones se integran en la CPU).
- **Southbridge:** gestiona E/S, buses y almacenamiento.

**Tendencia:** Integración progresiva del chipset en el propio procesador (SoC), especialmente en miniportátiles y sistemas embebidos.

---

## 4. Mantenimiento y cuidado

### Tareas periódicas
- Limpieza de polvo con aire comprimido; atención a ranuras y conectores.
- Comprobación de conexiones y anclajes (RAM, tarjetas, cables).
- Revisión de ventiladores y sensores de temperatura (monitorización vía BIOS/UTI).

### Buenas prácticas de seguridad
- Apagar y desconectar antes de manipular.
- Evitar electricidad estática (pulsera antiestática, superficies conductoras).
- Evitar humedad y fuentes de calor excesivas.

---

## 5. CPU: ALU y Unidad de Control (UC)

La **CPU** integra la ALU (unidad aritmético‑lógica) —ejecución de operaciones— y la UC —control y secuenciación de instrucciones—. La UC contiene el reloj del sistema que marca la cadencia de las operaciones (MHz/GHz).

---

## 6. Memoria y almacenamiento

- **ROM:** memoria no volátil, almacena firmware/BIOS.
- **RAM:** memoria volátil, acceso rápido para programas en ejecución.
- **Almacenamiento secundario:** HDD, SSD, cinta, CD/DVD —capacidad alta y no volátil, pero más lento que la RAM.

**Interacción:** El bus del sistema gestiona transferencias CPU ↔ memoria; buses locales (cache) aceleran accesos críticos.

---

## 7. Entrada/Salida (E/S)

### Modos de E/S
1. **E/S por programa:** CPU gestiona directamente —ineficiente para I/O intensivo.
2. **E/S por interrupciones:** dispositivo avisa a la CPU para atención puntual —mejora uso de CPU.
3. **DMA (Acceso Directo a Memoria):** controlador transfiere datos memoria↔dispositivo sin intervención constante de la CPU —ideal para grandes volúmenes de datos.

---

## 8. Dispositivos de almacenamiento masivo y controladores

- Dispositivos conectados vía IDE/ATA (legacy), SATA (actual) y SCSI (alto rendimiento, coste superior).
- Unidades externas y grabadoras antiguas también usaban conectores paralelos o USB en modelos más nuevos.

---

## 9. Puertos de comunicación y redes

### Ethernet (par trenzado)
- Conector RJ‑45, velocidades típicas: 100 Mbps, 1 Gbps (Gigabit Ethernet), y superiores en estándares actuales.
- Funciones avanzadas: Wake On LAN (WOL), PXE (arranque por red).

### WLAN (IEEE 802.11)
- Evolución: 802.11b → g → n → ac → ax (Wi‑Fi 6). Wi‑Fi 6 ofrece mayor eficiencia y capacidad (teóricos hasta 9.6 Gbps en escenarios agregados).

---

## 10. Modelo OSI y capas (resumen)

| Capa | Función principal | Ejemplos / Protocolos |
|---|---|---|
| 7. Aplicación | Interfaces de usuario / aplicaciones | HTTP, FTP, SMTP |
| 4. Transporte | Comunicación host a host | TCP, UDP |
| 3. Red | Enrutamiento y fragmentación | IP, OSPF, IPv6 |
| 2. Enlace | Comunicación fiable en un enlace físico | Ethernet, PPP |
| 1. Física | Señales y medios físicos | IEEE 802.3, RS‑232 |

**Conceptos clave:** subnetting, supernetting, VLANs y VPNs para segmentación y seguridad.

---

## 11. Medios de transmisión y conectores

- **Par trenzado (UTP/STP):** Cat5e, Cat6 para Ethernet.
- **Coaxial:** usado históricamente en TV/vídeo y redes antiguas.
- **Fibra óptica:** mayor ancho de banda y menor latencia; costosa.
- **Conectores comunes:** RJ‑45 (Ethernet), BNC (coaxial), RG‑6/RG‑59 (cables coaxiales).

**Estándares de cableado:** T568A / T568B (orden de pares dentro del RJ‑45).

---

## 12. Mapas y documentación de red

- **Mapa físico:** cables, racks, puntos de acceso, longitudes y tipos de cable.
- **Mapa lógico (Capa 3):** direcciones IP, rutas, VLANs, gateways.

**Herramientas recomendadas:**
- Microsoft Visio (diagramas detallados)
- SolarWinds Network Topology Mapper (descubrimiento automático)
- Lucidchart (colaboración en la nube)
- Nmap (escaneo y auditoría de red; técnico y forense)

---

## 13. Seguridad, riesgos y normativa laboral

- Normativas relevantes (ejemplos, España): Ley 31/1995 (Prevención de Riesgos Laborales), RD 486/1997 (condiciones de seguridad en puestos de trabajo). Verificar normativa local aplicable.

### Riesgos comunes
- Caídas (cables mal gestionados, uso incorrecto de escaleras).
- Riesgo eléctrico (aislamiento, humedad).
- Riesgo de incendio (sobrecarga de enchufes).
- Riesgos de ciberseguridad (malware, accesos no autorizados).

### Medidas preventivas
- Orden y gestión de cables, EPI, formación del personal, políticas de seguridad de red (firewalls, ZTNA, monitorización).

---

## 14. Sistemas operativos — clasificación y consideraciones

| Criterio | Tipos / Ejemplos |
|---|---|
| Por disponibilidad | Propietario: Windows, macOS — Código abierto: Linux (varias distribuciones) |
| Por dispositivo | Desktop: Windows, macOS — Server: Windows Server, Linux Server |
| Por gestión de procesos | Monotarea: MS‑DOS — Multitarea: Linux, Windows |

### Requisitos modernos (ejemplo comparativo)

| Característica | Windows 11 (2024‑2025) | Ubuntu 24.04 LTS |
|---|---:|---:|
| CPU | 1 GHz, 2 núcleos, 64‑bit, TPM 2.0 | 2 GHz 64‑bit recomendado |
| RAM | 4 GB mínimo (8 GB recomendado) | 4 GB mínimo (8 GB recomendado) |
| Almacenamiento | 64 GB mínimo (SSD recomendado) | 25–50 GB recomendado |
| Firmware | UEFI con Secure Boot | BIOS o UEFI |

---

## 15. Instalación y recuperación

- **Medios de instalación:** USB, óptico, redes (PXE).
- **Instalación desatendida:** Kickstart, respuestas automatizadas.
- **Gestores y reparación:** GRUB, Boot‑Repair, comandos de recuperación (bootrec, grub‑install).

---

## 16. Virtualización

| Tipo | Uso | Herramientas |
|---|---|---|
| Virtualización de servidores | Consolidación de máquinas | VMware ESXi, Proxmox |
| Virtualización de escritorio | Entornos accesibles desde cualquier lugar | VMware Horizon, Citrix |
| Virtualización a nivel de SO | Contenerización/instancias ligeras | VirtualBox, Docker |

**Herramientas comparadas:** VirtualBox (libre), VMware (propietaria/comercial), QEMU/KVM (Linux).

---

## 17. Licencias y modelos de distribución

- **GPL / MIT:** permiten modificación y redistribución (con matices para la GPL).
- **EULA / OEM:** restricciones de uso y transferibilidad.
- **Freeware / Dominio público:** limitaciones en redistribución o sin restricciones según el caso.

---

## 18. Procedimiento de gestión de incidencias (resumen)

1. Registro de la incidencia (fecha, hora, sistema afectado).
2. Clasificación (prioridad y tipo).
3. Investigación (análisis causa raíz).
4. Resolución (aplicación de la solución y pruebas).
5. Archivo y lecciones aprendidas.

---

## 19. Tablas útiles (resumen)

### Tabla: Comparativa de factores de forma

| Formato | Tamaño | Ranuras expansión | Ideal para |
|---|---:|---:|---|
| ATX | Grande | Varias | Gaming/estaciones de trabajo |
| microATX | Intermedio | 1–3 | PCs económicos |
| Mini‑ITX | Muy pequeño | 0–1 | HTPC, Mini PC |

### Tabla: Puertos comunes

| Puerto | Uso principal | Estado |
|---|---|---|
| USB | Periféricos generales | Actual |
| PS/2 | Teclado/ratón | Legacy (aún presente en some placas) |
| RJ‑45 | Red Ethernet | Actual |
| SATA | Almacenamiento | Actual |

---

## 20. Conclusión y siguientes pasos sugeridos

- El documento reorganiza la información para facilitar su uso en presentaciones o clases.
- Si desea, puedo:
  - Generar una versión en PDF o PPTX.
  - Crear tarjetas de resumen (flashcards) por sección.
  - Ampliar cualquier sección (por ejemplo: virtualización avanzada, seguridad de red, o prácticas de instalación automatizada).

---

*Fin del documento.*

