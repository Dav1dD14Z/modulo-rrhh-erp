# 6. Vista de Tiempo de Ejecución

## Escenario 1 – Alta de un nuevo empleado
1. El responsable de RRHH completa el formulario en la UI.
2. La UI envía una solicitud `POST /api/employees` al backend.
3. El `EmployeeController` valida la solicitud.
4. `EmployeeService` crea el registro en la base de datos.
5. `IntegrationService` notifica al módulo de Finanzas.
6. El sistema de notificaciones envía un correo de bienvenida.

## Escenario 2 – Solicitud de vacaciones
1. El empleado inicia sesión mediante el sistema SSO.
2. Envía una solicitud `POST /api/vacations/request`.
3. El `AttendanceService` registra la solicitud.
4. El gerente recibe una notificación para aprobarla.
5. El módulo actualiza el estado y genera un evento en el ERP.

## Escenario 3 – Evaluación de desempeño
1. El gerente accede al módulo de RRHH.
2. Completa la evaluación de un empleado.
3. `EvaluationService` guarda la información y calcula el promedio.
4. Se genera un informe que puede ser exportado a PDF.
