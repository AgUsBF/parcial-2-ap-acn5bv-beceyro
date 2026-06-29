# Objetivo General

Este documento detalla el planteamiento del objetivo del proyecto **AguaraVet** utilizando las metodologías **SMART** y **OKRs**.

## Enfoque SMART

### Specific - [S]MART

**¿Qué queremos lograr?**

Diseñar, desarrollar e implementar una plataforma web responsive y *mobile-first* que centralice, estandarice y permita la gestión segura y portable de la historia clínica digital de mascotas, controlada directamente por los propietarios y con la capacidad de compartir el acceso mediante permisos granulares con médicos veterinarios a través de un Portal Médico dedicado.

### Measurable - S[M]ART

**¿Cómo medir el éxito?**

- **Funcionalidad:** Implementación y aprobación del 100% de las historias de usuario de las épicas planteadas en el planeamiento.
- **Rendimiento:** Tiempos de respuesta de backend menores a 1.5 segundos para la carga del dashboard clínico.
- **Calidad:** Cobertura de pruebas automatizadas unitarias y de integración (Pest/PHPUnit) $\ge$ 80%.
- **Validación:** Completar con éxito pruebas de aceptación de usabilidad con los actores del grupo de control inicial (Ej.: 4 dueños de mascotas y 2 veterinarios) con una tasa de éxito de tareas críticas $\ge$ 90%.

### Achievable - SM[A]RT

**¿Es viable con los recursos y tiempo disponibles?**

Sí, la arquitectura propuesta basada en tecnologías robustas y de rápida iteración (Laravel 12, Livewire, Alpine.js/Tailwind y PostgreSQL) permite agilizar el desarrollo frontend y backend. El alcance se encuentra acotado estrictamente a un MVP mediante la matriz de impacto-esfuerzo, postergando funcionalidades complejas (como geolocalización o teleconsulta) a fases de mediano y largo plazo.

### Relevant - SMA[R]T

**¿Por qué es importante para el negocio/usuario?**

Resuelve el problema central identificado en las entrevistas preliminares: la pérdida de trazabilidad médica de la mascota debido al almacenamiento fragmentado (papel, WhatsApp, email, etc) y la repetición innecesaria de estudios clínicos. Devuelve la propiedad de la información al dueño sin perder la validez clínica del dato.

### Time-bound - SMAR[T]

**¿En cuánto tiempo se completará?**

El diseño, desarrollo, pruebas, validación y documentación del MVP de la plataforma se completará en un plazo de **24 semanas** (web + mobile), listo para su despliegue y presentación en la defensa del Seminario Final.

## OKR - Objectives and Key Results

Se proponen 3 Objetivos estratégicos con sus respectivos Resultados Clave orientados a Calidad, Seguridad y Usabilidad.

### Objetivo 1

**Entregar una plataforma robusta, ágil y de alto rendimiento que cubra el 100% del alcance del MVP.** Este objetivo se centra en la ejecución técnica y la calidad de la ingeniería de software.

- **KR 1.1:** Desarrollar y testear el 100% de los Requerimientos Funcionales prioritarios del MVP cumpliendo con todos los criterios de aceptación en las Historias de Usuario.
- **KR 1.2:** Alcanzar una cobertura de código del **85%** en pruebas unitarias y de integración utilizando Pest/PHPUnit ejecutados en la pipeline de integración continua (CI/CD).
- **KR 1.3:** Optimizar la base de datos PostgreSQL y las interacciones con Livewire para mantener los tiempos de carga del dashboard principal por debajo de **1.2 segundos** en el entorno de pre-producción.

### Objetivo 2

**Asegurar la privacidad, portabilidad y trazabilidad inmutable de los registros clínicos.** Este objetivo garantiza el cumplimiento de los estándares de seguridad y confianza demandados por los veterinarios y los propietarios en las entrevistas.

- **KR 2.1:** Implementar la inmutabilidad y firma digital (logs de auditoría/versiones) en el 100% de los registros médicos cargados por terceros, garantizando que figure quién y cuándo insertó o modificó cada dato.
- **KR 2.2:** Asegurar cero filtraciones de datos (aislamiento entre cuentas), garantizando por medio de políticas lógicas en Laravel que ningún usuario acceda a la ficha de una mascota sin invitación activa.
- **KR 2.3:** Habilitar el flujo de exportación de historial clínico en dos formatos estándares: **PDF** (legible para el profesional en consulta) y **JSON** (portabilidad absoluta para transferencia de datos) con un 100% de fidelidad de la información.

### Objetivo 3

**Validar la experiencia de usuario (UX) de manera cuantitativa y cualitativa con usuarios reales.** Este objetivo asegura que el producto realmente resuelva la fricción de uso diario identificada en el campo.

- **KR 3.1:** Lograr devoluciones satifactorias tras realizar pruebas directas con 4 dueños de mascotas.
- **KR 3.2:** Conseguir que los 2 veterinarios evaluadores logren aceptar una invitación y registren un evento médico simulado sin asistencia técnica previa.
