# Documentacion Tecnica Resumida

Esta documentacion resume las decisiones principales con las que se ha hecho TrazaOS. Su objetivo es justificar el funcionamiento de la plataforma y facilitar futuras mejoras haciendo de este documento un resumen del codigo fuente.

## Arquitectura General

TrazaOS se compone de:

- Frontend Next.js con App Router.
- Supabase Auth para autenticacion.
- PostgreSQL como base de datos relacional.
- Row Level Security para aislamiento multiempresa.
- Supabase Storage para evidencias.
- Microservicio Python con FastAPI.
- Google OR-Tools para optimizacion de rutas.
- Tablas de eventos para analitica Big Data.

## Seguridad Multiempresa

El campo 'empresa_id' es el eje del aislamiento de datos. Los usuarios se vinculan a una empresa mediante 'profiles'. Las politicas RLS filtran los registros que puede leer o modificar cada usuario.

Roles principales:

- 'admin': gestiona datos de su empresa.
- 'conductor': solo accede a pedidos asignados a su vehiculo.

Las operaciones sensibles se protegen en funciones RPC, por ejemplo el cierre seguro de las entregas.

## Motor De Optimizacion

El microservicio de IA recibe:

- Pedidos pendientes.
- Coordenadas.
- Peso.
- Vehiculos disponibles.
- Capacidad de cada vehiculo.

Google OR-Tools modela el problema como Vehicle Routing Problem y la salida incluye vehiculo asignado, orden de ruta, distancia estimada y ETA.

## Big Data

TrazaOS registra actividad en tablas como:

- 'eventos_logisticos': acciones de negocio y payload JSONB.
- 'tracking_eventos': posiciones GPS historicas.

La arquitectura analitica se plantea en capas:

- Bronze: son los eventos crudos.
- Silver: normalizacion por cada empresa, pedido, vehiculo y fecha.
- Gold: KPIs, alertas, calidad del dato y el forecast.

## Evidencias De Entrega

La app del conductor genera:

- Fotografias.
- Firma digital.
- Actualizacion de estado.
- Reduccion de stock.
- Evento logistico.

Las evidencias se guardan en Storage y se relacionan con empresa y pedido.

## Mejoras Futuras

- Geocodificacion real de direcciones.
- Ventanas horarias por cliente.
- Notificaciones al cliente final.
- Integracion con ERP o facturacion.
- Dashboard historico mensual.
- Monitorizacion de errores y logs.
- Asistente para conductores.
