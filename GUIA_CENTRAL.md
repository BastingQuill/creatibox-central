# 🧵 CreatiBox Central — Guía rápida

Esta es tu nueva herramienta que **centraliza todo**: cotizar, ventas con abonos, gastos, productos, materia prima y métricas. Reemplaza a la app anterior de solo precios.

## Instalación (usa el MISMO Firebase que ya tienes)

Como ya montaste Firebase y GitHub la vez pasada, esto es rápido:

1. **Copia tus llaves de Firebase.** Abre tu `firebase-config.js` viejo, copia los valores, y pégalos en el `firebase-config.js` nuevo de este paquete (reemplazando los `PEGA_AQUI...`). Son el mismo proyecto, así comparten los datos.

2. **Sube los archivos a un repositorio.** Puedes:
   - **Opción A (recomendada):** crear un repo nuevo `creatibox-central` y subir los 5 archivos ahí. Tu app vieja de precios sigue intacta por separado.
   - **Opción B:** reemplazar los archivos en tu repo actual (pero perderías la app vieja).

3. **Activa GitHub Pages** igual que antes (Settings → Pages → Deploy from branch → main → root).

4. **Autoriza el dominio** en Firebase → Authentication → Settings → Dominios autorizados (si usas un repo nuevo con distinta URL, agrégala).

5. **Abre la URL, entra con tu correo**, y acepta cargar los datos iniciales (materia prima + capital $44,057 + los 7 gastos de arranque de tu Excel).

## Las 7 secciones

- **Resumen** — capital actual en tiempo real, ingresos/gastos del mes, gráficas, últimas ventas y cuentas por cobrar.
- **Cotizar** — el flujo por pasos que pediste: Servicio → opciones → cantidad → precio al instante, con botones de WhatsApp, copiar, y "Crear pedido".
- **Ventas y Pedidos** — registra pedidos con su total y ve agregando **abonos parciales** conforme llegan; la barra de progreso muestra cuánto falta por cobrar.
- **Gastos** — registro con categorías; alimenta el capital y las métricas.
- **Productos** — precios de referencia de todo tu catálogo (los que usa el cotizador).
- **Materia Prima** — tus insumos con costo unitario, editable.
- **Métricas** — ingresos por mes, gastos por categoría, métodos de pago, top clientes.

## Flujo estrella: cotizar → pedido → cobrar
1. Cliente pregunta → **Cotizar** → armas el precio en 4 taps → **Crear pedido**.
2. El pedido queda en **Ventas** con su total. Cuando el cliente da el anticipo, abres el pedido → **＋ Agregar abono**.
3. Cada abono actualiza el capital y baja el "falta por cobrar" solo.

## Respaldo
**Exportar Excel** (menú lateral) baja todo — ventas, abonos, gastos, materia prima y resumen — en un archivo con fecha. Hazlo cada semana.

## Nota sobre la Tabla Maestra
Esta app usa los **precios competitivos** para cotizar rápido. Tu **Tabla Maestra en Excel sigue siendo la fuente de verdad** para el costeo profundo (márgenes, mano de obra, análisis de stickers). Las dos conviven: la app para el día a día, el Excel para pensar la estrategia.
