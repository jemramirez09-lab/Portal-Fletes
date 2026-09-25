# UNIBER · Portal de Fletes

Paquete completo del portal de gestión de fletes (sin stubs).

## Módulos

| Archivo | Descripción |
|---------|-------------|
| `index.html` | Portal principal con **Totalizador Semanal** mejorado |
| `comprobantes.html` | Gestión de Comprobantes / RTOS relacionados |
| `fletes-pro.html` | Control Gerencial de Fletes PRO (PHR / UNIMAX) |
| `logitrack.html` | LogiTrack RTOS (autorizaciones y remitos) |
| `Cortes_Facturas.html` | Control Cortes Pagos Fletes |
| `reportes.html` | Reportes Semanales consolidados |
| `tarifarios.html` | Tarifarios unificados (Hacha de Piedra / Sevillanita) |

## Cómo usar

```bash
cd uniber-portal-fletes
python3 -m http.server 8080
# Abrir http://localhost:8080
```

O abrir `index.html` directamente en el navegador (algunas APIs de archivos pueden requerir servidor local).

## Atajos de teclado (portal)

| Tecla | Acción |
|-------|--------|
| 1 | Comprobantes |
| 2 | FLETES-PHR |
| 3 | FLETES-RTOS |
| 4 | Reportes |
| 5 | Cortes Facturas |
| 6 | Totalizador Semanal |
| Esc | Cerrar modal |

## Datos

Todo se guarda en `localStorage` del navegador. Claves principales:

- `comprobantes_pro` / datos PHR (Fletes PRO)
- `unimax_fletes_v52` (LogiTrack)
- `comprobantes_multifactura` (Comprobantes)
- Claves propias del Totalizador (`totalizador_semana`, manuales, aliases, etc.)

## Totalizador (mejoras incluidas)

- Botón **Guardar semana** + badge en la tarjeta
- Filtro / búsqueda de transportistas
- Editor de aliases de nombres
- Origen PHR / RTOS / Manual en exportes
- Manuales asociados a la semana
- Cache de totales
- Mini gráfico Chart.js
- Export PNG profesional
- Atajo tecla **6**
