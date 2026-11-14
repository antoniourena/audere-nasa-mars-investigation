# Capa Atmosférica y Dinámica de Tormentas (Datos Oficiales NASA)

Base de datos meteorológicos, composición atmosférica, vientos de montaña y dinámica de tormentas de polvo recopilados de misiones de superficie y orbitales de la NASA para el modelado de rutas seguras en caminatas espaciales (EVA).


---

## 1. Composición Química y Propiedades Físicas del Aire
* **Fuentes:** *Curiosity* Sample Analysis at Mars (SAM) y NASA Goddard Space Flight Center (*Mars Fact Sheet*).
* **Dióxido de carbono (CO₂):** 95.32% (95.9% medido en Cráter Gale)
* **Nitrógeno molecular (N₂):** 2.70% (1.9% en Gale)
* **Argón (Ar):** 1.60% (1.9% en Gale)
* **Oxígeno (O₂):** 0.13% (0.16% en Gale; variación estacional de hasta 30%)
* **Monóxido de carbono (CO):** 0.08% (0.06% en Gale)
* **Vapor de agua (H₂O):** 210 ppm
* **Densidad superficial:** ~0.020 kg/m³ (<1% de la densidad terrestre al nivel del mar; exige traje presurizado rígido).

---

## 2. Variables Meteorológicas y Vientos Locales
* **Fuentes:** *Curiosity* REMS (Cráter Gale), *Perseverance* MEDA (Cráter Jezero) e InSight TWINS.

| Variable física | Instrumento NASA | Rango nominal (Despejado) | Rango extremo / Estacional | Unidad |
| :--- | :--- | :--- | :--- | :--- |
| **Presión atmosférica** | MSL REMS / Mars 2020 MEDA | 680 - 780 | 240 (alta montaña Tharsis) a 920 (cuencas bajas) | Pa |
| **Temperatura del aire (1.5 m)** | MSL REMS / Mars 2020 MEDA | -75 a -15 | -92 (madrugada polar/alta) a +5 (verano ecuatorial) | °C |
| **Temperatura del suelo (GTS)** | MSL REMS / Mars 2020 MEDA | -85 a +10 | -95 (madrugada) a +20 (roca oscura al mediodía) | °C |
| **Viento horizontal general** | Mars 2020 MEDA / InSight TWINS | 2.0 - 10.0 | 15.0 - 27.0 (ráfagas en tolvaneras / *dust devils*) | m/s |
| **Vientos catabáticos (ladera)** | MSL REMS (Monte Sharp) | 4.0 - 12.0 | 14.0 - 22.0 (descenso nocturno por cañones y cráteres) | m/s |
| **Humedad relativa** | MSL REMS / Mars 2020 MEDA | < 1% - 15% (día) | Hasta 70% - 100% en madrugadas (escarcha/neblina) | % |

---

## 3. Taxonomía de Tormentas de Arena y Factores de Riesgo
* **Fuentes:** MRO MARCI / Mars Climate Sounder (MCS), MSL Mastcam y Mars 2020 MEDA RDS.
* **Tamaño de partícula suspendida:** 1.5 a 3.0 μm (óxido de hierro fino).
* **Umbral de levantamiento (saltación):** Vientos superficiales de 20 a 30 m/s.
* **Temporada crítica:** Longitud Solar Ls = 180° a 330° (perihelio marciano; origen frecuente en Hellas, Argyre y Acidalia).

| Clasificación | Escala y duración | Opacidad óptica (τ) | Visibilidad horizontal | Efectos secundarios críticos |
| :--- | :--- | :--- | :--- | :--- |
| **Cielo Nominal** | Estable | 0.30 - 0.75 | 15,000 - 25,000 m | Condición óptima para exploración EVA. |
| **Local / Dust Devil** | < 2,000 km (horas a 2 días) | 1.00 - 2.40 | 3,000 - 5,000 m | Caída súbita de presión (0.5–3 Pa) y adherencia electrostática de polvo en visores. |
| **Tormenta Regional** | > 2,000 km (días a 3 semanas) | 2.50 - 5.00 | 300 - 1,000 m | Inversión térmica (días 15 °C más fríos), degradación de sensores ópticos y desvío obligatorio. |
| **Tormenta Global (PEDE)** | Planetaria (1 a 3 meses) | 6.00 - 10.8+ | < 250 m | Bloqueo >99% de luz solar directa; aborto total de misión y evacuación inmediata. |

---

## 4. Eventos Históricos de Referencia (Casos de Prueba)
1. **Tormenta Global de Polvo MY34 (Junio 2018 — Sol 2084 de *Curiosity*):** Observada por MRO MARCI, *Curiosity* y *Opportunity* (Sol 5111). La opacidad (τ) escaló de 0.6 a 8.5 en Cráter Gale y superó 10.8 en *Perseverance Valley*, reduciendo la visibilidad a unos pocos metros y comprimiendo la variación térmica diaria en ~20 °C.
2. **Temporada de Torbellinos de Polvo en Cráter Jezero (2021–2024):** Registrada por Mars 2020 MEDA entre las 11:00 y 15:00 LMST, con ráfagas de hasta 24.8 m/s y levantamiento repentino de columnas de polvo.
3. **Circulación Catabática en Monte Sharp (Cráter Gale):** Registrada continuamente por MSL REMS, mostrando vientos descendentes nocturnos y ascendentes diurnos controlados por la topografía del pico central.

---

## 5. Enlaces Oficiales de Datasets NASA
* **NASA Planetary Data System (PDS Atmospheres):** https://pds-atmospheres.nmsu.edu/
* **NASA Goddard Mars Fact Sheet:** https://nssdc.gsfc.nasa.gov/planetary/factsheet/marsfact.html
* **NASA Worldview (Observación de polvo y clima):** https://worldview.earthdata.nasa.gov/
* **Reportes Meteorológicos MSL REMS:** https://mars.nasa.gov/msl/weather/
* **Reportes Meteorológicos Mars 2020 MEDA:** https://mars.nasa.gov/mars2020/weather/
