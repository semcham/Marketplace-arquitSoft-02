# Restricciones del sistema

## 1. Descripción

Las restricciones representan condiciones técnicas, tecnológicas o externas
que limitan las alternativas disponibles para el diseño y construcción de
la arquitectura del marketplace.

## 2. Restricciones identificadas

| ID   | Restricción                     | Descripción                                                                                                                                                          |
| ---- | ------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| RC01 | Aplicación web                  | El sistema debe desarrollarse como una aplicación web accesible mediante un navegador.                                                                               |
| RC02 | Control de versiones            | El código fuente debe gestionarse mediante Git y mantenerse en un repositorio compartido.                                                                            |
| RC03 | API REST                        | La comunicación entre el frontend y los servicios del sistema debe realizarse mediante una API REST.                                                                 |
| RC04 | Pasarela de pago                | El sistema debe integrarse con una pasarela de pago externa para procesar las operaciones de pago.                                                                   |
| RC05 | Servicio de envío               | El sistema debe integrarse con un servicio externo de envío para gestionar la información relacionada con la entrega de pedidos.                                     |
| RC06 | Servicio de facturación         | El sistema debe integrarse con un servicio externo de facturación para generar los comprobantes de pago.                                                             |
| RC07 | Integración con ERP             | El sistema debe obtener información de productos y stock mediante la integración con un ERP externo.                                                                 |
| RC08 | Autenticación y autorización    | El sistema debe controlar el acceso de los usuarios según los roles y permisos definidos.                                                                            |
| RC09 | Persistencia de información     | El sistema debe utilizar un mecanismo de almacenamiento persistente para gestionar productos, usuarios, carritos, pedidos y demás información del negocio.           |
| RC10 | Integración mediante interfaces | Las integraciones con servicios externos deben realizarse mediante interfaces y protocolos compatibles con los servicios proporcionados.                             |
| RC11 | Separación de responsabilidades | La solución debe organizar sus componentes de manera que las responsabilidades principales del sistema se encuentren claramente separadas.                           |
| RC12 | Desarrollo académico            | El sistema se desarrollará como un proyecto académico, por lo que las tecnologías y servicios utilizados deben ser viables para el entorno de desarrollo disponible. |
