# Requerimientos No Funcionales

## Rendimiento

- **RNF-REN-1:** El sistema debe responder en menos de 1.5 segundos en el servidor para el 95% de las peticiones web de carga de tableros de resumen clínico.
- **RNF-REN-2:** El sistema debe procesar y subir en segundo plano los archivos adjuntos que superen los 5 MB, evitando bloqueos en el hilo principal.
- **RNF-REN-3:** El sistema debe resolver las consultas de búsqueda del historial con filtros múltiples en menos de 500 ms.

## Seguridad

- **RNF-SEG-1:** El sistema debe cifrar obligatoriamente las contraseñas en la base de datos mediante `Bcrypt` o `Argon2` provistos por Laravel.
- **RNF-SEG-2:** El sistema debe implementar por defecto los middlewares de protección de Laravel contra CSRF, XSS y SQL Injection (utilizando Eloquent ORM).
- **RNF-SEG-3:** El sistema debe limitar a un máximo de 5 intentos fallidos por minuto los accesos a endpoints críticos (como inicio de sesión y recuperación de contraseña) para prevenir ataques de fuerza bruta.
- **RNF-SEG-4:** El sistema debe expirar las sesiones web tras un tiempo de inactividad de 60 minutos, requiriendo que el usuario vuelva a autenticarse.

## Usabilidad

- **RNF-USA-1:** El sistema debe ofrecer una interfaz de usuario responsiva y mobile-first (resolución mínima de 360px × 780px) y también en pantallas Full HD (1920px × 1080px).
- **RNF-USA-2:** El sistema debe procesar las interacciones con los tableros clínicos, filtros y formularios de registro de forma asíncrona mediante Livewire, evitando recargas completas de la página.

## Escalabilidad y Mantenibilidad

- **RNF-ESC-1:** El sistema debe estructurar su código backend (PHP 8.4 / Laravel 12) respetando una arquitectura en capas, organizando controladores para la presentación, FormRequests para validaciones, Actions/Services para la lógica de negocio y Repositorios o modelos Eloquent puros para el acceso a datos.
- **RNF-ESC-2:** El sistema debe ejecutar de forma asíncrona mediante colas tareas como el envío de correos, la generación de PDFs complejos y el procesamiento masivo de imágenes.
- **RNF-ESC-3:** El sistema debe requerir type hinting estricto y return types obligatorios en todo el código fuente de PHP 8.4 para asegurar la mantenibilidad y calidad del código.

## Compatibilidad e Interoperabilidad

- **RNF-COM-1:** El sistema debe garantizar la compatibilidad web con las últimas versiones estables de los navegadores Google Chrome, Mozilla Firefox, Apple Safari y Microsoft Edge.
- **RNF-COM-2:** El sistema debe permitir la exportación del historial clínico tanto en formato PDF amigable para lectura humana como en formato JSON estándar para garantizar la portabilidad de datos hacia otros sistemas.

## Disponibilidad y Confiabilidad

- **RNF-DIS-1:** El sistema debe realizar respaldos automatizados diarios de la base de datos (PostgreSQL) y del almacenamiento de archivos, conservándolos en un almacenamiento externo durante un mínimo de 30 días.

## Arquitectura y Despliegue

- **RNF-ARQ-1:** El sistema debe operar y mantenerse en tres entornos de ejecución estrictamente aislados: Desarrollo, Pre-Producción y Producción.
- **RNF-ARQ-2:** El sistema debe automatizar el proceso de despliegue continuo (CI/CD) a producción, requiriendo la aprobación previa y obligatoria de las suites de pruebas unitarias y de integración (Laravel Pest/PHPUnit).

## Privacidad

- **RNF-PRI-1:** El sistema debe registrar y estampar de forma inmutable cada evento médico insertado, almacenando un historial de versiones (mediante logs de cambios o event sourcing simplificado) para la auditoría de cualquier edición o eliminación lógica.
- **RNF-PRI-2:** El sistema debe registrar de forma explícita cada acción de compartición de registros, detallando el autor, el destinatario y la fecha, permitiendo la revocación instantánea del acceso.
- **RNF-PRI-3:** El sistema debe garantizar el aislamiento de la información médica, impidiendo que usuarios y veterinarios accedan directa o indirectamente a registros clínicos de mascotas no vinculadas, mediante la validación obligatoria del `owner_id` o las invitaciones de acceso.
