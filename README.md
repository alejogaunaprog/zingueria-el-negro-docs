# Sistema de Gestión de Pedidos y Control de Producción — Zinguería "El Negro"

Trabajo Práctico Integrador y Progresivo de **Organización Empresarial** · Tecnicatura Universitaria en Programación a Distancia · Universidad Tecnológica Nacional.

## Descripción del sistema

La Zinguería "El Negro" fabrica piezas plegadas a medida en chapa galvanizada (canaletas, cenefas, babetas, caños de ventilación) y vende elementos tercerizados. Hoy los pedidos se toman de forma manual, lo que demora el presupuesto y dificulta saber qué hay que fabricar y si alcanza la chapa.

El sistema propuesto digitaliza ese proceso:

- Registra el pedido del cliente (minorista o mayorista) con piezas y medidas.
- Calcula el presupuesto y la fecha estimada de entrega.
- Verifica y descuenta el stock de chapa, y avisa cuando hay que reponer.
- Genera las órdenes de producción y muestra el estado de cada pedido (en producción / listo / entregado).

Este repositorio aloja la **documentación técnica** del proyecto. No contiene código fuente.

## Integrantes

| Integrante |
| Gauna Alejo |

**Cátedra:** Docente Titular López Mario Raúl · Docente Tutor Dominguez Gilda Jaquelina.

## Documentación

| Documento | Ubicación |
|---|---|
| Diagrama BPMN del proceso de gestión de pedidos | [`docs/bpmn/`](docs/docs/bpmn/LEEME.md) |
| Historias de usuario | [`docs/historias-de-usuario.md`](docs/historias-de-usuario.md) |
| Indicadores de control y estándares de desempeño | [`docs/indicadores-de-control.md`](docs/indicadores-de-control.md) |
| Entrega 1 · Organización y sistema abierto (TGS) | [`docs/entregas/`](docs/entregas/TP1-organizacion-y-sistema-abierto.pdf) |
| Entrega 2 · FODA, objetivos y Gantt | [`docs/entregas/`](docs/entregas/TP2-foda-objetivos-gantt.pdf) |
| Entrega 3 · Organigrama y diccionario de datos | [`docs/entregas/`](docs/entregas/TP3-organigrama-y-diccionario-de-datos.pdf) |

## Tablero ágil

Tablero de GitHub Projects

Columnas: **Por Hacer → En Progreso → Listo**. Las tres historias de usuario están vinculadas como *issues*.

## Flujo de trabajo con Git

- **`main`** contiene solo documentación revisada.
- Cada cambio se hace en una **rama secundaria** (`docs/bpmn`, `docs/historias-usuario`, `docs/indicadores-control`, `docs/entregas`) y llega a `main` mediante **Pull Request** con revisión de un par.
- **Commits** con formato `tipo(ámbito): descripción en presente`, por ejemplo `docs(bpmn): agrega diagrama del proceso de gestión de pedidos`.
- Los Pull Requests referencian la historia de usuario que corresponde (`Closes #n`).

## Declaración de uso de IA

Usé **Claude** como asistente en las cuatro entregas. Lo usé para ideas de diseño, maquetado de diagramas y documentos, y corrección de ortografía. El contenido lo definí yo. Cada resultado lo revisé y, cuando hizo falta, lo corregí.

### Prompts utilizados y por qué

| Prompt (resumido) | Para qué lo usé | Por qué lo planteé así |
|---|---|---|
| Resolver el ejercicio de la Entrega 1 "relacionándolo con una zinguería que hace plegados en chapa galvanizada" | Llevar la consigna genérica a un caso real del rubro que conozco | Quería que el caso salga de mi contexto y no de un ejemplo inventado por la IA |
| Dicté el contenido para el amrado del bloque del diagrama de sistema abierto (entradas, procesos, salidas, factores económicos) y pedir que lo vuelva a dibujar | Los datos del negocio los conozco yo |
| "Armá el FODA con esto", pasando mis fortalezas, debilidades, oportunidades y amenazas | Maquetar la matriz | El análisis es mío; la herramienta solo lo ordena visualmente |
| Pedir el Gantt a 4 meses dividido por semanas | Ajustar el cronograma a lo que pedía la consigna | Iteré el resultado hasta que coincidiera con la planificación real |
| Resolver un problema de legibilidad | Revisé el resultado visual contra la hoja real |
| "¿Por qué la clave?" sobre una columna PK/FK que la IA agregó en el diccionario de datos | Entender la decisión antes de aceptarla | La consigna no pedía esa columna; la cuestioné y la eliminé |
| Entrega 4: leer la consigna, armar el BPMN, proponer las historias de usuario y los indicadores | Acelerar el armado de la documentación | Revisé cada resultado contra mi proceso real y contra el diccionario de datos |

Soy responsable de la veracidad y la coherencia de todo el contenido de este repositorio.
