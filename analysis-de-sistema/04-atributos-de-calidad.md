# Atributos de calidad

## 1. Descripción

Los atributos de calidad representan las características que determinan cómo
debe comportarse el sistema bajo determinadas condiciones de operación.

Para el marketplace se consideran especialmente importantes el rendimiento,
la disponibilidad, la escalabilidad, la seguridad y la mantenibilidad.

## 2. Escenario de referencia

Durante una campaña comercial, el marketplace podría recibir una gran cantidad
de usuarios consultando productos, agregando productos al carrito y realizando
compras de manera simultánea.

Ante este escenario, la arquitectura debe considerar atributos de calidad que
permitan mantener un funcionamiento adecuado de la plataforma.

## 3. Atributos identificados

| ID   | Atributo de calidad | Escenario de calidad                                                                                                                                                        |
| ---- | ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AC01 | Rendimiento         | Las consultas de productos y operaciones del carrito deben responder en tiempos adecuados incluso cuando exista una alta cantidad de usuarios concurrentes.                 |
| AC02 | Disponibilidad      | El sistema debe permanecer disponible durante las campañas comerciales y permitir que los usuarios realicen sus operaciones principales.                                    |
| AC03 | Escalabilidad       | El sistema debe soportar un incremento de usuarios y solicitudes durante periodos de alta demanda sin afectar significativamente su funcionamiento.                         |
| AC04 | Seguridad           | Los datos de los usuarios, cuentas, pedidos y operaciones de compra deben estar protegidos frente a accesos no autorizados.                                                 |
| AC05 | Mantenibilidad      | La solución debe estar organizada en componentes con responsabilidades claramente definidas, facilitando la incorporación de cambios y correcciones.                        |
| AC06 | Interoperabilidad   | El sistema debe poder comunicarse con servicios externos como la pasarela de pago, el servicio de envío, el servicio de facturación y el ERP mediante interfaces definidas. |
| AC07 | Integridad de datos | La información relacionada con productos, stock, pedidos y pagos debe mantenerse consistente durante las operaciones del sistema.                                           |

## 4. Prioridad arquitectónica

Los atributos que tendrán mayor influencia inicial sobre las decisiones
arquitectónicas son:

- Rendimiento.
- Disponibilidad.
- Escalabilidad.
- Seguridad.
- Interoperabilidad.
- Integridad de datos.

Estos atributos serán considerados posteriormente al definir los componentes,
interfaces, mecanismos de comunicación y estrategia de despliegue del sistema.
