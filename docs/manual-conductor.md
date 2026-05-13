# Manual Del Conductor

La app del conductor esta disenada para su uso desde el movil. El objetivo es que el conductor pueda ver su jornada, navegar a cada entrega, registrar las evidencias y sincronizar el cierre sin acceder a informacion de administrador.

## Inicio De Sesion

1. Abrir la ruta '/login'.
2. Introducir email y password.
3. Si el perfil tiene rol 'conductor', TrazaOS redirige a '/conductor'.
4. El sistema carga automaticamente el vehiculo asignado.

El conductor no debe introducir codigos manuales ni elegir vehiculo.

## Pantalla de 'Mi Jornada'

La pantalla muestra:

- Vehiculo asignado.
- Estado de conexion.
- Estado GPS.
- Entregas pendientes.
- Entregas pendientes de sincronizar.
- Boton de actualizacion.
- Acceso al Centro conductor si esta disponible.

## Ruta Y Navegacion

Cada pedido asignado al vehiculo aparece como una parada, el conductor puede abrir Google Maps para navegar hasta el destino.

*Recomendacion: la interaccion con la app debe realizarse con el vehiculo detenido. (Se considera en actualizaciones futuras añadir un asistente que funcione con voz para navegar por el menú)

## Finalizar Entrega

Para completar una entrega:

1. Revisar pedido y destino.
2. Hacer fotografia de la mercancia.
3. Recoger firma digital del cliente.
4. Pulsar finalizar entrega.
5. Esperar la confirmacion o guardar para sincronizacion posterior.

## Modo Offline

Si no hay conexion, TrazaOS guarda la entrega en el dispositivo. Y cuando vuelve internet, el conductor puede sincronizarla.

La sincronizacion pendiente incluye:

- Pedido.
- Foto.
- Firma.
- Posicion si esta disponible.

## Mensajes Habituales

| Mensaje                 |              Significado                   |              Accion                  |
|-------------------------|--------------------------------------------|--------------------------------------|
| Sin vehiculo asignado   | El perfil no tiene vehiculo                | Contactar con administracion         |
| GPS con aviso           | No hay posicion actual o permiso denegado  | Revisar permisos del navegador       |
| Entrega guardada        | La entrega esta en el dispositivo          | Sincronizar al recuperar conexion    |
| Ruta cerrada localmente | No quedan paradas activas en el movil      | Subir entrega pendiente              |

## Buenas Practicas (MUY recomendado)

- Mantener la sesion iniciada solo en el dispositivo de trabajo.
- Hacer foto clara y con buene luminosidad de la mercancia.
- Pedir la firma antes de cerrar la entrega.
- Sincronizar las entregas pendientes al terminar la jornada.
- Avisar a administracion si una ruta no aparece.

