# Indicadores de control y estándares de desempeño

Indicadores para auditar el sistema de gestión de pedidos y control de producción de la Zinguería "El Negro". Cada uno responde a una meta del TP2 o a un paso del BPMN.

> Los estándares son **propuestos**. Los que dependen de una situación actual (tiempo de carga) se fijan contra una **línea base** medida durante el relevamiento, no con un número inventado.

| # | Indicador | Fórmula | Estándar de desempeño | Frecuencia | Fuente del dato |

| 1 | Tiempo de carga y presupuestado de un pedido | Promedio de minutos entre el inicio del registro y el envío del presupuesto | Reducción de al menos 50 % respecto de la línea base, dentro de los 2 primeros meses de uso | Semanal | Registros del sistema (HU-1) |
| 2 | Pedidos con estado actualizado | Pedidos activos con estado vigente / pedidos activos × 100 | 95 % o más, dentro de los 3 meses de implementación | Semanal | Campo `estado_pedido` (HU-2) |
| 3 | Cumplimiento de fecha de entrega | Pedidos entregados en o antes de `fecha_entrega_estimada` / pedidos entregados × 100 | 90 % o más | Mensual | Entidad Pedido |
| 4 | Tasa de retrabajo | Piezas rechazadas en control de calidad / piezas controladas × 100 | 5 % o menos | Semanal | Órdenes de producción (compuerta "¿Pieza aprobada?") |
| 5 | Quiebres de stock de chapa | Cantidad de pedidos demorados por falta de material | 0 por mes; alerta al llegar al stock mínimo | Mensual | Control de stock (HU-3) |
| 6 | Desvío de cronograma del proyecto | (Semanas reales − semanas planificadas) / semanas planificadas × 100 | 10 % o menos sobre las 14 semanas del Gantt | Semanal | Tablero y diagrama de Gantt (TP2) |

## Acciones correctivas

| Si el indicador... | Acción |

| 1 no baja respecto de la línea base | Revisar el formulario de carga y reforzar la capacitación al personal de atención |
| 2 queda debajo del estándar | Revisar con Producción cuándo se actualiza el estado y simplificar el registro |
| 3 queda debajo del estándar | Revisar el cálculo de la fecha estimada y la carga de las órdenes |
| 4 supera el estándar | Revisar el paso de corte y plegado y los criterios del control de calidad |
| 5 registra quiebres | Ajustar el stock mínimo y adelantar la compra a proveedores |
| 6 supera el estándar | Reprogramar tareas y recortar el alcance de la iteración |
