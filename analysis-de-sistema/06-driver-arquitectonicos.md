# Drivers arquitectónicos

## 1. Descripción

Los drivers arquitectónicos son los requisitos y restricciones que tienen una
influencia significativa sobre las decisiones relacionadas con la arquitectura
del sistema.

Estos drivers se obtienen principalmente a partir de los atributos de calidad
y las restricciones identificadas durante el análisis del sistema.

## 2. Drivers identificados

| ID   | Driver arquitectónico                                                                            | Origen                              | ¿Por qué influye en la arquitectura?                                                                                              |
| ---- | ------------------------------------------------------------------------------------------------ | ----------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| DA01 | El sistema debe soportar un incremento importante de usuarios durante campañas comerciales.      | AC03 - Escalabilidad                | Influye en la estrategia de escalamiento, distribución de carga y despliegue de los componentes del sistema.                      |
| DA02 | El sistema debe mantener tiempos de respuesta adecuados durante escenarios de alta concurrencia. | AC01 - Rendimiento                  | Influye en la comunicación entre componentes, procesamiento de solicitudes, acceso a datos y mecanismos de optimización.          |
| DA03 | El sistema debe mantener disponibilidad durante periodos de alta demanda.                        | AC02 - Disponibilidad               | Influye en la estrategia de despliegue, tolerancia a fallos y disponibilidad de los componentes críticos.                         |
| DA04 | El sistema debe proteger los datos de usuarios y operaciones de compra.                          | AC04 - Seguridad                    | Influye en los mecanismos de autenticación, autorización, protección de datos y comunicación segura.                              |
| DA05 | El sistema debe integrarse con una pasarela de pago externa mediante una API.                    | RC04 - Pasarela de pago             | Condiciona la forma de comunicación con el servicio externo y requiere definir mecanismos de integración y manejo de respuestas.  |
| DA06 | El sistema debe utilizar una API REST para la comunicación entre frontend y backend.             | RC03 - API REST                     | Limita las alternativas de comunicación entre las diferentes partes de la solución y condiciona el diseño de las interfaces.      |
| DA07 | El sistema debe integrarse con servicios externos de envío y facturación.                        | RC05, RC06 - Servicios externos     | Influye en la definición de interfaces, adaptadores y mecanismos para gestionar errores o indisponibilidad de servicios externos. |
| DA08 | El sistema debe obtener información de productos y stock desde un ERP externo.                   | RC07 - Integración con ERP          | Influye en la estrategia de integración, sincronización y consistencia de la información de productos y stock.                    |
| DA09 | El sistema debe mantener la consistencia de la información de pedidos, stock y pagos.            | AC07 - Integridad de datos          | Influye en la gestión de transacciones, persistencia y coordinación de las operaciones críticas del negocio.                      |
| DA10 | El sistema debe facilitar la incorporación de cambios y nuevas funcionalidades.                  | AC05 - Mantenibilidad               | Influye en la modularización del sistema, separación de responsabilidades y organización de los componentes.                      |
| DA11 | El sistema debe permitir la comunicación con diferentes servicios externos.                      | AC06 - Interoperabilidad            | Influye en el diseño de interfaces, contratos de comunicación y mecanismos de integración.                                        |
| DA12 | El sistema debe controlar el acceso según los roles de cliente, seller y administrador.          | RC08 - Autenticación y autorización | Influye en el diseño del mecanismo de autenticación, autorización y control de acceso a los recursos.                             |

## 3. Drivers prioritarios para el diseño

Los drivers que tendrán mayor impacto inicial en las decisiones arquitectónicas
son:

1. Escalabilidad ante incrementos de usuarios.
2. Rendimiento bajo alta concurrencia.
3. Seguridad de usuarios y operaciones.
4. Integración con servicios externos.
5. Integridad de pedidos, stock y pagos.
6. Mantenibilidad mediante separación de responsabilidades.

Estos drivers servirán como base para definir la arquitectura inicial del
marketplace y justificar las principales decisiones arquitectónicas.
