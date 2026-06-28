# Análisis de Interesados

Existen diferentes actores que interactuan con la plataforma, cada uno con distinto nivel de involucramiento y funcionalidad. En la siguiente tabla se presenta una breve comparativa.

| Interesado | Nivel de Interés | Nivel de Poder | Descripción |
| :--- | :--- | :--- | :--- |
| **Propietario de la Mascota** | Alto | Alto | Es el usuario final que adopta la plataforma, registra las mascotas y otorga los accesos a terceros. |
| **Médico Veterinario** | Alto | Medio-Alto | Aporta el valor clínico al ecosistema. Su adopción determina la utilidad de la plataforma en la consulta médica. |
| **Administrador / Desarrollador** | Alto | Alto | Responsable de la infraestructura, seguridad, funcionalidades y la escalabilidad del sistema. |
| **Laboratorios y Clínicas** | Medio | Bajo-Medio | Integración futura para automatizar la carga de órdenes y resultados médicos. |
| **Colegios Veterinarios / Reguladores** | Bajo-Medio | Medio | Asegurar el alineamiento con el marco regulatorio del ejercicio profesional y de datos en salud. |

## Perfiles de Stakeholders

### Propietario de la Mascota

- **Descripción:** Persona encargada del cuidado diario de uno o más animales de compañía. Es el titular principal de la cuenta en AguaraVet.
- **Rol en el sistema:** Registra y gestiona las fichas de las mascotas, asocia co-propietarios (familiares) y autoriza o revoca el acceso temporal de los veterinarios al historial.
- **Necesidades Principales:**
  - Centralizar y estructurar recordatorios de vacunas, vencimientos de desparasitación y tratamientos médicos activos de forma visualmente sencilla.
  - Compartir rápidamente el historial médico con profesionales ante emergencias, derivaciones o segundas opiniones.
  - Contar con un respaldo portátil de los datos médicos (exportación de backups).
- **Frustraciones:**
  - Pérdida de estudios clínicos, CDs o recetas por estar fragmentados en papel, correos o chats de WhatsApp.
  - Tener que explicar verbalmente y de memoria los antecedentes del animal ante un nuevo especialista, con riesgo de omitir detalles clave.
- **Nivel de Interés:** Alto.
- **Nivel de Poder:** Alto.

### Médico Veterinario

- **Descripción:** Profesional matriculado que realiza la atención clínica, diagnóstico y tratamiento de las mascotas.
- **Rol en el sistema:** Accede al Portal Médico previo consentimiento del propietario, consulta el historial clínico completo y registra eventos médicos (vacunas, cirugías, diagnósticos, recetas) con firmas de autoría inmutables.
- **Necesidades Principales:**
  - Acceder de forma rápida a antecedentes críticos (alergias, peso, medicación activa, desparasitaciones) antes de realizar una prescripción.
  - Asegurar la trazabilidad y validez clínica de los datos (saber exactamente qué colega o si el dueño ingresó un registro).
  - Disponer de herramientas eficientes en consulta (como la generación ágil de recetas u órdenes de laboratorios prearmadas).
- **Frustraciones:**
  - Incertidumbre en el diagnóstico y tratamiento por antecedentes médicos incompletos o relatos inexactos de los dueños.
  - Pérdida de tiempo administrativo y repetición innecesaria de estudios clínicos costosos por falta de documentación previa.
- **Nivel de Interés:** Alto.
- **Nivel de Poder:** Medio-Alto.

### Administrador

- **Descripción:** Rol técnico responsable de la operación, mantenimiento, auditoría y cumplimiento normativo de la plataforma. Representa también al equipo de desarrollo y evaluación académica del seminario.
- **Rol en el sistema:** Monitorea el uso de recursos, vigila las colas de procesamiento, audita logs de accesos/cambios inmutables para mitigar vulnerabilidades y asegura la aplicación de políticas de privacidad.
- **Necesidades Principales:**
  - Garantizar la alta disponibilidad del sistema e infraestructura estable con tiempos de respuesta óptimos ($< 1.5$ segundos de carga).
  - Asegurar la protección de datos (cifrado Bcrypt/Argon2, aislamiento de perfiles e información).
  - Disponer de logs detallados de auditoría de accesos y modificaciones para control interno.
- **Frustraciones:**
  - Vulnerabilidades de seguridad críticas como IDOR (referencias directas a objetos inseguras) que permitan a usuarios malintencionados leer fichas de mascotas sin permiso.
  - Sobrecarga del servidor por la subida descontrolada de adjuntos pesados (imágenes/PDFs).
- **Nivel de Interés:** Alto.
- **Nivel de Poder:** Alto.

### Laboratorios y Clínicas

- **Descripción:** Instituciones y empresas proveedoras de servicios de diagnóstico (análisis de laboratorio, imágenes) y centros de atención especializada o internación veterinaria.
- **Rol en el sistema:** Actúan como emisores externos de datos médicos. A mediano/largo plazo, consumirán APIs para adjuntar de forma directa y automatizada los resultados de estudios clínicos a la ficha de la mascota. También accederan a las órdenes de estudio médicos.
- **Necesidades Principales:**
  - Canales de integración sencillos y estandarizados (APIs JSON) con sus propios sistemas de software de laboratorio.
  - Minimizar el tiempo dedicado a reenviar estudios perdidos por los dueños de mascotas.
  - Garantizar que los documentos clínicos subidos solo sean accesibles por los propietarios y profesionales debidamente autorizados.
- **Frustraciones:**
  - Sobrecarga operativa y de comunicación al gestionar el envío de estudios en formatos heterogéneos (WhatsApp, email, descargas manuales).
  - Incompatibilidad entre las plataformas de los laboratorios y los softwares de gestión de las clínicas.
- **Nivel de Interés:** Medio.
- **Nivel de Poder:** Bajo-Medio.

### Colegios Veterinarios / Reguladores

- **Descripción:** Entidades provinciales y nacionales encargadas de regular, fiscalizar y otorgar matrículas para el ejercicio legal de la medicina veterinaria (ej.: colegios veterinarios en Argentina).
- **Rol en el sistema:** Actor indirecto regulatorio que establece las bases del ejercicio profesional. Valida los lineamientos legales de la firma, recetas y la legitimidad de las historias clínicas.
- **Necesidades Principales:**
  - Asegurar que la plataforma exija y valide la matrícula profesional de los veterinarios registrados para evitar el ejercicio ilegal de la profesión.
  - Promover el uso de registros inmutables que sirvan como respaldo legal ante posibles disputas de mala praxis.
- **Frustraciones:**
  - Presencia de plataformas de salud digital que permitan a personas no matriculadas simular diagnósticos o prescribir recetas.
  - Vulnerabilidades o pérdida de confidencialidad en el manejo de historiales clínicos que comprometan la ética profesional.
- **Nivel de Interés:** Bajo-Medio.
- **Nivel de Poder:** Medio.
