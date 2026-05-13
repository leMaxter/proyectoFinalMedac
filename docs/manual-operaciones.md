# Manual De Operaciones

El modulo de Operaciones concentra el trabajo diario de despacho. Esta guia esta orientada al usuario que crea pedidos, revisa el mapa, controla la cola de reparto y ejecuta la optimizacion de rutas.

## Flujo Diario Recomendado

1. Revisar inventario disponible.
2. Crear una nueva orden de envio.
3. Comprobar que el pedido queda en estado pendiente.
4. Ejecutar la optimizacion de rutas.
5. Revisar el vehiculo asignado.
6. Consultar el mapa operativo.
7. Supervisar entregas en ruta.
8. Revisar evidencias una vez completadas.

## Crear Un Pedido

Desde Operaciones se introduce una nueva orden de envio con:

- Cliente.
- Direccion de entrega.
- Producto de stock.
- Cantidad.
- Peso.
- Bultos.
- Prioridad.
- Fecha prevista.
- Contacto y telefono si aplica.
- Referencia externa o albaran.
- Observaciones operativas.

El sistema valida el stock disponible para evitar crear pedidos imposibles.

## Asignacion Manual De Pedidos

Si no se quiere usar la optimizacion automatica, el pedido puede asignarse desde el mapa operativo:

1. Abrir Operaciones.
2. Localizar la Bandeja de asignacion.
3. Arrastrar un pedido sin asignar.
4. Soltarlo sobre la tarjeta del vehiculo.
5. TrazaOS guarda el 'vehiculo_asignado'.

El conductor vinculado a ese vehiculo vera la ruta en su app.

## Optimizacion Con IA

El boton de optimizacion envia los pedidos pendientes y la flota activa al microservicio Python. El motor utiliza Google OR-Tools para resolver el reparto teniendo en cuenta:

- Coordenadas.
- Peso del pedido.
- Capacidad del vehiculo.
- Estado del pedido.
- Proximidad.
- Orden de ruta.
- ETA estimado.

El resultado se guarda en Supabase y queda visible en el mapa y en la app del conductor.

## Mapa Operativo

El mapa muestra:

- Pedidos con coordenadas.
- Vehiculos con GPS disponible.
- Paradas asignadas por vehiculo.
- Lineas de ruta por colores.
- Pedidos sin asignar.

Si hay demasiados registros, el mapa puede mostrar un modo resumen para mantener el rendimiento.

## Evidencias

Cuando el conductor cierra una entrega, TrazaOS guarda:

- Estado del pedido como entregado.
- Foto de entrega.
- Firma digital.
- Actualizacion de stock.
- Evento logistico para analisis posterior.

## Recomendaciones

- Usar la optimizacion cuando haya muchos pedidos.
- Revisar pedidos sin coordenadas antes de calcular rutas.
- Confirmar que los conductores tienen vehiculo asignado.

