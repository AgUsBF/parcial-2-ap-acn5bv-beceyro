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
