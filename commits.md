# Formato commits
Aquí se mencionan algunas buenas prácticas comúnmente usadas.

## Commits Atómicos
Realiza commits que sean pequeños y atómicos, lo que significa que cada commit debe representar una unidad lógica de cambio. Esto facilita la revisión, la depuración y la identificación de problemas.

## Mensajes de Commit Descriptivos
Escribe mensajes de commit claros y descriptivos que expliquen qué cambios se realizaron y por qué. Sigue una convención, como la Convención de Mensajes de Commit Consciente (Conventional Commits). Costa de las siguientes partes separadas por una línea en blanco entre ellas:
- Encabezado: Breve y descriptivo, consta de dos partes, tipo de commit y descripción. Aquí si se desea se puede añadir también el número de la tarea de JIRA asociada para poder vincularlos automáticamente y que aparezcan los commit en la tarea. Tipos de encabezados:
  - feat: cuando se agrega una nueva característica o funcionalidad.
  - fix: cuando se corrige un error.
  - refactor: cuando se refactoriza código sin añadir funcionalidad.
  - docs: cambios relacionados con la documentación del proyecto.
  - style: cambios de estilo en el código. (formato, espaciado, orden de importaciones…)
  - refactor: refactorización del código.
  - perf: mejoras de rendimiento en el código.
  - test: adición o modificación de tests.
  - chore: tareas de mantenimiento que no afectan a la funcionalidad. (actualización de dependencias, configuración…)
  - build: cambios relacionados con la construcción o configuración del proyecto.
  - ci: cambios en la configuración de integración continua.
 
- Cuerpo (opcional): Si se necesita ampliar la información del commit como explicaciones técnicas o el contexto.
- Pie de página (opcional): Mencionar referencias para seguimiento.

Ejemplos:
```
feat(JIRA-123): Agregar función de inicio de sesión

Agrega la capacidad de los usuarios para iniciar sesión en la aplicación.
Esta característica incluye la autenticación basada en tokens JWT.

Closes #123
```

```
fix(JIRA-456): Corregir error crítico en el cálculo de impuestos

Se ha solucionado un problema crítico que provocaba un cálculo incorrecto de impuestos
en la página de pago. La variable de tasa de impuestos ahora se calcula correctamente
y se aplica a los productos en el carrito de compras.

Este hotfix es urgente y debe ser desplegado de inmediato para solucionar el problema
 en producción.

Closes #456
```
