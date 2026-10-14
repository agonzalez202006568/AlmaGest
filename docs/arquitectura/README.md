
# Arquitectura de Software – AlmaGest

## 1. Descripción general

AlmaGest es un sistema de gestión de inventario
concebido como una aplicación web.

Se propone una arquitectura cliente-servidor
organizada en tres capas:

1. Presentación.
2. Lógica de negocio.
3. Acceso a datos.

Esta organización busca facilitar el mantenimiento,
la seguridad, la escalabilidad y la separación
de responsabilidades.

## 2. Arquitectura seleccionada

### Capa de presentación (Frontend)

Es la parte del sistema con la que interactúan
directamente los usuarios.

Responsabilidades:

- Mostrar la interfaz de inicio de sesión.
- Presentar el catálogo de materiales.
- Facilitar el registro de entradas y salidas.
- Consultar las existencias disponibles.
- Mostrar el historial de movimientos.
- Presentar los reportes de inventario.
- Mostrar mensajes de validación y errores.

### Capa de lógica de negocio (Backend)

Procesa las solicitudes recibidas desde el frontend
y aplica las reglas funcionales de AlmaGest.

Responsabilidades:

- Autenticar y autorizar usuarios.
- Administrar materiales.
- Procesar entradas y salidas.
- Validar cantidades y existencias.
- Evitar salidas superiores al inventario disponible.
- Registrar movimientos.
- Generar información para reportes.

### Capa de acceso a datos

Gestiona la comunicación con la base de datos.

Responsabilidades:

- Consultar registros.
- Almacenar nuevos materiales.
- Actualizar existencias.
- Registrar entradas y salidas.
- Recuperar el historial de movimientos.
- Mantener la integridad de los datos.

## 3. Organización propuesta del frontend

El frontend podrá organizarse en:

- Componentes reutilizables.
- Páginas o vistas.
- Formularios.
- Servicios para consumir la API.
- Gestión de autenticación.
- Validación básica de formularios.

### Módulos previstos

1. Inicio de sesión.
2. Panel principal.
3. Gestión de materiales.
4. Entradas y salidas.
5. Consulta de inventario.
6. Historial.
7. Reportes.
8. Administración de usuarios.

## 4. Organización propuesta del backend

El backend podrá organizarse en:

- Rutas y controladores.
- Servicios de negocio.
- Modelos de datos.
- Acceso a base de datos.
- Autenticación y autorización.
- Validaciones.
- Gestión de errores.
- Generación de reportes.

Cada componente deberá contar con
responsabilidades claramente definidas.

## 5. Comunicación entre frontend y backend

Se propone utilizar una API REST mediante HTTP/HTTPS.

El intercambio de información se realizará
principalmente en formato JSON.

### Flujo de funcionamiento

1. El usuario interactúa con una pantalla.
2. El frontend prepara y envía una solicitud.
3. El backend recibe y valida los datos.
4. Se verifican los permisos del usuario.
5. La lógica de negocio procesa la operación.
6. La capa de datos consulta o actualiza registros.
7. El backend devuelve una respuesta.
8. El frontend presenta el resultado.

### Ejemplo: salida de materiales

Un encargado solicita retirar 5 unidades
de un material.

El frontend envía la solicitud al backend.

El backend comprueba que:

- El usuario tiene autorización.
- El material existe.
- La cantidad solicitada es válida.
- Hay existencias suficientes.

Si las condiciones se cumplen, el sistema
registra el movimiento y actualiza las existencias
mediante una operación transaccional.

Si no se cumplen, rechaza la operación
y devuelve un mensaje explicativo.

## 6. Base de datos

Se propone una base de datos relacional
con las siguientes entidades principales:

- Usuarios.
- Roles.
- Permisos.
- Materiales.
- Movimientos.
- Detalles de movimientos.

La estructura definitiva será validada
durante el diseño de la base de datos.

## 7. Seguridad

La arquitectura deberá contemplar:

- Autenticación de usuarios.
- Control de acceso basado en roles.
- Comunicación mediante HTTPS.
- Validación de datos en el backend.
- Almacenamiento seguro de contraseñas.
- Prevención de modificaciones no autorizadas.
- Registro de operaciones relevantes.

## 8. Tecnologías y herramientas

### Herramientas utilizadas

- Git.
- GitHub.
- GitHub Projects.
- GitHub Issues.
- Visual Paradigm Online.
- Markdown.

### Tecnologías pendientes de selección

- Framework de frontend.
- Lenguaje y framework de backend.
- Motor de base de datos.
- Infraestructura de alojamiento.

Estas tecnologías serán seleccionadas
en una etapa posterior.

## 9. Estado de la arquitectura

La arquitectura se encuentra definida
a nivel conceptual y documental.

La implementación funcional del frontend,
backend y base de datos continúa pendiente.

## 10. Próximos pasos

1. Validar la arquitectura propuesta.
2. Seleccionar las tecnologías.
3. Diseñar el modelo de datos definitivo.
4. Crear la estructura inicial del código.
5. Implementar los módulos prioritarios.
6. Realizar pruebas de integración y seguridad.
