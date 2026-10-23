# Lote retiro vs lote en picking

Panel Castaño que cruza el lote retiro (FEFO) contra los lotes encontrados en picking. Es un solo `index.html`, sin build.

- **Fuera (rojo):** lote en picking **menor o igual** al lote retiro.
- **Dentro (verde):** lote en picking **mayor** al lote retiro.

Las celdas con varios lotes (`426/432`) se separan y cada lote toma la cantidad en la misma posición (`657/576`).

## Uso

1. **Subir Excel:** el formato "Toma de Inventario Físico por Zonas". El panel busca la fila de encabezados con SKU, Descripción, Lote FEFO, Lote en Picking y Cant, y toma la fecha de la celda junto a **FECHA REALIZADO** (fila 2).
2. **Filtros:** periodo (todas, última toma, últimos 7 días, mes actual), rango de fechas, estado y búsqueda por SKU o producto.
3. **Historial de cargas:** cada Excel queda como una toma por fecha; subir la misma fecha la reemplaza. Se puede ver o eliminar cada toma.

## Dónde se guarda el historial

- En **GitHub Pages** (o abriendo el archivo localmente) el historial se guarda solo en el navegador de cada persona.
- En el link de **claude.ai** el historial es compartido: todos los que abren el link ven las mismas cargas.

Lee el Excel con [SheetJS](https://sheetjs.com) desde cdnjs, así que necesita conexión a internet. El archivo no sale del navegador.
