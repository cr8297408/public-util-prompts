# 🏋️‍♂️ Requerimientos de Software – GymVision

## 1.1. Propósito 🎯

El propósito de GymVision es proporcionar una solución tecnológica integral que permita a gimnasios y centros deportivos de cualquier tamaño gestionar de manera eficiente y centralizada todos los aspectos operativos, administrativos y de interacción con sus clientes. El sistema busca optimizar procesos clave como la administración de usuarios y membresías, el control financiero, la gestión de inventario, la planificación de clases y entrenamientos, la comunicación interna y externa, y la mejora continua de la experiencia del usuario, todo ello mediante herramientas digitales intuitivas, seguras y escalables.

### 1.2. Alcance 🗺️

GymVision abarcará la digitalización y automatización de los procesos principales de un gimnasio, incluyendo:

    Registro y administración de usuarios, membresías y cobros (incluyendo suscripciones y pagos recurrentes).

    Gestión de inventario, novedades, daños y compras de insumos.

    Manejo de nóminas y control de personal.

    Control de acceso mediante código QR o biometría.

    Paneles de métricas y reportes sobre asistencia, ingresos, retención y desempeño.

    Gestión de entrenadores, horarios y reservas de clases.

    Seguimiento del progreso físico de los usuarios.

    Tienda en línea para venta de productos y servicios.

    Notificaciones automáticas y personalizadas (push, email, etc.).

    Integración con pasarelas de pago.

    Espacios de comunidad y comunicación interna (foros, encuestas, anuncios).

    Módulo de mantenimiento de equipos.

    Soporte para la administración de múltiples sucursales desde una sola plataforma.

El sistema está diseñado para ser modular y escalable, permitiendo su adaptación a las necesidades específicas de cada gimnasio y facilitando la integración con otras plataformas o servicios externos en el futuro.

### 1.3. Referencias 🔗

    Normativas locales e internacionales de protección de datos (por ejemplo, GDPR).

    Estándares de seguridad de la información (ISO/IEC 27001).

    Buenas prácticas de desarrollo ágil y DevOps.

    Documentación técnica de APIs de pasarelas de pago compatibles.

## 2. Descripción General 🖼️

### 2.1 Perspectiva del Producto 🏢

GymVision se presenta como una solución SaaS (Software como Servicio) accesible a través de navegadores web y dispositivos móviles. Está compuesta por múltiples módulos interconectados que permiten una gestión integral de las operaciones de gimnasios y centros deportivos. Su arquitectura modular facilita la implementación escalonada y la personalización según las necesidades específicas de cada cliente.

### 2.2 Funcionalidad General 🚀

    Gestión de Usuarios y Membresías: Registro, actualización y seguimiento de clientes, incluyendo planes de membresía y pagos recurrentes.

    Control de Inventario: Administración de equipos, suplementos y otros productos, con seguimiento de existencias, novedades y daños.

    Gestión de Nóminas: Registro y control de pagos al personal, incluyendo entrenadores y administrativos.

    Control de Acceso: Implementación de sistemas de autenticación mediante códigos QR o biometría para socios.

    Panel de Métricas y Reportes: Visualización de estadísticas clave como asistencia, ingresos y retención de clientes.

    Gestión de Clases y Entrenadores: Programación de clases grupales y personalizadas, asignación de entrenadores y seguimiento de horarios.

    Seguimiento del Progreso Físico: Registro de rutinas, medidas corporales y logros de los usuarios.

    Tienda en Línea: Venta de productos y servicios adicionales, con integración de pasarelas de pago.

    Notificaciones: Envío de recordatorios y comunicaciones relevantes a través de notificaciones push y correos electrónicos.

    Comunidad Interna: Espacios para interacción entre usuarios y entrenadores, incluyendo foros y encuestas.

    Mantenimiento de Equipos: Registro y seguimiento de mantenimientos preventivos y correctivos.

    Gestión Multisucursal: Administración centralizada de múltiples sucursales bajo una misma plataforma.

### 2.3 Características de los Usuarios 👥

    Dueños de Gimnasio: Acceso completo a todas las funcionalidades, incluyendo la gestión de múltiples sucursales, visualización de métricas globales y administración de personal.

    Administradores de Sucursal: Gestión de usuarios, membresías, inventario y personal dentro de su sucursal específica.

    Entrenadores: Visualización de agendas, programación de clases y seguimiento del progreso de los clientes asignados.

    Clientes: Acceso a su perfil personal, incluyendo información de membresía, programación de clases, seguimiento de progreso y opciones de pago.

