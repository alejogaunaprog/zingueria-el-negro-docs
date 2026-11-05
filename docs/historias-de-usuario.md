# Historias de Usuario

Formato: **Como** [usuario], **quiero** [funcionalidad], **para** [beneficio].
Cada historia se vincula con un paso del [BPMN](bpmn/bpmn-gestion-de-pedidos.png), con las entidades del diccionario de datos (TP3) y con una meta del TP2.

---

## HU-1 · Registrar pedido y obtener presupuesto

**Como** empleado de atención al cliente (minorista o mayorista),
**quiero** registrar un pedido con las piezas y medidas solicitadas y obtener automáticamente el presupuesto y la fecha estimada de entrega,
**para** responderle rápido al cliente y evitar errores de cálculo.

- **BPMN:** "Registrar pedido en el sistema" → "Calcular presupuesto y fecha de entrega" → "Enviar presupuesto y fecha al cliente".
- **Entidades:** Cliente, Pedido, DetallePedido.
- **Meta TP2:** reducir el tiempo de carga y presupuestado de un pedido.

**Criterios de aceptación**
1. Se puede cargar un pedido con uno o más ítems (tipo de pieza, medidas, cantidad).
2. El sistema calcula el total presupuestado a partir de `cantidad` y `precio_unitario`.
3. El pedido queda asociado a un cliente, marcado como minorista o mayorista.
4. El sistema propone una fecha de entrega estimada.

---

## HU-2 · Seguir las órdenes de producción

**Como** encargado de producción,
**quiero** ver las órdenes de producción ordenadas por fecha de entrega y marcar su avance (en producción / listo),
**para** organizar el trabajo de la fábrica y mantener el estado del pedido actualizado en tiempo real.

- **BPMN:** "Generar orden de producción" → "Cortar, plegar y soldar" → "Control de calidad" → "Actualizar estado: Listo para entrega".
- **Entidades:** Pedido, OrdenDeProduccion.
- **Meta TP2:** que los pedidos muestren su estado actualizado en tiempo real.

**Criterios de aceptación**
1. Al confirmarse un pedido se genera una orden de producción asociada.
2. Las órdenes se listan ordenadas por fecha de entrega estimada.
3. El operario asignado puede registrar fecha de inicio y fecha de fin.
4. Si la pieza no pasa el control de calidad, la orden vuelve a "en producción" (retrabajo).
5. Al completarse la orden, el estado del pedido pasa a "Listo".

---

## HU-3 · Controlar el stock de chapa

**Como** administrativo,
**quiero** que el sistema verifique y descuente el stock de chapa al confirmarse un pedido, y me avise cuando esté por debajo del mínimo,
**para** reponer a tiempo y evitar que un pedido se demore por falta de material.

- **BPMN:** "Verificar stock de chapa" → compuerta "¿Stock suficiente?" → "Gestionar compra de chapa".
- **Entidades:** Pedido, DetallePedido (y el stock, a definir en la siguiente iteración del diccionario de datos).
- **Meta TP2:** que todas las áreas estén en sintonía con los pedidos a producir y con la reposición de stock.

**Criterios de aceptación**
1. Al registrar un pedido, el sistema verifica si hay chapa suficiente para fabricarlo.
2. Si no hay stock suficiente, avisa a Administración para gestionar la compra.
3. Al confirmarse el pedido, el stock disponible se descuenta.
4. Se muestra una alerta cuando el stock baja del mínimo definido.

---

## Estado en el tablero

| Historia | Estado | Observación |

| HU-1 · Registrar pedido y obtener presupuesto | Listo | Modelada en el BPMN y en el diccionario de datos |
| HU-2 · Seguir las órdenes de producción | En Progreso | Falta definir el detalle de las órdenes en el sistema |
| HU-3 · Controlar el stock de chapa | Por Hacer | El stock se define en la próxima iteración del diccionario |
