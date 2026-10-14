
# AlmaGest – Sistema de Gestión de Inventario

## 1. Descripción del sistema

AlmaGest es un sistema digital de gestión de inventario y almacén, diseñado para centralizar la información de los materiales y facilitar el control de sus movimientos.

El sistema contempla el registro de materiales, entradas, salidas, existencias disponibles, historial de movimientos y generación de reportes.

**Proyecto académico:** Ingeniería de Software I  
**Institución:** Universidad Abierta Para Adultos (UAPA)  
**Responsable:** Aneurys González  
**Estado:** Análisis, diseño y planificación técnica  
**Versión documental:** 0.1.0

## 2. Objetivo general

Diseñar y desarrollar un sistema digital que permita administrar eficientemente los materiales de un almacén, proporcionando herramientas para registrar movimientos, consultar existencias y generar información que facilite la toma de decisiones.

## 3. Problema que resuelve

El control manual del inventario mediante documentos físicos u hojas de cálculo puede provocar:

- Diferencias entre las existencias reales y las registradas.
- Errores durante el registro de entradas y salidas.
- Dificultades para consultar materiales disponibles.
- Falta de trazabilidad de los movimientos.
- Retrasos en la elaboración de reportes.

AlmaGest propone centralizar la información y automatizar los procesos principales del inventario.

## 4. Funcionalidades principales

| Módulo | Funcionalidad |
|---|---|
| Autenticación | Acceso mediante usuario y contraseña. |
| Usuarios y roles | Administración de permisos según el usuario. |
| Materiales | Registro, consulta, modificación y organización. |
| Entradas | Registro de materiales recibidos. |
| Salidas | Registro de materiales retirados. |
| Inventario | Consulta de existencias actualizadas. |
| Historial | Seguimiento de entradas y salidas. |
| Reportes | Generación de informes de inventario. |
| Validaciones | Prevención de cantidades incorrectas y existencias negativas. |

Estas funcionalidades están definidas como parte del alcance del proyecto. Su implementación completa permanece pendiente.

## 5. Arquitectura seleccionada

Se propone una arquitectura cliente-servidor organizada en tres capas:

### Capa de presentación

Responsable de mostrar las interfaces y permitir la interacción con los usuarios.

Incluye formularios, consultas, tablas, paneles y reportes.

### Capa de lógica de negocio

Responsable de ejecutar las reglas funcionales del inventario.

Incluye:

- Autenticación y autorización.
- Validación de entradas y salidas.
- Actualización de existencias.
- Procesamiento de movimientos.
- Generación de información para reportes.

### Capa de acceso a datos

Responsable de consultar, almacenar y actualizar la información persistente.

Gestionará datos de usuarios, roles, materiales, movimientos e inventario.

## 6. Organización del frontend

El frontend será la parte visible de AlmaGest y permitirá la interacción de los usuarios con el sistema.

Se organizará conceptualmente en:

- Inicio de sesión.
- Panel principal.
- Gestión de materiales.
- Registro de entradas.
- Registro de salidas.
- Consulta de inventario.
- Historial de movimientos.
- Reportes.
- Administración de usuarios.

El frontend enviará solicitudes al backend mediante una API HTTP.

## 7. Organización del backend

El backend será responsable de procesar las operaciones y garantizar el cumplimiento de las reglas del sistema.

Se organizará conceptualmente en:

- Controladores y rutas de API.
- Servicios de lógica de negocio.
- Módulo de autenticación.
- Gestión de usuarios y permisos.
- Gestión de materiales.
- Procesamiento de movimientos.
- Validación de existencias.
- Acceso a base de datos.
- Servicios de reportes.

La tecnología de implementación se definirá en una etapa posterior.

## 8. Comunicación entre frontend y backend

La comunicación propuesta seguirá este flujo:

