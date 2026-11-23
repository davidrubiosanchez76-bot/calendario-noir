# Calendario Noir · BALAS Y ESTRELLAS

Bóveda única del **Calendario Noir** y las efemérides de la **portada**.

## Archivo de datos
- `efemerides.json` (rama `main`) es la única fuente que se edita al incorporar efemérides.
- Fuente: https://raw.githubusercontent.com/davidrubiosanchez76-bot/calendario-noir/main/efemerides.json
- Respaldo: https://cdn.jsdelivr.net/gh/davidrubiosanchez76-bot/calendario-noir@main/efemerides.json

## Estructura
- `version`: versión del esquema.
- `daily`: efemérides con fecha **exacta** (campos `dia`, `mes`, `ano`, `nombre`, `tipo`, `desc`).
- `monthOnly`: acontecimientos con mes y año conocidos, pero **sin día exacto** (campos `mes`, `ano`, `nombre`, `desc`).

Si se conoce solo el año, registrar en **Cronología Negra**, no aquí.

## Protocolo de altas
1. Verificar el día y el año con fuentes fiables. No asignar días supuestos.
2. Comprobar duplicados y fechas conflictivas.
3. Añadir a `daily` o `monthOnly`, sin cambiar el formato.
4. Validar el JSON y comprobar ambas vistas en Blogger.
5. **No añadir efemérides nuevas al HTML de Blogger ni al XML de la plantilla**. Ambas deben leer este JSON.

## Instalación
Una sola actualización de la página estática Calendario Noir y de la plantilla base (para la portada) permite sincronizar las dos vistas. Si no se ha instalado aún la integración, esta bóveda no altera Blogger por sí sola.

## Contenido migrado
306 efemérides diarias y 4 hitos mensuales de la última versión preparada. La migración no supone una auditoría histórica individual de los registros.
