# 🕯️ Plan Financiero — Velas Artesanales

Dashboard financiero interactivo para modelar la rentabilidad de un negocio de velas artesanales. Permite ajustar todos los parámetros en tiempo real y ver al instante cómo afectan al EBITDA, break-even y cash flow.

---

## ¿Qué incluye?

- **Parámetros editables** — ventas, precio, coste por vela (producción + envío + packaging), inversión en ADS y hosting
- **Estimación automática por ADS** — calcula ventas esperadas a partir de impresiones, CTR y tasa de conversión
- **Cuenta de resultados mensual** — ingresos, COGS, margen bruto y EBITDA
- **Break-even** — unidades mínimas para cubrir todos los costes, conversión mínima necesaria
- **CAC y ROAS** — eficiencia de la inversión publicitaria
- **Proyección de cash flow a 6 meses** — con crecimiento orgánico estimado
- **Tabla de escenarios** — desde muy pesimista hasta muy optimista
- **Conclusiones clave** — resumen estratégico del modelo

---

## Cómo usar

1. Abre el archivo `velas_plan_financiero.html` en cualquier navegador
2. Edita los campos de la sección **Parámetros del negocio**
3. Todos los cálculos se actualizan automáticamente

No requiere instalación, servidor ni conexión a internet (salvo para cargar las fuentes tipográficas de Google Fonts).

---

## Parámetros base del modelo

| Parámetro | Valor |
|---|---|
| Precio de venta | 15€ |
| Coste total por vela | 8€ (producción + envío + packaging) |
| Margen bruto por vela | 7€ (47%) |
| Inversión ADS mensual | 100€ |
| Hosting mensual | 29€ |
| **Total costes fijos** | **129€/mes** |
| **Break-even** | **19 unidades/mes** |

---

## Lógica de cálculo

```
Ingresos          = ventas × precio
COGS              = ventas × coste por vela
Margen bruto      = ingresos − COGS
EBITDA            = margen bruto − costes fijos (ADS + hosting)
Break-even (uds)  = costes fijos ÷ margen unitario
CAC               = inversión ADS ÷ unidades vendidas
ROAS              = ingresos ÷ inversión ADS
```

---

## Conclusiones del modelo base

1. **Necesitas vender 19 velas al mes** para cubrir todos los costes. Con 15 velas pierdes ~24€/mes; con 20 ya ganas 11€.
2. **El margen por vela es sólido** (7€, 47%) — el reto es el volumen, no el producto.
3. **La repetición de compra es la palanca más eficiente** — un cliente que compra 3 veces al año genera 21€ de margen adicional sin incrementar el gasto publicitario.

---

## Tecnologías

- HTML5 + CSS3 + JavaScript vanilla
- [Chart.js 4.4.1](https://www.chartjs.org/) — gráficos
- [DM Sans + DM Serif Display](https://fonts.google.com/) — tipografía

---

## Estructura del archivo

```
velas_plan_financiero.html   ← archivo único, todo incluido
README.md                    ← este archivo
```
