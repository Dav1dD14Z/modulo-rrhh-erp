# 7. Vista de Despliegue

## Entorno de Producción
El sistema se desplegará en la infraestructura corporativa, bajo contenedores Docker y orquestación Kubernetes.

### Nodos Principales
| Nodo | Descripción |
|-------|--------------|
| **Servidor Web** | Aloja la interfaz de usuario (Angular/React). |
| **Servidor de Aplicaciones** | Ejecuta el backend (Spring Boot). |
| **Base de Datos** | PostgreSQL compartida con otros módulos ERP. |
| **API Gateway** | Control de acceso e integración central. |
| **Servidor de Notificaciones** | Maneja los correos automáticos. |

