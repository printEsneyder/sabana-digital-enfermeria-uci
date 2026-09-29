# Capturas de pantalla

Imágenes referenciadas por el `README.md` de la raíz del repositorio. **Mantén los nombres exactos** de las tablas, porque el README las vincula por ruta.

Esta carpeta está en la raíz del repositorio, fuera de `lib/`, por lo que **no se empaqueta en los builds** de Android, iOS, web ni escritorio.

---

## Antes de capturar: datos clínicos

Este proyecto maneja **información clínica de pacientes reales**. El repositorio es público. Antes de tomar cualquier captura:

1. **Usa una base de datos de prueba.** Crea ingresos ficticios: nombres de prueba, identificaciones inventadas y diagnósticos genéricos. Nunca captures pacientes reales.
2. **Oculta datos personales.** Revisa que no aparezcan correo, teléfono, EPS/ARL real, número de carpeta ni dirección del paciente.
3. **Cierra sesión ajena.** Si alguna pantalla muestra tu correo o tu foto, cierra sesión o usa la cuenta de prueba antes de capturar.
4. **Cierra el navegador de la vista de Firestore.** No incluyas pestañas del emulador de Firebase en la captura.
5. **Sin firmas reales.** La pantalla de observaciones extra incluye seis paneles de firma: usa trazos de prueba.
6. **Sin datos de conexión.** La pantalla de inicio de sesión debe capturarse con los campos vacíos, nunca con una sesión abierta.

Revisa cada PNG antes de guardarlo: haz zoom al 100 % y confirma que no haya texto legible que identifique a una persona.

---

## Formato recomendado

La aplicación se usa en tableta y escritorio, con tablas densas. Captura en **formato horizontal**.

| Parámetro | Valor |
|-----------|-------|
| Relación de aspecto | 16:9 o 16:10 |
| Resolución | 1920x1080 (o 1600x900 si la tabla no se corta) |
| Escala del sistema | 100 % |
| Formato de archivo | PNG sin pérdida |

El README las muestra a `width="360"` en cuadrículas de tres columnas, así que una resolución mayor solo aumenta el peso del repositorio sin mejorar la lectura.

## Cómo tomar cada captura

1. Usa el emulador de Android en horizontal, o la versión web en el navegador a pantalla completa.
2. **Carga las listas.** Las tablas se ven vacías si no hay datos: crea al menos dos o tres ingresos de prueba con sus registros diarios.
3. Si la pantalla tiene pestañas o filtros, deja activa la opción que mejor represente el módulo.
4. Recorta el espacio sobrante para que la captura ocupe todo el ancho asignado.

---

## Capturas principales

Son las que el `README.md` muestra en la sección **Capturas de pantalla**. Las 15 son necesarias para que la cuadrícula quede completa.

| Archivo | Pantalla | Código fuente |
|---------|----------|---------------|
| `login.png` | Inicio de sesión | `lib/pages/login_page.dart` |
| `ingresos.png` | Lista de ingresos con buscador y filtro por sala | `lib/pages/ingreso/ingresos_page.dart` |
| `ingreso-detalle.png` | Detalle del ingreso y sus módulos | `lib/pages/ingreso/ingreso_details_page.dart` |
| `registro-diario.png` | Registro diario con las ocho secciones clínicas | `lib/pages/registro_diario/registro_diario_page.dart` |
| `monitoria.png` | Monitoría hemodinámica por hora | `lib/pages/monitoria_hemodinamica/monitoria_hemodinamica_page.dart` |
| `graficos.png` | Gráficos de presión arterial | `lib/pages/monitoria_hemodinamica/monitoria_hemodinamica_graphics_page.dart` |
| `balance-liquidos.png` | Balance de líquidos administrados y eliminados | `lib/pages/balance_liquidos/balances_de_liquidos_page.dart` |
| `nutricion.png` | Nutrición, IMC y requerimiento calórico | `lib/pages/nutricion/nutricion_page.dart` |
| `glasgow.png` | Escala de Glasgow | `lib/pages/glasgow/glasgow_page.dart` |
| `sedacion.png` | Control de sedación (RASS) | `lib/pages/control_sedacion/control_sedacion_page.dart` |
| `cateteres.png` | Catéteres | `lib/pages/cateteres/catateres_page.dart` |
| `antibioticos.png` | Tratamientos antibióticos | `lib/pages/tratamiento_antibioticos/tratamientos_antibioticos_page.dart` |
| `necesidades.png` | Lista de necesidades (NIC) | `lib/pages/necesidades/necesidades_page.dart` |
| `observaciones-firmas.png` | Observaciones extras y firmas por turno | `lib/features/observaciones_extras/presentation/pages/observaciones_extras_page.dart` |
| `reporte-pdf.png` | Vista del reporte PDF generado | Salida de `lib/features/reportes/application/pdf_reporte_service.dart` |

## Capturas opcionales

Amplían el README. Si las agregas, añade también su celda en la tabla correspondiente del `README.md`.

| Archivo | Pantalla | Código fuente |
|---------|----------|---------------|
| `cambio-posicion.png` | Cambio de posición por hora | `lib/pages/cambio_posicion/cambio_posicion_page.dart` |
| `control-riesgos.png` | Control de riesgos (UPP, caídas, aislamiento) | `lib/pages/control_riegos/control_de_riesgos_page.dart` |
| `marcapasos.png` | Marcapasos | `lib/pages/marcapasos/marcapasos_page.dart` |
| `sondas.png` | Sondas y drenajes | `lib/pages/sondas/sondas_page.dart` |
| `procedimientos.png` | Procedimientos especiales | `lib/pages/procedimientos_especiales/precedimientos_page.dart` |
| `lista-tratamientos.png` | Lista de tratamientos | `lib/pages/lista_tratamientos/lista_tratamientos_page.dart` |
| `intervenciones.png` | Intervenciones de enfermería | `lib/pages/intervenciones/intervenciones_page.dart` |
| `resultados.png` | Resultados e indicadores (NOC) | `lib/pages/resultados/resultados_de_intervencion_page.dart` |
| `ingreso-nuevo.png` | Formulario de ingreso de paciente | `lib/pages/ingreso/create_ingreso_page.dart` |

---

## Nota sobre el rótulo de las imágenes

El `README.md` no puede superponer texto sobre las imágenes porque GitHub descarta el CSS en el README. Por eso cada nombre va en una celda de tabla encima de su captura. Si cambias el orden o los nombres, actualiza también la tabla del `README.md` para que no se desalineen.
