# Solución — Maqueta del control de ingreso al Casino

## Arquitectura (VERIFICADO)
Un solo archivo `index.html` sin dependencias externas ni servidor. Se publica como sitio estático en GitHub Pages. Estado en memoria; al recargar vuelve a los datos semilla. Única persistencia: `localStorage["casino.perfil"]`.

## Componentes (en `index.html`)
- Generador de personas ficticias (semilla fija) y 12 casos base con nombre propio para las demostraciones.
- Validación de RUT (dígito verificador módulo 11, la tecla `*` vale K), formato y enmascarado.
- Reglas: tramo de valor por grado (1: 3-11, 2: 12-14, 3: 15-21; sin grado lo asigna el Jefe Casino), calendario hábil con feriados fijos, límite de elección de menú (día 25 del mes anterior), aviso de ausencia hasta 23:59 del día anterior, cierres que bloquean la terminal.
- Cuatro perfiles conmutables con «Maqueta · probar como».
- Reportes CSV generados en el navegador.

## Flujo de datos
Semilla -> estructuras en memoria (`P`, `R`, `AUS`, `INV`, `MENU`, `MSEM`, `CIERRES`, `ALERTAS`) -> render por perfil. Una emisión en la terminal crea un registro con ID `AAAA-NNNNNN` que alimenta detalle de ingresos, «Mi casino» y el reporte mensual.

## Decisiones
- Identificación solo por RUT digitado (UIA, 22-10-2026). VERIFICADO.
- Los valores del almuerzo son de ejemplo. VERIFICADO.

## Estado y pendientes
- Estado: maqueta funcional, último cambio 2026-10-22 (franja institucional). VERIFICADO (git log).
- No comprobé: la publicación en Pages ni el comportamiento en navegadores distintos de los habituales.
- Pendientes de confirmar por el equipo: valores y tramos reales, fuente de la nómina y de los feriados, versión productiva (RUT + PIN), responsable y criterios de aceptación.
