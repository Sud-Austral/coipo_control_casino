# Problema — Control de ingreso al Casino Institucional

Marcas: VERIFICADO = visto en el repo (README, `index.html`, historial git). INFERIDO = deducido. «Pendiente de confirmar» = no se desprende del repo.

## Contexto
- Iniciativa CON005 de la Unidad de Información y Análisis (UIA) de CONAF, a pedido del Servicio de Bienestar (solicitud del 13-08-2026). VERIFICADO (README).
- El repo cita como referencia una propuesta comercial «Control de Comedor» de GeoVictoria (agosto 2026). Por acuerdo de la reunión UIA del 22-10-2026 se descartó biometría, licencia y arriendo: la persona se identifica con su RUT digitado en un teclado numérico. VERIFICADO (README).

## Usuarios
Funcionarios (dotación, plazo fijo, honorarios), Jefe Casino y Jefa de Bienestar, más el personal que opera la terminal del casino. VERIFICADO (perfiles de la maqueta).

## Dolor actual
- La minuta semanal se envía por correo electrónico; la maqueta propone publicarla en el sistema. VERIFICADO (README, «Menú semanal»).
- Planificar raciones, registrar asistencia y calcular el descuento por planilla según tramo de grado. Cómo se hace hoy: pendiente de confirmar por el equipo (el repo no lo describe).

## Alcance de la maqueta
Terminal con RUT digitado y ticket con ID único; «Mi casino» (asistencias, elección de menú normal/hipocalórico/vegano hasta el día 25 del mes anterior, avisos de ausencia, invitados); planificación de raciones a 10 días hábiles; menú semanal; reportes CSV (descuento mensual, consumo por unidad, anual); cierres del casino con alertas; personas habilitadas por tramo. VERIFICADO.

## Fuera de alcance
Validación con RUT y PIN (versión futura), biometría, persistencia, integración con RR.HH./remuneraciones, datos reales. VERIFICADO (README) salvo la integración, INFERIDA.

## Criterios de éxito
No definidos en el repo; pendiente de confirmar por el equipo. Lo único explícito es que sirva para validar el flujo con Bienestar antes de construir el sistema.
