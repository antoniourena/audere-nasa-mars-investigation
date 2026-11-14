# audere-nasa-mars-investigation
Nasa
# Audere: Mars EVA Navigator
**Copiloto táctico multicapa para la navegación segura y exploración científica de astronautas en Marte.**

---

## 1. Problema y Propuesta de Solución
* **El Problema:** Herramientas actuales como *Mars Trek* ofrecen vistas globales o regionales pensadas para rovers, pero no integran en tiempo real los riesgos físicos de desplazamiento humano (pendientes críticas, trampas de arena, radiación y tormentas de polvo) junto con los objetivos científicos.
* **Nuestra Solución:** Una interfaz interactiva estilo *Google Maps + Waze* que fusiona datos orbitales y de superficie de la NASA para trazar rutas seguras (algoritmo A*), calcular el consumo de oxígeno ($O_2$) y recalcular desvíos o rutas de evacuación en vivo ante una tormenta de arena.

---

## 2. Arquitectura de Datos (Capas Integradas)
El sistema cruza cuatro categorías de datos reales almacenados localmente en `/data`:
1. **Atmosféricos (`/data/atmosfericos`):** Opacidad óptica por polvo ($\tau$), temperatura, presión y dosis de radiación superficial (instrumentos REMS, MEDA y RAD).
2. **Topográficos (`/data/topograficos`):** Modelos Digitales de Elevación (DEM) y mapas de pendiente en grados (MRO HiRISE / MOLA).
3. **Ópticos (`/data/opticos`):** Imágenes orbitales de alta resolución e imágenes crudas en primera persona tomadas por *Curiosity* y *Perseverance* (Mastcam-Z / Navcam).
4. **Térmicos (`/data/termicos`):** Mapas de inercia térmica para diferenciar lecho rocoso firme de arena suelta (Mars Odyssey THEMIS).

---

## 3. Reglas Físicas y Supuestos del Modelo
Para garantizar la supervivencia del astronauta (gravedad marciana $0.38g$), el motor de rutas aplica los siguientes umbrales:
* **Pendiente máxima segura:** $\le 15^\circ$ (inclinaciones mayores bloquean la ruta por riesgo de caída con traje presurizado).
* **Penalización por suelo blando:** Caminar sobre zonas de baja inercia térmica (polvo fino/arena) incrementa el gasto metabólico y consumo de $O_2$ en un factor de $1.8\times$.
* **Protocolo de Tormenta de Arena ($\tau > 2.5$):** Si un frente de polvo intercepta la ruta activa y el $O_2$ restante es $\ge 35\%$, el sistema traza un desvío seguro; si es $< 35\%$, ordena evacuación inmediata al hábitat o rover más cercano.

---

## 4. Trazabilidad de Fuentes Oficiales (NASA / USGS)
| Capa / Archivo | Instrumento / Misión | Unidades | URL Oficial | Limitaciones / Notas |
| :--- | :--- | :--- | :--- | :--- |
| `gale_atm_clima.csv` | Curiosity REMS / RAD | °C, Pa, mSv/día, $\tau$ | https://worldview.earthdata.nasa.gov/ | Valores estacionales de referencia |
| `gale_topo_dem.png` | MRO HiRISE | Metros / Grados | https://trek.nasa.gov/mars/ | Recorte hiperlocalizado de 500x500 m |
| `jezero_opt_raw01.jpg` | Perseverance Mastcam-Z | Píxeles (RGB) | https://mars.nasa.gov/mars2020/multimedia/raw-images/ | Sol [Anotar número de Sol] |
| Unidades Geológicas | USGS Astrogeology | Polígonos | https://astrogeology-usgs.hub.arcgis.com/pages/interactive-maps-mars | Cartografía regional de referencia |

---

## 5. Cómo Ejecutar el Prototipo
1. Descargar o clonar este repositorio (`Code` -> `Download ZIP`).
2. Abrir el archivo `index.html` directamente en cualquier navegador web (funciona 100% sin conexión a internet).
3. Seleccionar un objetivo científico en el menú superior, activar las capas de riesgo y presionar **"Simular Tormenta de Arena"** para probar el recálculo dinámico.

---

## 6. Transparencia en el Uso de IA y Equipo
* **Equipo Audere (1er Semestre):** [Nombres de los integrantes y rol de cada uno].
* **Uso de Inteligencia Artificial:** Se utilizaron asistentes de IA para estructurar el esqueleto de código (`HTML/JS`) y optimizar el algoritmo A*; todas las fuentes de la NASA, unidades físicas y umbrales de seguridad fueron investigados, verificados y calibrados manualmente por el equipo.
