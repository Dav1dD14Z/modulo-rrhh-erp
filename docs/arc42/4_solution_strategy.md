# 4. Estrategia de Solución

## Enfoque General
La solución sigue una arquitectura **modular basada en microservicios**, integrándose al ERP mediante APIs REST.  
Cada componente se comunica de forma desacoplada, permitiendo una evolución independiente.

## Principios Arquitectónicos
- **Separación de responsabilidades** (MVC y capas bien definidas).
- **Integración mediante APIs RESTful**.
- **Persistencia unificada en PostgreSQL**.
- **Seguridad basada en JWT / SSO**.
- **Automatización CI/CD** para despliegues controlados.

## Estrategia Tecnológica
| Área | Tecnología / Herramienta |
|------|---------------------------|
| **Backend** | Java 17 + Spring Boot |
| **Base de Datos** | PostgreSQL |
| **Frontend** | Angular / React (según stack del ERP) |
| **Comunicación** | REST API / JSON |
| **Versionado** | GitHub |
| **CI/CD** | GitHub Actions |
| **Documentación** | Markdown + PlantUML + arc42 |

## Estrategia de Integración
- El módulo RRHH se integrará con el ERP mediante una **API Gateway**.
- Las dependencias externas (nómina, notificaciones) se consumirán vía **REST**.
