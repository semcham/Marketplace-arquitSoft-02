# Actores del sistema

## 1. Descripción

El sistema corresponde a un marketplace de productos para mascotas, donde
diferentes sellers pueden ofrecer sus productos y los clientes pueden
consultarlos y realizar compras mediante la plataforma.

Para el funcionamiento del sistema se identifican actores principales,
actores administrativos y servicios externos que interactúan con la
plataforma.

## 2. Actores identificados

| ID  | Actor                   | Tipo      | Descripción                                                                                                                                 |
| --- | ----------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| A01 | Cliente                 | Principal | Usuario que busca productos, consulta información, gestiona su carrito, realiza pedidos, efectúa pagos y consulta el estado de sus compras. |
| A02 | Seller                  | Principal | Vendedor que registra, actualiza y administra los productos que ofrece en la plataforma y consulta información relacionada con sus ventas.  |
| A03 | Administrador           | Principal | Usuario responsable de administrar y supervisar la plataforma, incluyendo la gestión de sellers y operaciones generales.                    |
| A04 | Pasarela de pago        | Externo   | Servicio externo encargado de procesar los pagos realizados por los clientes.                                                               |
| A05 | Servicio de envío       | Externo   | Servicio encargado de gestionar la información relacionada con la entrega de los pedidos.                                                   |
| A06 | Servicio de facturación | Externo   | Servicio encargado de generar los comprobantes correspondientes a las compras realizadas.                                                   |
| A07 | ERP                     | Externo   | Sistema externo que proporciona información relacionada con los productos y el stock disponible.                                            |

## 3. Responsabilidades de los actores

### A01 - Cliente

- Buscar productos.
- Consultar información y disponibilidad de productos.
- Agregar productos al carrito.
- Modificar o eliminar productos del carrito.
- Realizar pedidos.
- Efectuar pagos.
- Consultar sus pedidos.
- Consultar el estado de sus pedidos.

### A02 - Seller

- Registrar productos.
- Actualizar información de productos.
- Consultar sus productos.
- Gestionar la información relacionada con sus ventas.

### A03 - Administrador

- Administrar la plataforma.
- Registrar sellers.
- Actualizar información de sellers.
- Desactivar sellers.
- Supervisar las operaciones de la plataforma.

### A04 - Pasarela de pago

- Recibir las solicitudes de pago.
- Procesar las operaciones de pago.
- Informar el resultado de la operación.

### A05 - Servicio de envío

- Recibir información relacionada con los pedidos.
- Gestionar la información de entrega.
- Proporcionar información sobre el estado de la entrega.

### A06 - Servicio de facturación

- Recibir información de las operaciones realizadas.
- Generar comprobantes de pago.
- Proporcionar la información del comprobante generado.

### A07 - ERP

- Proporcionar información de productos.
- Proporcionar información de stock.
- Mantener la información relacionada con disponibilidad de productos.
