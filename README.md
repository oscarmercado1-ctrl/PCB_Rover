# Diseño de PCB basada en FPGA para Robot Móvil Autónomo

## Descripción

Este proyecto corresponde al diseño electrónico de una plataforma robótica móvil desarrollada como parte del curso **Diseño de Productos Electrónicos** de la **Universidad de Antioquia**.

El objetivo fue diseñar una PCB multicapa basada en una FPGA **Digilent CMOD A7 (Artix-7)** capaz de integrar sensores, actuadores, comunicaciones inalámbricas y sistemas de navegación en una arquitectura modular y escalable.

El desarrollo incluye el diseño completo del esquemático, captura jerárquica, reglas de diseño (DRC), generación del PCB de cuatro capas, análisis de costos y documentación técnica del proyecto.

---

# Características principales

- Diseño de PCB de **4 capas**.
- Arquitectura basada en FPGA **Xilinx Artix-7**.
- Comunicación inalámbrica mediante **LoRa SX1276**.
- Sistema de posicionamiento **GNSS (u-blox NEO-M9N)**.
- Sensores ambientales, inerciales y de presión.
- Comunicación mediante:
  - SPI
  - I²C
  - UART
- Control de:
  - Motores DC
  - Servomotores
  - Motor paso a paso
- Interfaz para pantalla LCD.
- Sistema de alimentación unificado a **3.3 V**.

---

# Arquitectura del sistema

La FPGA actúa como unidad central de procesamiento, implementando de forma concurrente:

- Comunicación LoRa
- Comunicación GNSS
- Lectura de sensores
- Control de motores
- Generación de señales PWM
- Procesamiento de encoders
- Gestión de la interfaz de usuario

Todo el sistema fue diseñado utilizando una arquitectura modular mediante hojas jerárquicas en Altium Designer.

---

# Componentes principales

| Componente | Función |
|------------|---------|
| Digilent CMOD A7 (Artix-7) | Unidad de procesamiento |
| SX1276 | Comunicación LoRa |
| u-blox NEO-M9N | Posicionamiento GNSS |
| MPU-6050 | IMU |
| Magnetómetro | Orientación |
| ADS1115 | Conversor ADC |
| Sensores de presión Honeywell MPRLS | Medición de presión |
| Encoders ópticos TCST2103 | Velocidad de motores |
| Drivers A4988 | Motor paso a paso |
| Driver L298N | Motores DC |

---

# Diseño de la PCB

El PCB fue desarrollado considerando criterios profesionales de diseño electrónico:

- PCB de cuatro capas
- Plano de tierra continuo
- Plano de alimentación dedicado
- Separación entre dominios:
  - Radiofrecuencia
  - Potencia
  - Lógica digital
- Capacitores de desacople próximos a cada circuito integrado
- Impedancia controlada para líneas RF
- Reglas de diseño compatibles con fabricantes comerciales

---

# Herramientas utilizadas

- Altium Designer
- Altium 365
- GitHub
- LaTeX
- Microsoft Excel

---

# Archivos incluidos

- Proyecto completo de Altium Designer.
- Librerías personalizadas.
- Esquemáticos jerárquicos.
- Diseño del PCB.
- Bill of Materials (BOM).
- Archivos Gerber.
- Informe técnico.
- Documentación del proyecto.

---

# Objetivos del diseño

- Integrar múltiples sensores sobre una única plataforma.
- Implementar procesamiento concurrente mediante FPGA.
- Garantizar comunicaciones inalámbricas de largo alcance.
- Facilitar futuras expansiones del sistema.
- Cumplir criterios profesionales de manufactura de PCB.

---

# Fabricación

La PCB fue diseñada para fabricación en proveedores comerciales como:

- JLCPCB
- PCBWay
- OSH Park

Características:

- 4 capas
- Espesor: 1.6 mm
- Cobre: 1 oz
- Acabado HASL libre de plomo
- Vías mínimas: 0.20 mm
- Separación mínima: 0.15 mm

---

# Autores

**Oscar David Mercado Gómez**

**Carlos Daniel Galvis Ramirez**

Ingeniería Electrónica  
Universidad de Antioquia

---

# Licencia

Este proyecto fue desarrollado con fines académicos como parte del curso **Diseño de Productos Electrónicos** de la Universidad de Antioquia.
