# Decisiones arquitectónicas

## 1. Descripción

Las decisiones arquitectónicas documentan las principales elecciones realizadas
durante el diseño de la arquitectura del Marketplace de Productos para
Mascotas.

Cada decisión se relaciona con uno o más drivers arquitectónicos previamente
identificados y presenta la justificación de la alternativa seleccionada.

## 2. Decisiones arquitectónicas

| ID      | Decisión arquitectónica                                | Driver relacionado                          | Justificación                                                                                                                                                                    | Resultado                                                          |
| ------- | ------------------------------------------------------ | ------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| ADR-001 | Monolito modular                                       | DA01 - Escalabilidad; DA06 - Mantenibilidad | Organizar las funcionalidades del marketplace en módulos independientes dentro de una misma aplicación desplegable, evitando inicialmente la complejidad de múltiples servicios. | Módulos de Usuarios, Sellers, Catálogo, Carrito, Pedidos y Pagos.  |
| ADR-002 | Clean Architecture                                     | DA06 - Mantenibilidad                       | Separar las reglas de negocio de los detalles tecnológicos para reducir el acoplamiento y facilitar la evolución del sistema.                                                    | Separación en Dominio, Aplicación, Infraestructura y Presentación. |
| ADR-003 | Estrategia de caché                                    | DA02 - Rendimiento                          | Reducir consultas repetitivas y mejorar los tiempos de respuesta para información consultada frecuentemente, especialmente productos y categorías.                               | Caché para información de consulta frecuente del catálogo.         |
| ADR-004 | Integración de pagos mediante interfaces y adaptadores | DA04 - Integración con pasarela de pago     | Desacoplar la lógica de negocio del proveedor específico de pagos, permitiendo cambiar o integrar diferentes proveedores sin modificar los casos de uso principales.             | Contrato de pagos y adaptador para la pasarela externa.            |

## 3. Justificación de las decisiones

### ADR-001: Monolito modular

Se selecciona un enfoque de **monolito modular** para organizar el sistema en
módulos funcionalmente independientes dentro de una única aplicación
desplegable.

Esta decisión permite mantener una arquitectura organizada y modular sin
introducir inicialmente la complejidad operacional asociada a una arquitectura
de microservicios.

Los principales módulos serán:

- Usuarios
- Sellers
- Catálogo
- Carrito
- Pedidos
- Pagos

Esta decisión se relaciona principalmente con la necesidad de mantener una
estructura modular y permitir que el sistema pueda evolucionar conforme
aumenten sus funcionalidades y usuarios.

### ADR-002: Clean Architecture

Se utilizará **Clean Architecture** como criterio de organización interna de
los módulos para separar las reglas de negocio de los detalles tecnológicos.

La estructura propuesta considera:

- **Dominio:** entidades y reglas principales del negocio.
- **Aplicación:** casos de uso y coordinación de las operaciones.
- **Infraestructura:** persistencia, APIs externas y otros servicios
  tecnológicos.
- **Presentación:** API REST y mecanismos de interacción con el usuario.

Esta decisión favorece la mantenibilidad y reduce las dependencias directas
entre las reglas de negocio y las tecnologías utilizadas.

### ADR-003: Estrategia de caché

Se incorporará una estrategia de **caché** para reducir consultas repetitivas
sobre información que no cambia constantemente.

El principal caso de aplicación será el catálogo de productos y otra
información de consulta frecuente.

Esta decisión busca mejorar el rendimiento del sistema cuando exista una alta
cantidad de solicitudes concurrentes, especialmente durante campañas
comerciales.

### ADR-004: Integración de pagos mediante interfaces y adaptadores

La integración con la pasarela de pago se realizará mediante una interfaz o
contrato definido por la aplicación y un adaptador encargado de comunicarse
con el proveedor externo.

De esta manera, los casos de uso relacionados con pedidos y pagos no
dependerán directamente de una implementación específica de la pasarela.

La estructura conceptual será:

```text
Caso de uso de pago
        │
        ▼
Interfaz de pago
        │
        ▼
Adaptador de pasarela
        │
        ▼
Pasarela de pago externa
```
