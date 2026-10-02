# Drivers arquitectónicos

## 1. Descripción

Los drivers arquitectónicos son los requisitos y restricciones que tienen una
influencia significativa sobre las decisiones relacionadas con la arquitectura
del sistema.

Estos drivers se obtienen principalmente a partir de los atributos de calidad
y las restricciones identificadas durante el análisis del sistema.

## 2. Drivers identificados

| ID   | Driver arquitectónico                                                                            | Origen                  | ¿Por qué influye en la arquitectura?                                                                     |
| ---- | ------------------------------------------------------------------------------------------------ | ----------------------- | -------------------------------------------------------------------------------------------------------- |
| DA01 | El sistema debe soportar un incremento importante de usuarios durante campañas comerciales.      | AC03 - Escalabilidad    | Influye en la estrategia de escalamiento y en la forma en que se despliegan los componentes del sistema. |
| DA02 | El sistema debe mantener tiempos de respuesta adecuados durante escenarios de alta concurrencia. | AC01 - Rendimiento      | Influye en la comunicación entre componentes, el procesamiento de solicitudes y el acceso a los datos.   |
| DA03 | El sistema debe proteger los datos de los usuarios y las operaciones de compra.                  | AC04 - Seguridad        | Influye en los mecanismos de autenticación, autorización, protección de datos y comunicación segura.     |
| DA04 | El sistema debe integrarse con una pasarela de pago externa mediante una API.                    | RC04 - Pasarela de pago | Condiciona la forma de comunicación e integración con servicios externos y el manejo de sus respuestas.  |
| DA05 | El sistema debe utilizar una API REST para la comunicación entre el frontend y el backend.       | RC03 - API REST         | Condiciona la comunicación entre las diferentes partes del sistema y la definición de sus interfaces.    |
| DA06 | El sistema debe permitir modificar funcionalidades sin afectar innecesariamente otros módulos.   | AC05 - Mantenibilidad   | Influye en la separación de responsabilidades, modularidad y dependencias internas del sistema.          |

## 3. Relación con los atributos de calidad y restricciones

Los drivers arquitectónicos seleccionados se relacionan con los principales
atributos de calidad y restricciones identificados durante el análisis:

| Driver                                  | Elemento de origen      |
| --------------------------------------- | ----------------------- |
| DA01 - Escalabilidad                    | AC03 - Escalabilidad    |
| DA02 - Rendimiento                      | AC01 - Rendimiento      |
| DA03 - Seguridad                        | AC04 - Seguridad        |
| DA04 - Integración con pasarela de pago | RC04 - Pasarela de pago |
| DA05 - API REST                         | RC03 - API REST         |
| DA06 - Mantenibilidad                   | AC05 - Mantenibilidad   |

## 4. Influencia en la arquitectura

Los drivers identificados serán utilizados como referencia para definir la
arquitectura inicial del marketplace.

En particular:

- **DA01 - Escalabilidad:** orientará las decisiones relacionadas con el
  crecimiento de usuarios y solicitudes durante campañas comerciales.
- **DA02 - Rendimiento:** orientará las decisiones relacionadas con el
  procesamiento de solicitudes y acceso a los datos.
- **DA03 - Seguridad:** orientará las decisiones relacionadas con el control
  de acceso y protección de la información.
- **DA04 - Pasarela de pago:** orientará el mecanismo de integración con el
  servicio externo de pagos.
- **DA05 - API REST:** establecerá el mecanismo de comunicación entre la
  aplicación web y la lógica de negocio.
- **DA06 - Mantenibilidad:** orientará la separación de responsabilidades,
  modularidad y control de dependencias entre los componentes.

Estos drivers constituyen la base para justificar las principales decisiones
de la arquitectura inicial del Marketplace de Productos para Mascotas.