### 2.4 Restricciones Generales 🚧

    Compatibilidad: El sistema debe ser compatible con los principales navegadores web y sistemas operativos móviles.

    Seguridad: Implementación de medidas de seguridad para proteger la información sensible de los usuarios.

    Escalabilidad: Capacidad para adaptarse al crecimiento en número de usuarios y sucursales sin comprometer el rendimiento.

## 3. Requerimientos funcionales ✅

### RF-01: Registro de gimnasios 📝

- **Descripción:** En la pantalla principal de auth los gimnasios podrán registrarse bajo el nombre del mismo y los datos del dueño del gimnasio
- **Prioridad:** Alta
- **Criterios de aceptación:** Se debe poder registrar el gimnasio, crear su sucursal principal y un perfil para el administrador con los datos proporcionados
- **Dependencias:** Ninguna

### RF-02: Inicio de sesión 📝

- **Descripción:** Los usuarios pueden iniciar sesión en el aplicativo con su correo electronico y contraseña
- **Prioridad:** Alta
- **Criterios de aceptación:** Se debe poder iniciar sesión con el correo electronico y la contraseña, además de que se debe redirigir al usuario al dashboard correspondiente
- **Dependencias:** RF-01

### RF-03: Registro de sucursales 📝

- **Descripción:** Los dueños de un gimnasio pueden registrar sus nuevas sucursales en el aplicativo
- **Prioridad:** Alta
- **Criterios de aceptación:** Se debe poder registrar nuevas sucursales y asignar administradores a ella o invitarlos via correo electronico
- **Dependencias:** RF-02

### RF-04: Registro de clientes 📝

- **Descripción:** Los administradores de una sucursal pueden registrar sus nuevos clientes en el aplicativo
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder registrar el cliente, crear su membresía y un perfil para el cliente con los datos proporcionados
- **Dependencias:** RF-03

### RF-05: Registro de administradores 📝

- **Descripción:** Los dueños de un gimnasio pueden registrar sus nuevos administradores en el aplicativo
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder registrar el administrador, crear su perfil y un perfil para el administrador con los datos proporcionados
- **Dependencias:** RF-02

### RF-06: Registro de entrenadores 📝

- **Descripción:** Los dueños de un gimnasio y los administradores de una sucursal pueden registrar sus nuevos entrenadores en el aplicativo
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder registrar el entrenador, crear su perfil y un perfil para el entrenador con los datos proporcionados
- **Dependencias:** RF-02

### RF-07: Registro de inventario 📝

- **Descripción:** Los dueños de un gimnasio y los administradores de una sucursal pueden registrar sus nuevos productos en el inventario, mancuernas, barras, discos, maquinas etc
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder registrar el producto y la cantidad del mismo que se tiene
- **Dependencias:** RF-02

### RF-08: Registro de novedades 📝

- **Descripción:** Los dueños de un gimnasio y los administradores de una sucursal pueden registrar sus nuevas novedades en el inventario, mancuernas, barras, discos, maquinas etc
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder registrar la novedad permitiendo disminuir la cantidad en caso de daño o perdida y aumentar en caso de ingreso de stock
- **Dependencias:** RF-02

### RF-09: Registro de daños 📝

- **Descripción:** Los dueños de un gimnasio y los administradores de una sucursal pueden registrar daños generales en el gimnasio, como daños en el suelo, daños en los equipos no inventariados, daños en los espejos eetc
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder registrar el daño y las razones, además de una fotografia del mismo
- **Dependencias:** RF-02

### RF-10: Registro de inventario de tipo venta📝

- **Descripción:** Los dueños del gimnasio y administradores pueden crear productos de tipo venta, como por ejemplo suplementos, ropa, lociones, guantes etc. registrando además el precio de venta y el costo del mismo, además de la cantidad que se tiene
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder registrar el producto, la cantidad del mismo que se tiene y el precio de venta y el costo del mismo
- **Dependencias:** RF-02

### RF-11: Registro de gastos generales 📝

