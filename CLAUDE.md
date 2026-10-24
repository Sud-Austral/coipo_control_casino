# coipo_control_casino — guía para agentes

Maqueta de validación (iniciativa CON005, UIA) del control de ingreso al Casino Institucional de CONAF.
Descripción funcional y cómo probarla: [`README.md`](README.md). Problema y solución: [`insumos/`](insumos/).

## Estado y alcance (VERIFICADO en el repo)
- Es **una maqueta no operacional**: un único archivo `index.html` (HTML + CSS + JS + imágenes embebidas), sin backend, sin build, sin dependencias externas, sin `package.json`, sin pruebas automatizadas ni CI.
- Los datos (personas, RUT, grados, valores, registros) son **ficticios** y se generan al cargar con un generador pseudoaleatorio de semilla fija (`seed=7`). Nada se persiste, salvo el perfil elegido en `localStorage` (clave `casino.perfil`).
- Se publica en GitHub Pages (`.nojekyll` presente): https://sud-austral.github.io/coipo_control_casino/ (URL tomada del README; no la comprobé).

## Estructura
- `index.html` — toda la aplicación. Secciones por orden: estilos, marcado de los 4 perfiles (Terminal casino, Funcionario, Jefe Casino, Jefa de Bienestar), y un `<script>` con datos de prueba (`seedPersonas`, `seedCierres`, `seedMenuSem`, `MINUTAS`), reglas (tramos por grado, feriados `FER`, días hábiles, límite del día 25 para elegir menú, aviso de ausencia hasta las 23:59 del día anterior) y render.
- `README.md` — manual de la maqueta (perfiles, terminal, ticket, reportes, cierres).
- `.nojekyll`, `.gitattributes`, `.gitignore` — publicación y normalización de fin de línea.

## Cómo ejecutar
Abrir `index.html` en el navegador (no hay servidor ni comandos). Para reiniciar el estado: botón «Reiniciar datos de prueba» del pie, o recargar.

## Convenciones y trampas
- Todo en español. Los cambios de reglas de negocio deben reflejarse también en el `README.md`.
- Mantener el archivo autocontenido: no agregar CDN, fuentes ni scripts externos.
- Nunca poner RUT, nombres ni valores reales: la maqueta debe seguir siendo demostración con datos ficticios.
- Hay feriados fijos en `FER` (sin año): revisarlos si se usa otro año; los feriados móviles (p. ej. Viernes Santo) están escritos a mano.
- El ID del ticket es `AAAA-NNNNNN` correlativo por año, recalculado en `asignarIds()`.
- La identificación es solo por RUT digitado (decisión UIA 22-10-2026); RUT + PIN y biometría están fuera de alcance.

## Qué no tocar
No convertir la maqueta en sistema productivo ni conectar datos reales sin decisión del equipo (ver `insumos/01-SOLUCION.md`, pendientes).
