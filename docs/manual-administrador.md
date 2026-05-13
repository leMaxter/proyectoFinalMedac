# Manual Del Administrador

El administrador es el usuario responsable de configurar la empresa y mantener actualizados los datos principales de TrazaOS. Antes de empezar las operaciones diarias, este perfil debe preparar la flota, el inventario y los accesos de conductores.

## Acceso A La Plataforma

1. Entrar en la pantalla de login.
2. Iniciar sesion con el email y password de administrador.
3. El sistema redirige al Centro de mando.
4. Desde la barra de navegacion superior se puede acceder a Centro, Operaciones, Inteligencia, Inventario y Configuracion.

Si el usuario no tiene perfil configurado, TrazaOS muestra el primer arranque para crear la empresa inicial.

## Configuracion De Empresa

La empresa es el eje del sistema multiempresa. Cada pedido, producto, vehiculo, conductor y evento queda vinculado a una 'empresa_id'.

Datos recomendados:

- Nombre comercial de la empresa.
- Descripcion breve de la actividad.
- Telefono y email de contacto.
- Direccion.
- Web.
- Logo o color de marca si se utiliza personalizacion.

## Gestion De Flota

Desde Configuracion/Admin, el administrador puede crear y gestionar vehiculos.

Campos principales:

- Nombre del vehiculo.
- Tipo: coche, furgon o camion. (A futuro se añadirá más personalización)
- Capacidad maxima en kg.
- Codigo o referencia operativa interna.
- Estado activo/inactivo.

La capacidad es importante porque el motor de optimizacion evita asignar pedidos que superen la carga disponible.

## Gestion De Conductores

El administrador puede crear conductores y asociarlos a un vehiculo concreto. El conductor no elige vehiculo manualmente ya que TrazaOS lee el 'vehiculo_id' desde su perfil.

Flujo recomendado:

1. Crear o seleccionar un vehiculo.
2. Crear el usuario conductor.
3. Asignar el vehiculo al conductor.
4. Entregar al conductor sus credenciales de acceso.
5. Comprobar que al iniciar sesion entra directamente en la app de conductor.

## Gestion De Inventario

El inventario permite controlar productos, stock, peso y precio.

Campos principales:

- Nombre del producto.
- SKU o referencia.
- Categoria.
- Unidad.
- Stock actual.
- Stock minimo.
- Peso unitario.
- Precio unitario.
- Estado activo.

Antes de crear pedidos reales, se aconseja revisar que los productos tengan stock suficiente, peso y precio configurados.

## Historico Y Reportes

El administrador puede consultar operaciones completadas y exportar informacion en CSV. Esta funcion sirve para revisar actividad comercial, entregas cerradas y soporte documental para contabilidad o facturacion.

## Buenas Practicas (MUY recomendado)

- Mantener la flota actualizada.
- No reutilizar usuarios de conductor entre personas distintas.
- Revisar stock antes de lanzar pedidos.
- Comprobar evidencias de entregas importantes.
- Desactivar vehiculos o productos que no deban usarse.

