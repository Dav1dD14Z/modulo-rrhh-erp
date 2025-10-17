# 5. Vista de Bloques de Construcción

## Nivel 1 – Estructura General del Sistema
El sistema se divide en los siguientes bloques principales:

| Bloque | Descripción |
|---------|--------------|
| **UI Web** | Interfaz de usuario para empleados, gerentes y RRHH. |
| **API REST** | Capa de servicios que expone las operaciones principales. |
| **Lógica de Negocio** | Implementa las reglas y procesos del dominio RRHH. |
| **Persistencia** | Acceso a la base de datos PostgreSQL. |
| **Integración** | Comunicación con Finanzas y Notificaciones. |

## Nivel 2 – Componentes del Backend
| Componente | Descripción |
|-------------|-------------|
| **EmployeeService** | CRUD de empleados. |
| **AttendanceService** | Control de asistencia y vacaciones. |
| **EvaluationService** | Evaluaciones de desempeño. |
| **ReportService** | Generación de informes y métricas. |
| **IntegrationService** | Conexión con módulos externos (Finanzas, Email). |

## Nivel 3 – Detalle Interno de Componentes
Cada servicio sigue el patrón:
- **Controller** → expone endpoints REST.
- **Service** → contiene la lógica de negocio.
- **Repository** → acceso a datos.

Ejemplo de estructura:
