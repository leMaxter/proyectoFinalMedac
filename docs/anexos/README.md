# Anexos TrazaOS

Los anexos incluyen material que complementa la explicacion del proyecto. No sustituyen al contenido principal de la memoria, sino que sirven como evidencias visuales y tecnicas del producto desarrollado.

Todas las imagenes de esta seccion estan guardadas en [`imagenes/`](imagenes/), para que puedan visualizarse correctamente desde gitHub.

## Anexo I - Pantallas Principales De La Aplicacion

### Login

Pantalla de acceso a TrazaOS. Permite iniciar sesion como administrador o conductor mediante Supabase Auth.

![Login TrazaOS](imagenes/login.png)

### Centro De Mando

Vista ejecutiva del administrador. Resume el estado general de la empresa: flota, pedidos pendientes, rutas activas y entregas.

![Centro de mando](imagenes/centroMando.png)

### Operaciones Y Mapa Logistico

Pantalla de trabajo diario. Permite crear pedidos, revisar el mapa, asignar rutas y lanzar la optimizacion con IA.

![Operaciones y mapa logistico](imagenes/operacionesMapa.png)

### Inventario

Modulo para gestionar productos, stock disponible, minimos, pesos y precios.

![Inventario](imagenes/inventario.png)

### Inteligencia IA Y Big Data

Panel analitico para revisar eventos, calidad de los datos, variables del modelo, tracking GPS y metricas operativas.

![Inteligencia IA y Big Data](imagenes/inteligencia.png)

## Anexo I.II - Panel De Administracion

El panel de administracion se divide en varias secciones para mantener separados los datos maestros de la empresa.

### Empresa

Configuracion de datos generales de la empresa.

![Administracion empresa](imagenes/adminEmpresa.png)

### Gestion De Flota

Alta y mantenimiento de vehiculos, tipo y capacidad maxima.

![Administracion flota](imagenes/adminFlota.png)

### Equipo

Gestion de conductores y asignacion de vehiculos.

![Administracion equipo](imagenes/adminEquipo.png)

### Inventario Y Catalogo

Vista de catalogo desde configuracion, orientada a mantenimiento de productos.

![Administracion inventario y catalogo](imagenes/adminInvenCat.png)

### Historial De Operaciones

Consulta historica de pedidos y entregas completadas.

![Administracion historial](imagenes/adminHistorial.png)

## Anexo I.III - App Del Conductor

La app del conductor esta disenada para uso movil. El conductor solo ve el vehiculo asignado y las rutas vinculadas a su perfil.

### Jornada Del Conductor

Vista principal de la jornada, estado de conexion, GPS y sincronizacion.

![App conductor jornada](imagenes/conductor1.png)

### Entrega Y Sincronizacion

Pantalla de apoyo para finalizar o sincronizar entregas con evidencias.

![App conductor entrega](imagenes/conductor2.png)

## Anexo II - Arquitectura General

### Arquitectura General

Este diagrama muestra la separacion entre frontend, Supabase, motor IA, app conductor, event lake y la capa de decision.

![Arquitectura TrazaOS](imagenes/arquitectura_trazaos.png)

## Anexo III - Modelo De Datos Simplificado

Resume las tablas principales del sistema: 'empresas', 'profiles', 'vehiculos', 'stock', 'pedidos', 'eventos_logisticos' y 'tracking_eventos'.

![Modelo de datos TrazaOS](imagenes/modelo_datos_trazaos.png)

## Anexo IV - Pipeline Big Data

El pipeline Big Data representa como la actividad operativa se transforma en eventos, capas analiticas e indicadores para la toma de decisiones.

![Pipeline Big Data TrazaOS](imagenes/pipeline_bigdata_trazaos_detallado.png)

## Anexo V - Fragmento Motor De Optimizacion IA

Fragmento del motor Python donde se utiliza Google OR-Tools para resolver el problema de rutas con restricciones de capacidad, distancia y orden de paradas.

![Fragmento motor IA](imagenes/fragmentoMotorIA.png)

## Anexo VI - Fragmento Seguridad RLS / RPC

Fragmento de la funcion de cierre seguro de entrega. Valida usuario autenticado, rol conductor, empresa, vehiculo asignado y pedido antes de modificar el estado de la entrega.

![Fragmento seguridad](imagenes/fragmentoSeguridad.png)

## Anexo VII - Guion De Demostracion (Visible en videos de la defensa)

Flujo recomendado para ver TrazaOS:

1. Login administrador.
2. Centro de mando.
3. Revision de inventario.
4. Creacion de pedido en Operaciones.
5. Optimizacion de ruta con IA.
6. Revision del mapa y vehiculo asignado.
7. Login como conductor.
8. Finalizacion de entrega con foto y firma.
9. Consulta de Inteligencia IA y Big Data.

Este recorrido permite demostrar el ciclo completo de TrazaOS: los pedidos, optimizacion, ruta, entrega, evidencia y analisis.
