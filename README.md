# Microservicio de Inventario

Este repositorio contiene el microservicio de inventario, utilizado como base para la Evaluación Parcial 1 de flujos de trabajo DevOps.

## Estrategia de Ramificación: GitFlow

Para este proyecto hemos decidido implementar **GitFlow** (por sobre Trunk-Based Development). 
**Justificación:** GitFlow nos permite mantener un control estricto sobre las versiones del código. Al tener una rama `main` exclusiva para código estable (producción) y una rama `develop` para integrar nuevas características, reducimos el riesgo de romper el entorno de producción. Además, las ramas `feature/` y `hotfix/` estructuran de forma clara qué tipo de trabajo se está realizando, lo cual es ideal para simular un entorno colaborativo y ordenado.

## Convenciones y Buenas Prácticas

### 1. Naming de Ramas
- `main`: Código estable y listo para producción.
- `develop`: Código en desarrollo e integración.
- `feature/nombre-de-la-caracteristica`: Para nuevos desarrollos (ej. `feature/mejora-modelo`).
- `hotfix/nombre-del-arreglo`: Para correcciones urgentes en producción (ej. `hotfix/corregir-stock`).

### 2. Convención de Commits (Conventional Commits)
Se utilizarán los siguientes prefijos para mantener una trazabilidad clara:
- `feat:` Para nuevas funcionalidades.
- `fix:` Para solucionar errores.
- `docs:` Para cambios en la documentación (como este README).
- `chore:` Para tareas de mantenimiento o configuración.

### 3. Flujo de Merge y Revisiones (Pull Requests)
- Todo código nuevo debe nacer de `develop` mediante una rama `feature/`.
- No se permite hacer *commit* directo a `develop` ni a `main`.
- Se debe abrir un Pull Request (PR) hacia `develop`. 
- Una vez aprobado e integrado en `develop`, los cambios se preparan para su posterior paso a `main`.
- Los errores críticos en `main` se resuelven creando una rama `hotfix/` desde `main`, y luego se hace PR tanto a `main` como a `develop`.

## Tecnologías Utilizadas
- Java
- Spring Boot
- Maven

## Declaración de uso de IA
Para el desarrollo de este encargo, se utilizó asistencia de Inteligencia Artificial (Gemini) con el objetivo de estructurar los pasos del flujo de trabajo, redactar la plantilla base de este documento y generar el archivo de configuración YAML para GitHub Actions. Todas las ejecuciones de comandos, resolución de conflictos (merge conflicts) y decisiones de arquitectura de ramas fueron realizadas y validadas de forma manual.

## Reflexión Individual
("Al aplicar GitFlow me di cuenta de la importancia de serparar el codigo en distintas ramas para evitar que el codigo se caiga o evitar codigos graves, ademas estuve investigando que muchas empresas utilizan GitFlow lo que de a poco nos mentaliza para el dia de mañana estar preparados para la produccion de codigos. Ademas la automatizacion con Github Actions me demostro lo vital e importante es tener una herramienta que valide el codigo automaticamente antes de integrarlo.")