1. El usuario realiza una acción desde la interfaz.
2. El frontend envía una solicitud HTTP al backend.
3. El backend valida los datos y permisos.
4. La lógica de negocio procesa la operación.
5. La capa de acceso a datos consulta o actualiza la base de datos.
6. El backend devuelve una respuesta al frontend.
7. La interfaz presenta el resultado al usuario.

Se propone utilizar una API REST con intercambio de información en formato JSON y comunicación segura mediante HTTPS.

## 9. Requisitos principales

### Requisitos funcionales

- RF-01: Registrar digitalmente movimientos de inventario.
- RF-02: Consultar las existencias actuales de materiales.
- RF-03: Registrar entradas y salidas con fecha, cantidad y responsable.
- RF-04: Consultar el historial de movimientos.
- RF-05: Generar reportes de inventario.

### Requisitos no funcionales

- RNF-01: Requerir autenticación de usuarios.
- RNF-02: Proporcionar una interfaz clara y fácil de utilizar.
- RNF-03: Responder a las consultas habituales de inventario en un máximo de tres segundos bajo condiciones normales de operación.

## 10. Herramientas utilizadas

| Herramienta | Propósito |
|---|---|
| GitHub | Repositorio y control de versiones. |
| GitHub Projects | Planificación y seguimiento Kanban. |
| GitHub Issues | Registro de tareas, requisitos y mejoras. |
| Visual Paradigm Online | Modelado UML. |
| Markdown | Documentación técnica del proyecto. |

## 11. Gestión del proyecto

Se utiliza un enfoque ágil basado en Kanban.

El tablero está organizado en:

1. Backlog.
2. Por hacer.
3. En progreso.
4. En revisión.
5. Finalizado.

Las tareas cuentan con prioridades, responsables, estados y fechas estimadas para facilitar su seguimiento.

**Repositorio:** https://github.com/agonzalez202006568/AlmaGest

## 12. Riesgos identificados

| Código | Riesgo | Acción preventiva |
|---|---|---|
| R-01 | Errores en la estructura de datos. | Revisar el modelo y realizar pruebas. |
| R-02 | Diferencias en las existencias. | Validar movimientos y cantidades. |
| R-03 | Retrasos en el desarrollo. | Priorizar tareas y revisar el tablero. |
| R-04 | Acceso no autorizado. | Implementar autenticación y permisos. |

## 13. Estado actual del proyecto

AlmaGest se encuentra en una etapa de documentación, diseño y planificación técnica.

### Avances documentados

- Identificación del problema y objetivo del sistema.
- Definición de funcionalidades y requisitos.
- Elaboración de historias de usuario.
- Creación de Issues en GitHub.
- Organización del tablero Kanban.
- Identificación de riesgos.
- Definición de arquitectura inicial.
- Elaboración de un modelo de casos de uso.

### Pendiente de implementación o verificación

- Desarrollo funcional del frontend.
- Desarrollo funcional del backend.
- Creación y conexión de la base de datos.
- Implementación de autenticación.
- Programación de entradas y salidas.
- Generación de reportes.
- Ejecución de pruebas funcionales.

## 14. Próximos pasos técnicos

1. Revisar y validar los modelos de datos y arquitectura.
2. Seleccionar el lenguaje de programación y las tecnologías.
3. Crear la estructura inicial de frontend y backend.
4. Implementar la base de datos.
5. Desarrollar los módulos prioritarios.
6. Realizar pruebas de funcionamiento.
7. Preparar una primera versión ejecutable.

## 15. Control de versiones

La documentación y los futuros archivos del sistema se administrarán mediante Git y GitHub.

Cada actualización relevante se registrará mediante un commit descriptivo, permitiendo identificar cambios y recuperar versiones anteriores.

La versión documental inicial del proyecto será **0.1.0**.

## 16. Responsable del proyecto

**Aneurys González**  
Ingeniería de Software I  
Universidad Abierta Para Adultos (UAPA)

Este repositorio forma parte del proyecto académico AlmaGest y documenta su planificación y evolución técnica.
