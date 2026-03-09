# RPK NEXUS | Simulador Make or Buy v5.5

## 📋 Descripción General
Esta herramienta es un motor de decisión estratégica diseñado para el entorno industrial **RPK NEXUS**. Permite evaluar la viabilidad de subcontratar un lote de producción frente a la fabricación interna, considerando costes horarios, cadencias, logística y plazos de entrega.

## 🛠️ Arquitectura Técnica
- **Frontend**: React 18 (via CDN) con Babel para procesamiento en caliente.
- **Estilos**: TailwindCSS con una paleta personalizada "RPK Dark Mode".
- **Generación de Reportes**: jsPDF + autoTable para la creación de PDFs profesionales.
- **Persistencia**: LocalStorage para el histórico de decisiones.

## 🏷️ Guía de Etiquetas y Componentes

### 1. Datos de Producción (Sección Interna)
- `Referencia`: Identificador único del artículo o pedido.
- `Cantidad`: Tamaño total del lote a fabricar.
- `Palets`: Número de palets necesarios para el transporte (influye en el coste logístico).
- `Viajes`: Calculado automáticamente (1 viaje por cada 2 palets). Define el coste administrativo.
- `Cadencia Interna (pzs/h)`: Velocidad de producción real en las máquinas de RPK.
- `Coste Interno RPK (€/h)`: Coste hora de la máquina/operario en planta.

### 2. Estructura de Subcontratación (Sección Externa)
- `Nombre del Proveedor`: Información descriptiva para el reporte.
- `Coste Unitario Subcontrata (€/pz)`: El precio por pieza ofertado por el proveedor. Es el dato maestro de la factura.
- `Simulación por Horas`: (Opcional) Permite calcular el coste unitario a partir de un coste hora y una cadencia prometida.
- `Coste Logístico`: Suma del transporte por palet y la gestión administrativa por cada viaje.
- `Cadencia Mínima Exigida (Break-even)`: Punto de equilibrio. Si el proveedor no supera esta cadencia, la operación es inviable.

### 3. Impacto en Operaciones (KPIs)
- `Horas Liberadas`: Tiempo de máquina que queda libre en RPK para otros trabajos.
- `Ahorro Neto Real`: Beneficio económico total tras descontar el coste de subcontratación y logística del coste teórico interno.
- `Plazo de Ejecución`: Días laborables necesarios para completar el lote según la cadencia del proveedor.

### 4. Funcionalidades Especiales
- `📄 PDF`: Genera un reporte profesional con el ADN de diseño RPK.
- `💾 Guardar`: Almacena la simulación en la base de datos local y dispara la descarga automática del PDF.
- `📄 (Histórico)`: Permite regenerar el PDF de una decisión pasada usando el *snapshot* de datos guardado.

## 🚀 Instalación y Uso
1. Descarga el archivo `index.html`.
2. Ábrelo en cualquier navegador moderno.
3. No requiere servidor backend; todo el cálculo es vectorial y se ejecuta en el cliente.

---
*RPK NEXUS v5.5 • INDUSTRY 5.0 CORE • SECURE ANALYTICS*
