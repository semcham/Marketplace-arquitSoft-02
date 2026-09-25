# Requisitos funcionales

## 1. Descripción

Los requisitos funcionales representan las funcionalidades que el marketplace
de productos para mascotas debe proporcionar a sus usuarios y sistemas
externos.

## 2. Requisitos funcionales

| ID   | Requisito funcional                                                                                                                |
| ---- | ---------------------------------------------------------------------------------------------------------------------------------- |
| RF01 | El sistema debe permitir buscar productos mediante criterios de búsqueda.                                                          |
| RF02 | El sistema debe permitir consultar la información, precio y disponibilidad de los productos.                                       |
| RF03 | El sistema debe permitir registrar productos en la plataforma.                                                                     |
| RF04 | El sistema debe permitir actualizar la información de los productos registrados por un seller.                                     |
| RF05 | El sistema debe permitir consultar los productos registrados por un seller.                                                        |
| RF06 | El sistema debe permitir agregar productos al carrito de compra.                                                                   |
| RF07 | El sistema debe permitir modificar las cantidades de productos del carrito.                                                        |
| RF08 | El sistema debe permitir eliminar productos del carrito de compra.                                                                 |
| RF09 | El sistema debe permitir generar un pedido a partir de los productos seleccionados en el carrito.                                  |
| RF10 | El sistema debe permitir consultar el detalle de un pedido realizado.                                                              |
| RF11 | El sistema debe permitir consultar los pedidos realizados y su estado.                                                             |
| RF12 | El sistema debe permitir procesar el pago de un pedido mediante una pasarela de pago externa.                                      |
| RF13 | El sistema debe permitir registrar sellers en la plataforma.                                                                       |
| RF14 | El sistema debe permitir actualizar la información de los sellers.                                                                 |
| RF15 | El sistema debe permitir desactivar sellers de la plataforma.                                                                      |
| RF16 | El sistema debe permitir consultar la información relacionada con las ventas de un seller.                                         |
| RF17 | El sistema debe permitir administrar las operaciones generales de la plataforma.                                                   |
| RF18 | El sistema debe permitir consultar información de disponibilidad y stock proporcionada por el ERP.                                 |
| RF19 | El sistema debe permitir gestionar la información relacionada con la entrega de los pedidos mediante un servicio externo de envío. |
| RF20 | El sistema debe permitir generar y consultar el comprobante de pago mediante un servicio de facturación.                           |

## 3. Relación entre historias de usuario y requisitos funcionales

| Historia de usuario                 | Requisitos funcionales relacionados |
| ----------------------------------- | ----------------------------------- |
| HU01 - Buscar y consultar productos | RF01, RF02                          |
| HU02 - Gestionar productos          | RF03, RF04, RF05                    |
| HU03 - Gestionar carrito            | RF06, RF07, RF08                    |
| HU04 - Realizar pedido              | RF09, RF10                          |
| HU05 - Gestionar sellers            | RF13, RF14, RF15                    |
| HU06 - Consultar pedidos            | RF10, RF11                          |
| HU07 - Realizar pago                | RF12                                |
| HU08 - Consultar ventas             | RF16                                |
| HU09 - Supervisar plataforma        | RF17                                |
| HU10 - Consultar disponibilidad     | RF02, RF18                          |
| HU11 - Consultar entrega            | RF19                                |
| HU12 - Obtener comprobante          | RF20                                |
