# RPK NEXUS | Simulador Make or Buy v5.5

## 📋 Descripción General
Esta herramienta es un motor de decisión estratégica diseñado para el entorno industrial **RPK NEXUS**. Permite evaluar la viabilidad de subcontratar un lote de producción frente a la fabricación interna, considerando costes horarios, cadencias, logística y plazos de entrega.

## 🛠️ Arquitectura Técnica
- **Frontend**: React 18 (via CDN) con Babel para procesamiento en caliente.
- **Estilos**: TailwindCSS con una paleta personalizada "RPK Dark Mode".
- **Generación de Reportes**: jsPDF + autoTable para la creación de PDFs profesionales.
- **Persistencia**: LocalStorage para el histórico de decisiones.

## 🚀 Instalación y Uso
1. Descarga el archivo `index.html`.
2. Ábrelo en cualquier navegador moderno.
3. No requiere servidor backend; todo el cálculo es vectorial y se ejecuta en el cliente.