- **Descripción:** Los dueños de un gimnasio y los administradores de una sucursal pueden registrar sus gastos generales, como por ejemplo electricidad, agua, internet, alquiler, etc
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder registrar el gasto, la cantidad del mismo que se tiene y el precio de venta y el costo del mismo
- **Dependencias:** RF-02

### RF-12: Registro de nóminas 📝

- **Descripción:** Los dueños de un gimnasio y los administradores de una sucursal pueden registrar las nominas que deben pagar a sus empleados, seleccionando el usuario y el monto que se le debe pagar además de la periocidad
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder registrar la nómina, el usuario, el monto y la periocidad y además de esto poder añadir observaciones para llevar un seguimiento mes a mes de lo que se paga a sus empleados
- **Dependencias:** RF-02

### RF-13 Registro de gastos generales 📝

- **Descripción:** Los dueños de un gimnasio y los administradores de una sucursal pueden registrar sus gastos generales, como por ejemplo electricidad, agua, internet, alquiler, etc
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder registrar el gasto, la cantidad del mismo que se tiene y el precio de venta y el costo del mismo
- **Dependencias:** RF-02

### RF-14: Creación de clases grupales 📝

- **Descripción:** Los dueños de un gimnasio los administradores de una sucursal y los entrenadores pueden crear nuevas clases grupales, seleccionando el entrenador, el horario y el tipo de clase
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder crear la clase grupales, el entrenador, el horario y el tipo de clase
- **Dependencias:** RF-02

### RF-15: Reserva de clases personalizadas 📝

- **Descripción:** Los clientes pueden reservar clases personalizadas, seleccionando el entrenador, el horario y el tipo de clase
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder reservar la clase personalizada, el entrenador, el horario y el tipo de clase
- **Dependencias:** RF-02

### RF-16 Aprobación de clases personalizadas 📝

- **Descripción:** Los dueños de un gimnasio, los administradores de una sucursal y los entrenadores pueden aprobar las clases personalizadas, seleccionando el cliente, el entrenador, el horario y el tipo de clase
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder aprobar la clase personalizada, el cliente, el entrenador, el horario y el tipo de clase
- **Dependencias:** RF-15

### RF-17: Cancelación de clases personalizadas 📝

- **Descripción:** Los dueños de un gimnasio, los administradores de una sucursal y los entrenadores pueden cancelar las clases personalizadas, seleccionando la clase a cancelar
- **Prioridad:** Media
- **Criterios de aceptación:** Se debe poder cancelar la clase personalizada con un minimo de 12 horas de anticipación
- **Dependencias:** RF-15, RF-16

---

## 4. Requerimientos no funcionales 🚀

### RNF-01: Rendimiento ⚡  

- **Descripción:**  
  El sistema debe responder en menos de 2 segundos para el 95% de las solicitudes bajo condiciones de carga estándar.

- **Criterios de aceptación:**  
  - El 95% de las respuestas a través de la API de Supabase deben completarse en ≤ 2000 ms, medido mediante herramientas de monitoreo o el SDK de Supabase.  
  - Las consultas a la base de datos deben estar optimizadas e indexadas correctamente.  
  - Las funciones RPC deben ejecutarse en menos de 500 ms en condiciones normales.  
  - Se debe monitorear el rendimiento usando herramientas como Supabase Studio, Logs, o APM externo si se integra.

### RNF-02: Seguridad 🔒  

- **Descripción:**  
  Todos los datos sensibles del usuario deben cifrarse tanto en tránsito como en reposo. El acceso a la información debe estar controlado rigurosamente mediante políticas.

- **Criterios de aceptación:**  
  - Toda la comunicación con Supabase debe realizarse a través de HTTPS (TLS 1.2+).  
  - Supabase debe tener habilitado el cifrado en reposo en su base de datos.  
  - Se deben definir y aplicar políticas de seguridad de nivel de fila (RLS) en todas las tablas con datos sensibles.  
  - Se debe utilizar Supabase Auth para autenticación segura con al menos un proveedor robusto (OAuth, email/password con verificación).  
  - Los tokens deben manejarse de forma segura en el cliente (preferentemente memoria o cookies HTTP-only).

### RNF-03: Usabilidad 🖱️  

- **Descripción:**  
  La interfaz debe ser intuitiva, accesible y permitir que usuarios sin experiencia técnica puedan operar el sistema fácilmente.

