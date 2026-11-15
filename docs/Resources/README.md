# Resources — Material técnico y diagramas

Material técnico del proyecto (diagramas de clases, base de datos / entidad-relación, secuencia, estados, actividad, componentes y despliegue) elaborados bajo la metodología **ICONIX**.

> **Nota:** Coloca los archivos de diagramas dentro de [`diagrams/`](diagrams/).

## Diferencias conocidas entre los diagramas originales y el código actual

Al contrastar el documento funcional del semestre anterior con el código PHP y el script [`../db_9eleven.sql`](../db_9eleven.sql), se identificaron los siguientes puntos a tener en cuenta:

1. **Modelo Entidad-Relación (BD):** El script `db_9eleven.sql` implementa **6 tablas** (`administrador`, `categorias`, `productos`, `proveedores`, `ventas`, `detalle_ventas`). No existen tablas físicas `reportes` ni `alerta_stock`, ya que ambos se calculan dinámicamente mediante consultas SQL. Asimismo, falta la tabla de entradas de mercancía (ver **US-105** y **US-302** en `Management/product-backlog.md`).
2. **Diagrama de paquetes / archivos PHP:** El documento funcional plantea archivos separados por acción (`nuevoProducto.php`, `consultarProducto.php`, `eliminarProducto.php`), mientras que la implementación real agrupa cada módulo en un solo archivo (`productos.php`, `categorias.php`, `proveedores.php`, `ventas.php`) manejando vistas mediante el parámetro `?vista=`.
