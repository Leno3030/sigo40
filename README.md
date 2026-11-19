# SIGO 4.0 – Sistema Integrado de Gestión de Obras
Constructora Andes Sur 4.0 S.A.C. · Principios de los Sistemas de Software Distribuido (IS6085SP) · 2026-I

Prototipo en Java 17 + Gradle (sin librerías externas).

## Estructura
| Paquete | Contenido | Sección PPT |
|---|---|---|
| `comun` | Protocolo propio y lector JSON | 8, 9 |
| `servidor` | Servidor TCP (5000) y receptor UDP (5001) | 9 |
| `cliente` | `ClienteParte` (TCP) y `SensorUDP` | 9 |
| `algoritmo` | Simulación del algoritmo del Matón (Bully) | 10 |
| `blockchain` | Bloque, cadena y demo con alteración | 11 |

## Protocolo (una línea por mensaje)
`ENVIAR_PARTE {json}` · `PEDIR_MATERIAL {json}` · `PING` · `SALIR`  →  `OK {json}` | `ERROR mensaje`

## Cómo ejecutar
```
gradle run            # servidor (TCP 5000 + UDP 5001)
gradle runParte       # cliente de la obra (en otra terminal)
gradle runSensor      # sensor de curado UDP (en otra terminal)
gradle runBully       # simulación de elección de líder
gradle runBlockchain  # cadena de 3 actas y detección de alteración
```
Para probar entre dos PC: `gradle runParte --args="192.168.10.5"`.

## Integrantes
- A – Analista de redes: 
- B – Desarrollador de comunicaciones: 
- C – Arquitecto de algoritmos: 