- **Criterios de aceptación:**  
  - Cumplimiento del estándar WCAG 2.1 nivel AA (contrastes, navegación por teclado, etiquetas).  
  - Pruebas de usabilidad realizadas con usuarios reales no técnicos.  
  - Los flujos de uso deben requerir un número mínimo de pasos (ej. login en ≤ 3 pasos).  
  - Deben aplicarse evaluaciones heurísticas de usabilidad y solucionarse problemas críticos detectados.

### RNF-04: Mantenibilidad 🛠️  

- **Descripción:**  
  El sistema debe ser fácil de mantener, escalar y extender. Todo el código y configuración deben estar versionados y seguir estándares del sector.

- **Criterios de aceptación:**  
  - Uso de `supabase db` y migraciones versionadas para políticas, funciones y estructura de la base de datos.  
  - Uso de linters, formateadores automáticos y convenciones de codificación aplicadas por CI.  
  - Cobertura de pruebas unitarias mínima del 80% en frontend y funciones personalizadas.  
  - Toda nueva funcionalidad debe incluir documentación técnica (README, comentarios, ADRs si aplica).  
  - Separación clara de responsabilidades en capas (frontend, lógica de negocio RPC, reglas RLS).

### RNF-05: Portabilidad 🌐  

- **Descripción:**  
  El sistema debe funcionar correctamente en todos los navegadores web modernos, tanto en escritorio como en dispositivos móviles.

- **Criterios de aceptación:**  
  - Soporte garantizado para las dos últimas versiones de Chrome, Firefox, Safari y Edge.  
  - Pruebas de compatibilidad realizadas en BrowserStack o herramientas similares.  
  - Diseño adaptable (responsive) para diferentes tamaños de pantalla.  
  - Evitar uso de APIs obsoletas o incompatibles con navegadores soportados.

### RNF-06: Dependencia de terceros 🔌  

- **Descripción:**  
  El sistema debe manejar de forma resiliente su dependencia con Supabase, previendo caídas o errores temporales del servicio.

- **Criterios de aceptación:**  
  - Mecanismos de retry en operaciones críticas (login, carga de datos esenciales).  
  - Visualización clara de estados de carga, error y éxito en la interfaz.  
  - Logging y monitoreo de errores de red o API mediante herramientas como Sentry o LogRocket.  
  - La lógica del cliente debe estar desacoplada de Supabase en lo posible (abstracción de servicios).

### RNF-07: Estructura Modular y Arquitectura de Código 🧩

- **Descripción:**  
La solución debe estar construida bajo una arquitectura limpia y modular, garantizando una alta cohesión y bajo acoplamiento entre los componentes, lo cual facilita el mantenimiento, pruebas, reutilización y escalabilidad.

- **Criterios de aceptación:**  

Frontend:

Implementación de Atomic Design para la organización de componentes (átomos, moléculas, organismos, plantillas y páginas).

Cada componente debe ser autocontenible, testeable y con responsabilidades claras.

Los archivos de componentes deben mantenerse cortos (<300 líneas) y divididos si es necesario.

Separación de lógica de negocio (hooks personalizados, contextos) de la presentación.

Uso de feature folders para agrupar funcionalidades por dominio.

Backend (Supabase):

Separación clara entre lógica de negocio (funciones RPC), reglas de acceso (RLS), y estructura de datos (migraciones).

Todos los objetos versionados mediante supabase db.

Las funciones deben ser pequeñas y realizar una única tarea.

Documentación y Tests:

Cada componente, función RPC y módulo debe incluir documentación técnica clara (README, comentarios, ADRs si aplica).

Se debe mantener documentación centralizada y accesible (idealmente en formato Markdown y alojada en un portal de documentación como Docusaurus o similar).

Deben existir pruebas unitarias y de integración con al menos un 80% de cobertura para cada módulo.

Los tests deben automatizarse mediante pipelines CI/CD usando frameworks como Vitest, Testing Library o Jest para frontend, y PostgREST o pruebas RPC para backend.

Buenas prácticas del sector:

Uso de convenciones como conventional commits, integración continua (CI), revisiones de código obligatorias.

Linting y formateo automático obligatorio (ESLint, Prettier) en cada push.

Tipado estricto usando TypeScript en todo el stack frontend y validación de esquemas en backend (zod, ajv o similar).
