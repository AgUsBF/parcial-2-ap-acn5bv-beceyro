# Requerimientos Funcionales

- **RF1:** El sistema debe permitir el registro de usuarios mediante email y contraseña, validando la unicidad del correo y requiriendo la confirmación obligatoria del correo electrónico para habilitar la cuenta.
- **RF2:** El sistema debe permitir el inicio y cierre de sesión de forma segura, incluyendo la recuperación y el restablecimiento de contraseñas.
- **RF3:** El sistema debe permitir al usuario crear, editar y eliminar mascotas asociadas a su cuenta, soportando la estandarización de imágenes, y la selección de especies y razas a partir de un catálogo maestro.
- **RF4:** El sistema debe permitir el registro de eventos clínicos clasificados por tipo (consulta, vacuna, cirugía, etc.), aplicando una validación estricta a los archivos adjuntos (permitiendo únicamente PDF e imágenes con un tamaño máximo establecido).
- **RF5:** El sistema debe registrar los eventos clínicos con marcas de tiempo inmutables de creación y última modificación, manteniendo un registro de auditoría con detalles del autor, la fecha y la hora.
- **RF6:** El sistema debe permitir al propietario compartir los registros de sus mascotas con veterinarios, definiendo el nivel de acceso (Solo Lectura o Lectura/Escritura) y configurando fechas de expiración para dicho acceso.
- **RF7:** El sistema debe permitir a los veterinarios aceptar invitaciones y acceder a un Portal Médico que muestre únicamente las mascotas a las que se les otorgó acceso, garantizando el aislamiento de los datos.
- **RF8:** El sistema debe permitir la exportación de los registros clínicos de las mascotas en formato PDF.
- **RF9:** El sistema debe mostrar un dashboard de resumen y alertar automáticamente sobre calendarios de vacunación según la especie de la mascota.
- **RF10:** El sistema debe registrar y mantener un log de auditoría de accesos para garantizar la trazabilidad de las acciones en el sistema.
- **RF11:** El sistema debe enviar una notificación push o correo electrónico al propietario cuando un veterinario añade un nuevo registro médico al historial clínico de su mascota.
- **RF12:** El sistema debe permitir a un usuario transferir la titularidad de una mascota a otro usuario, traspasando el historial clínico completo una vez que el receptor acepte la transferencia.
- **RF13:** El sistema debe permitir la gestión de múltiples propietarios para una mascota, distinguiendo entre un Propietario Principal y Co-propietarios con permisos de gestión compartida.
