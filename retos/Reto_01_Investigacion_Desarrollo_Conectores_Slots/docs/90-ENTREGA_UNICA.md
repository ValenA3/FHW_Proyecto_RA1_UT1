# ENTREGA ÚNICA - Reto 01

> Exporta este archivo como **PDF único** con nombre:  
> `apellido1_apellido2_nombre_FHW01_Tarea`  *(sin ñ ni tildes)*

## Índice

- [Portada](#portada)
- [1. Introducción](#1-introduccion)
- [2. Conectores internos (energía)](#2-conectores-internos-energia)
- [3. Conectores de datos](#3-conectores-de-datos)
- [4. Slots de expansión](#4-slots-de-expansion)
- [5. Conectores externos](#5-conectores-externos)
- [6. Bibliografía](#6-bibliografia)

<a id="portada"></a>
## Portada
![Portada](../assets/img/00-portada/portadaa.jpg "Portada")
Los conectores, ranuras y puertos de una placa base constituyen el sistema de interconexión que permite el funcionamiento coordinado del hardware. A través de ellos se distribuye energía, se transfieren datos y se amplían las capacidades del equipo mediante componentes y periféricos adicionales. Su diseño estandarizado asegura la compatibilidad entre generaciones y la correcta comunicación entre los distintos dispositivos, tanto internos como externos.

En conjunto, estas interfaces combinan líneas de energía, carriles de datos y buses de alta velocidad que evolucionan con cada generación para ofrecer mayor eficiencia, menor consumo y más ancho de banda. Su identificación física mediante formas, llaves, colores y símbolos facilita el montaje y evita errores de conexión. La tendencia actual se orienta hacia la integración de múltiples funciones en menos tipos de conectores, priorizando la velocidad, la versatilidad y la compatibilidad universal.

<a id="1-introduccion"></a>
## 1. Introducción
Este proyecto recopila y organiza información técnica sobre los distintos conectores, ranuras y puertos presentes en las placas base actuales. Su objetivo es ofrecer una referencia clara y estructurada que facilite la identificación, comprensión y comparación de las principales interfaces utilizadas en la conexión de componentes, dispositivos de almacenamiento, expansión y periféricos.

<a id="2-conectores-internos-energia"></a>
## 2. Conectores internos (energía)
# Cable 12VHPWR

**Descripción breve:** Conector de alimentación de 16 pines para tarjetas gráficas de alta potencia<br>
**Pines/Carriles/Voltajes/Velocidad:** 16pines(12 de potencia, 4 de deteccion), hasta 600 W, no velocidad <br>
**Uso principal:** Suministrar potencia a las tarjetas gráficas de gama alta más modernas.<br>
**Compatibilidad actual:** Alta con GPUs modernas

## Identificación física

- 16pines(12 de potencia, 4 de señal), pines de potencia organizados en dos filas paralelas (6 + 6) y detras los pines de señal.<br>
Algunos pines tienen bordes cortados o esquinas biseladas para que no puedan insertarse al revés o mal orientados.<br>
Pueden ser negros o blancos. Pueden venir con texto “PCIe 5.0” o “12VHPWR” impreso o grabado, para identificar que es para GPU / potencia alta.<br>
Se encuentra en el lado superior o lateral, cerca de las salidas de energía de la tarjeta.
## Notas técnicas

- Verisones: 12VHPWR (H+), 12V-2x6 (H++). <br>
Limitaciones: Cada pin de potencia soporta hasta ~9.2 A, distribuidos entre los 12 pines principales.<br>
Calibre mínimo de AWG 16 (recomendado AWG 14 para GPUs >450 W) y longitud máxima de ≤ 750 mm<br>
Compatibilidad: solo con GPUs y PSUs con estándar PCIe 5.0 / ATX 3.0 o adaptadores oficiales.

# Conector: ATX de 24 pines

**Descripción breve:** Conector principal que alimenta la placa base en sistemas ATX/ATX12V.  
**Pines/Carriles/Voltajes/Velocidad:** 24 pines · +3.3V, +5V, +12V  
**Uso principal:** Alimentación de la placa base  
**Compatibilidad actual:** Alta

## Identificación física
- Bloque rectangular de 24 pines con clip, situado en el borde de la placa base.

## Notas técnicas
- Estándar ATX12V 2.x. No confundir con el EPS de CPU (4/8 pines).

# Conector EPS de 8 pines (4+4)

**Descripción breve:** Cable de alimentación para la CPU. Compuesto por dos conectores de 4 pines que se pueden unir para formar uno de 8.<br>
**Pines/Carriles/Voltajes/Velocidad:** 8 pines, 12V, 336W, no tiene velocidad (no trasmite datos)<br>
**Uso principal:** Alimentación de la CPU.<br>
**Compatibilidad actual:** Alta

## Identificación física

- Situdo en la fuente de alimentación y se conecta directamente a un puerto de 8 pines en la placa base cerca del CPU.

## Notas técnicas

- El EPS 8 pines entrega corriente continua (DC) de 12 V a la CPU, proviene de los estándares ATX/EPS12V,
tiene una corriente maxima de 28 A aprox. y tiene un requisito de cable de 16-18 AWG cobre.

# Cable PCIe 6/8p

**Descripción breve:** Cable adaptador de alimentación para tarjetas gráficas.<br>
**Pines/Carriles/Voltajes/Velocidad:** 6/8 pines, 16 carriles, 75W(6p)/150W(8p), no velocidad(no transmiten datos)<br>
**Uso principal:** Alimentar tarjetas gráficas (GPU) de gama media y alta que requieren más energía de la que puede suministrar la placa base<br>
**Compatibilidad actual:** Alta

## Identificación física

- Conectores rectangulares, tiene llaves que impiden conectarlos incorrectamente, color amarillo +12V y negro: tierra, se encuentra en la fuente de alimentación.

## Notas técnicas

- No tienen versiones ya que solo entregan corriente, limitaciones de 75 W (6 pines), 150 W (8 pines), requisitos de 12 V, cable AWG16–18 , compatibilidad muy alta con GPUs PCIe desde hace 20 años

# Cable SATA Power

**Descripción breve:** es una interfaz de transferencia de datos
en serie entre la placa base y algunos dispositivos de almacenamiento. <br>
**Pines/Carriles/Voltajes/Velocidad:** 15 pines, No utiliza carriles (transmisión serial), 
+12V, +5V, +3.3V <br>
Velocidad: SATA 1.0: 1.5 Gbps / SATA 2.0: 3 Gbps / SATA 3.0: 6 Gbps / SATA 3.2 (o posterior): Hasta 12 Gbps <br>
**Uso principal:** Suministra energía directamente desde la fuente de alimentación al disco duro o unidad óptica. <br>
**Compatibilidad actual:** Alta

## Identificación física

Tiene forma de L con colores amarillo rojo y negro y se encuentra en la fuente de poder.

## Notas técnicas

Versiones: SATA I, II y III
Necesita ser suministrado por la fuente de alimentación del ordenador.
El cable de datos SATA tiene 7 pines y permite la conexión de una sola unidad. 

<a id="3-conectores-de-datos"></a>
## 3. Conectores de datos
# Conector M.2 NVMe

**Descripción breve:** Rrotocolo de almacenamiento y transferencia especialmente diseñado para 
medios de almacenamiento no volátiles de alto rendimiento.<br>
**Pines/Carriles/Voltajes/Velocidad:**  Hasta 67 pines y un paso de \(0.5\) mm, carriles como x1, x4, x8 y x16.
Voltaje de funcionamiento principal de $3.3$V, las velocidades teóricas pueden alcanzar hasta 20 Gbps.
**Uso principal:** Los SSD NVMe ofrecen mayor rendimiento y menor latencia que los protocolos anteriores,
lo que los hace ideales para aplicaciones informáticas intensivas como el trabajo creativo profesional.
**Compatibilidad actual:**Mediaa

## Identificación física
- Forma rectangular y plana, llaves como B kay/M key y B+M Key, normalmente es negro o verde en la PCB de la placa base.
Simbolos: M.2 PCIe 3.0 x4 / NVMe → indica soporte NVMe/M.2 SATA → solo compatible con SSD SATA
Se encuantran cerca de la CPU o ranuras PCIe, horizontal o ligeramente inclinada.
## Notas técnicas
Versiones: NVMe 1.2/NVMe 1.3/NVMe 1.4/NVMe 1.5/NVMe 2.0
Longitud física de la SSD: 22 mm ancho / Protocolo: no todas las ranuras M.2 aceptan NVMe; algunas solo SATA.
Potencia maxima de 8-12W por SSD
M.2 NVMe no usa cables externos: se conecta directamente a la ranura M.2 de la placa base.
GT/s pero en el bus PCIe.

# Conector de datos: SATA (Serial ATA)

**Descripción breve:** Interfaz de datos en serie para conectar HDD/SSD/unidades ópticas.  
**Pines/Carriles/Voltajes/Velocidad:** 7 pines · 1.5/3/6 Gbps (SATA I/II/III)  
**Uso principal:** Conexión de almacenamiento interno común  
**Compatibilidad actual:** Alta

## Identificación física
- Conector plano en forma de L; cables delgados, longitud típica ≤1 m.

## Notas técnicas
- Hot-swap según controladora; no lleva alimentación (va por conector SATA power).

  

<a id="4-slots-de-expansion"></a>
## 4. Slots de expansión
# Slot: M.2 Wi-Fi

**Descripción breve:** ranura de expansión compacta (Next Generation Form Factor o NGFF) que se encuentra en
ordenadores modernos yque permite conectar una tarjeta de módulo para redes inalámbricas, como la conexión Wi-Fi y Bluetooth.<br>
**Pines/Carriles/Voltajes/Velocidad:** 
- Pines y carriles: Utiliza la interfaz PCIe, no SATA, ya que ofrece mayor velocidad.
- Voltaje: 3.3V
- Velocidad: Wi-Fi 5 (1.3 Gb/s), Wi-Fi 6 (2.4 Gb/s), Wi-Fi 6E / 7 (4.8 Gb/s o más)<br>
**Uso principal:** El uso principal de una ranura M.2 para Wi-Fi es para instalar un módulo de red inalámbrica, como una
tarjeta Wi-Fi/Bluetooth, que aprovecha esta interfaz de factor de forma compacto para conectarse directamente a la placa base del ordenador.
**Compatibilidad actual:** Alta

## Identificación física
- Pequeño y rectangular, y tiene una sola muesca (Key E) situada hacia el lado izquierdo
- Son generalmente verdes, y el slot suele ser negro o beige en la placa base.
- En la placa suele aparecer serigrafiado como “M.2 (Wi-Fi)”, “E Key”, “CNVi”, o “WLAN”.
- Está cerca de las salidas de audio o USB traseras de la placa base (zona superior-trasera) o junto a las ranuras PCIe.

## Notas técnicas
- Versiones
- Limitaciones: Las principales limitaciones al usar un slot M.2 para Wi-Fi son el tipo de slot y el ancho de banda,
ya que un slot para Wi-Fi no puede ser utilizado para un SSD NVMe de alta velocidad.
- No requiere cable
- Hz: 100 MHz en el bus PCIe / GT/s: 5 GT/s (PCIe 2.0 x1) o 8 GT/s (PCIe 3.0 x1)

# Slot: PCIe Gen4

**Descripción breve:** es la cuarta generación de la interfaz Peripheral Component Interconnect Express,
que duplica la velocidad de datos de su predecesor, PCIe 3.0. <br>
**Pines/Carriles/Voltajes/Velocidad:** Carriles y pines: x1(18p),4(32p),x8(49),x16(82) / Velocidad por carril: 16GT/s<br>
**Uso principal:** Permite la conexión de dispositivos de alto rendimiento, como tarjetas gráficas (GPU) y unidades de estado sólido (SSD) NVMe, ofreciendo un mayor ancho de banda y velocidad para aplicaciones exigentes. <br>
**Compatibilidad actual:** Alta

## Identificación física
- Rectangular largo, con una sola muesca (llave) hacia un extremo.<br>
- Suelen ser negros o gris metalizado<br>
- Serigrafiado en la placa como “PCIEX16_1”, “PCIe 4.0 x16” o “PCIe Gen 4”. Algunos modelos también marcan “x16_4.0” para distinguirlo del 3.0.<br>
- Generalmente es el primer slot debajo del procesador (CPU), el más cercano al socket.
  
## Notas técnicas
- Versione: PCIe 4.0<br>
- Retrocompatible con PCIe 3.0 y 2.0 (funciona pero a menor velocidad). El rendimiento real depende del número de carriles activos (x4, x8, x16).<br>
- Ofrece hasta 31.5 GB/s en x16, opera a 100 MHz, usa 12 V y 3.3 V, no tiene PD<br>
- Alcanza 16 GT/s por carril..

# Slot: PCI Express x16 (Gen4/Gen5)

**Descripción breve:** Ranura de expansión de altas prestaciones usada para GPUs/aceleradoras.  
**Pines/Carriles/Voltajes/Velocidad:** x16 carriles · Gen4 16 GT/s · Gen5 32 GT/s  
**Uso principal:** Tarjetas gráficas; también aceleradoras y NVMe en adaptador  
**Compatibilidad actual:** Alta

## Identificación física
- Ranura larga con pestaña; color variable por fabricante.

## Notas técnicas
- Ancho de banda efectivo depende de generación y carriles disponibles (CPU/Chipset).

  
<a id="5-conectores-externos"></a>
## 5. Conectores externos
# Conector DisplayPort 1.4

**Descripción breve:** permite reproducir vídeos de hasta 7680 x 4320 (8K) a 60Hz con un ancho de banda de 32,4 Gb/s,
y soporta la mayoría de los formatos de vídeo en 3D <br>
**Pines/Carriles/Voltajes/Velocidad:** 20 pines, 4 carriles, no voltajes, ancho de banda: 32,4 Gbps (total), velocidad de datos: 25,92 Gbps<br>
**Uso principal:** Permite actualizaciones de pantalla «parciales» desde la GPU,
especialmente cuando se trata de páginas o contenido estático en una parte de la pantalla con la que no está interactuando.<br>  
**Compatibilidad actual:** Alta
## Identificación física
- Forma: rectangular
- Llaves: tiene una muesca o bisel en la parte superior que asegura la orientación correcta.
- Colores: Generalmente negro, gris oscuro o plateado.
- Simbolos: Lleva grabado o impreso el logo “DP” / Algunos cables certificados muestran “HBR3 / 1.4” indicando la versión y ancho de banda.
- Ubicacion: El conector principal suele estar en el panel trasero de la GPU o monitor, y el mini DP en el lateral o trasero de laptops.

## Notas técnicas
- Versiones: DP 1.0 / 1.1  / DP 1.2 / DP 1.3 / DP 1.4
- Limitaciones: Para 8K o 4K a 120 Hz se requiere DSC / Limitado por el tipo de cable / No transporta energía significativa
- Requisitos de cable: Cable certificado HBR3 / DP 1.4 para 32.4 Gbps. / Longitud recomendada: hasta 2 m sin pérdida
- Hasta 120 Hz en 4K / 60 Hz en 8K con DSC / Hasta 8.1 GT/s por línea en HBR3, 4 líneas → 32.4 Gbps

# Conector HDMI 2.1

**Descripción breve:** HDMI 2.1 es la última versión del estándar para transmitir audio y video .<br>
**Pines/Carriles/Voltajes/Velocidad:** 19 pines, no se especifican carriles ni voltaje.<br>
Velocidad: Ancho de banda: Hasta 48 Gbps / Resoluciones soportadas: Hasta 8K a 60Hz y 4K a 120Hz sin compresión<br>
**Uso principal:** El uso principal del HDMI 2.1 es transmitir vídeo y audio de alta calidad con un mayor ancho de banda,
permitiendo resoluciones de hasta 10K y 8K a 60Hz, y 4K a 120Hz.<br>
**Compatibilidad actual:** Alta

## Identificación física
- Forma: conector plano y ancho
- Llaves: tiene una muesca interna asimétrica 
- Colores: Color negro o gris metálico.
- Simbolos: Lleva grabado o impreso el logo “HDMI”, a veces acompañado de “2.1” o “Ultra High Speed”.
- Ubicacion: En la parte trasera o lateral de televisores, monitores, consolas (PS5, Xbox Series X/S),
tarjetas gráficas, receptores AV, portátiles y proyectores, en placas base o GPUs, normalmente está en el panel trasero de E/S.

## Notas técnicas
- Versiones: HDMI 1.4: hasta 10.2 Gbps → 4K a 30 Hz / HDMI 2.0: hasta 18 Gbps → 4K a 60 Hz / HDMI 2.1: hasta 48 Gbps → 8K a 60 Hz o 4K a 120 Hz
- Limitaciones: Para aprovechar sus funciones, el dispositivo, el cable y la pantalla deben ser HDMI 2.1. / Los cables antiguos limitan el ancho de banda.
- Requisitos del cable: Se necesita un cable “Ultra High Speed HDMI” certificado / Blindaje reforzado / Compatible con HDCP 2.3 y eARC
- Hz: Hasta 120 Hz en 4K / 60 Hz en 8K / GT/s: 12 GT/s por línea, 4 líneas → 48 GT/s total

# Modulo RJ-45 1G

**Descripción breve:** Módulo SFP de cobre diseñado para quienes requieren una solución robusta y adaptable para su red <br>
**Pines/Carriles/Voltajes/Velocidad:**  8 pines, 4 carriles trenzados, voltaje ±2.5 V por par, 1Gbps full duplex <br>
**Uso principal:** Su función es conectar dispositivos como ordenadores, routers, switches, impresoras y consolas de 
videojuegos a la red de área local (LAN) para la transmisión de datos y acceso a Internet. <br>
**Compatibilidad actual:** Alta

## Identificación física
- Forma: cocector rectangular de plástico
- Llaves: posee una pestaña plástica de retención en la parte superior que asegura la conexión y evita que se desconecte accidentalmente.
- Pueden ser amarillo, azul, gris, rojo, verde o negro.
- Algunos conectores llevan grabado el logo “Ethernet” o un símbolo de red.
- Se encuantra en el panel trasero de PCs, servidores o equipos de red, y también en paredes con rosetas RJ45 para cableado estructurado.

## Notas técnicas
- Versiones: 10BASE-T / 100BASE-TX / 1000BASE-T / 10GBASE-T
- Limitaciones: Alcance máximo de 100 metros / Limitado a par trenzado balanceado
- Requisitos del cable: Cable Cat5e mínimo para 1 Gbps; Cat6 o superior recomendado para estabilidad
- 125 MHz para Gigabit Ethernet

# Conector USB-A 2.0

**Descripción breve:** Es un estándar de conexión USB que se caracteriza por su conector rectangular (USB-A) y
una velocidad de transferencia de datos de hasta 480 Mbps.<br>
**Pines/Carriles/Voltajes/Velocidad:** 
- Pines: 4 pines [Pin 1 (VBUS), Pin 2(D-), Pin 3(D+), Pin 4 (GND)
- Carriles: 2 (D- y D+)
- Voltaje: 5V
- Velocidad: 480 Mbps (en la teoria), 280 Mbps (practica)<br>
**Uso principal:** Permiten transferir datos, imágenes, vídeos y archivos en general a una velocidad de 60 Mb por segundo.
Gracias a esto, se ha convertido en la versión más común de entradas en la mayoría de los ordenadores y dispositivos informáticos.<br>
**Compatibilidad actual:** Alta

## Identificación física
- Forma: Rectangular
- Color: Negro (color mas comun)
- Simbolo: El símbolo del tridente es la clave para identificarlo.
- Ubicacion: Normalmente se encuentran en la parte trasera de los PCs de escritorio o en los laterales de los portátiles.

## Notas técnicas
- Versiones: Sucesor del USB 1.1
- Velocidad máxima: 480 Mbps (0.48 Gbps) / No soporta vídeo ni modos alternativos (solo datos y energía) / Potencia limitada: 5 V a 0.5 A → 2.5 W máximo.
- Requisitos del cable: Usa 4 hilos internos, 2 de energía (VCC, GND) y 2 de datos (D+, D−) / Longitud recomendada: máximo 5 m para mantener buena señal.
- Hz: 480 MHz

# Conector USB-B

**Descripción breve:** Es un tipo de conector empleado para comunicar dispositivos con el PC u otros ordenadores
**Pines/Carriles/Voltajes/Velocidad:** 
- Pines: El USB tipo B tiene 4 o 5 pines (VBUS/alimentación, D-/datos, D+/datos, GND/tierra)
- Voltaje: 5V
- Carriles: No utiliza carriles de datos en el mismo sentido que el USB-C
- Velocidades: Dependen del estándar USB como 480 Mbps para USB 2.0 y hasta 10 Gbps para USB 3.2 Gen 2,
que usa conectores Micro-USB 3.0 de 10 pines<br>
**Uso principal:** Se utiliza principalmente en dispositivos que tradicionalmente han contado con este puerto, como routers, impresoras y fotocopiadoras.<br>
**Compatibilidad actual:** Media

## Identificación física
- Forma: Casi cuadrada
- Llaves: posee una muesca interna que evita insertarlo al revés (solo entra en una dirección).
- Colores: Negro, Azul, Turquesa o celeste
- Símbolos: Lleva el símbolo universal USB (tridente con tres puntas: flecha, círculo y cuadrado).
- Se encuantra en la parte trasera de impresoras, escáneres, interfaces de audio, hubs o discos duros externos.
## Notas técnicas
- Versiones: USB-B 1.1, USB-B 2.0, USB-B 3.0 / 3.1
- Limitaciones: Tamaño físico grande → no apto para dispositivos compactos, no transporta vídeo ni modos alternativos (solo datos y energía), no reversible (solo entra de una forma)
- Requisitos de cable: USB-B 2.0: 4 hilos / USB-B 3.0: 9 pines, longitud máxima recomendada: 5 m (USB 2.0) o 3 m (USB 3.0).
- Hz: 480 MHz en USB 2.0 / ~5 GHz en USB 3.0

<a id="6-bibliografia"></a>
## 6. Bibliografía
https://en.wikipedia.org/wiki/12VHPWR
https://www.profesionalreview.com/2018/11/10/alimentacion-atx-24-pines-eps/ https://hardzone.es/tutoriales/componentes/conectores-fuente-atx-eps-placa-base/
https://www.moddiy.com/pages/Power-Supply-Connectors-and-Pinouts.html
https://hardzone.es/tutoriales/componentes/conectores-fuente-atx-eps-placa-base/
https://hardzone.es/tutoriales/componentes/conectores-fuente-alimentacion/
https://www.corsair.com/es/es/explorer/diy-builder/power-supply-units/individual-8-pin-vs-pigtail-connectors-for-gpus/
https://www.ordenatech.es/conector-sata-caracteristicas-y-ventajas/
https://ibericavip.com/blog/pc-workstation/guia-para-principiantes-sobre-cables-sata-todo-lo-que-necesitas-saber/
https://www.ibm.com/es-es/think/topics/nvme-vs-m2
https://www.profesionalreview.com/guias/que-es-el-formato-m-2-en-los-ssd/
https://www.pccomponentes.com/que-son-y-para-que-se-usan-los-cables-serial-ata-o-sata
https://ibericavip.com/blog/pc-workstation/guia-para-principiantes-sobre-cables-sata-todo-lo-que-necesitas-saber/
https://www.assured-systems.com/es/faq/what-is-a-m-2-key/
https://www.corsair.com/es/es/explorer/glossary/what-is-m2/
https://www.kingston.com/unitedkingdom/latam/blog/pc-performance/pcie-gen-4-explained
https://www.adata.com/ar/quikTips/pcie3-vs-pcie4-speed-compatibility/
https://www.intel.la/content/www/xl/es/gaming/resources/what-is-pcie-4-and-why-does-it-matter.html
https://pcisig.com/ https://www.profesionalreview.com/2021/10/03/tarjeta-grafica-pci-express-x16/
https://ibericavip.com/blog/pc-workstation/todos-los-tipos-de-ranuras-pcie-explicados-y-comparados/?srsltid=AfmBOoqRkbSaZIMGpDn7TWnUmfyt90E21OopStVPLrw-J9sOh4tOlw4B
https://ibericavip.com/blog/pc-workstation/displayport-1-4a-vs-2-0-2-1-en-la-tarjeta-grafica-por-que-es-importante/
https://compukaed.com/tienda/cables/video/displayport/cable-displayport-dp-1-4-de-1-80-metros-ultra-hd-8k-a-60hz-4k-a-144hz-forrado-en-nylon-netcom/
https://fycables.com/es/what-is-displayport-1-4/
https://es.wikipedia.org/wiki/High-Definition_Multimedia_Interface
https://cabletimetech.com/es-es/blogs/knowledge/3-ways-to-identify-hdmi-2-1-cables
https://www.sincables.com.ec/product/ubiquiti-uf-rj45-1g-modulo-sfp-1g-puerto-gigabit-rj45/
https://seetronic.com/es/blog/what-is-an-rj45-connector/
https://www.assured-systems.com/es/faq/what-is-a-rj-45/
https://es.wikipedia.org/wiki/Universal_Serial_Bus
https://www.pcbasic.com/es/blog/usb_pinout.html
https://www.xataka.com/basics/tipos-usb-estandares-conectores-caracteristicas-cada-uno
https://www.anker.com/blogs/cables/how-to-identify-different-types-of-usb-cables-a-brief-guide
https://www.pcbasic.com/es/blog/usb_pinout.html
https://hilelectronic.com/es/usb-pinout/
https://opencircuit.es/blog/usb-a-b-c-mini-micro-welke-usb-kabel-heb-je)
