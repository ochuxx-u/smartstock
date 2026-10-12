# SmartStock

**SmartStock** es un sistema encargado de gestionar inventario, diseñado para controlar el stock de productos por **lotes con fecha de vencimiento**, registrar **movimientos de inventario** (entradas, salidas, ajustes y anulaciones) y generar **alertas automáticas** por stock bajo, vencimiento próximo o productos vencidos, con notificaciones por correo a los responsables.

El sistema cubre el ciclo completo del inventario: catálogo de productos y proveedores, compras y reposición, salidas de stock con criterio de rotación **FEFO** (*First Expired, First Out*: se consume primero el lote más próximo a vencer), valoración del inventario, auditoría de operaciones y un dashboard para la toma de decisiones.

El acceso al sistema está definido por **roles** con permisos diferenciados:

- **Administrador:** gestiona usuarios, catálogo, compras, alertas y puede anular movimientos.
- **Empleado:** registra movimientos de inventario y gestiona alertas del día a día.
- **Propietario (visor):** consulta el dashboard y el estado del inventario en modo lectura.

En cuanto a su arquitectura, SmartStock combina una interfaz construida con **Python + NiceGUI**, un backend en **Google Apps Script** que expone una API, **Google Sheets** como base de datos, **Google Drive** para respaldos periódicos y **Gmail** para el envío de notificaciones. El código fuente se versiona en un repositorio de GitHub y las tareas programadas (triggers) ejecutan revisiones diarias de stock y vencimientos.

---

## Diagramas UML

El sistema cuenta con una documentación completa de diagramas de análisis y diseño (estructural, casos de uso, componentes, entidad–relación, clases, despliegue, actividad, estados y secuencia).

👉 **[Ver todos los diagramas UML](Docs/DIAGRAMAS_UML.md)**
