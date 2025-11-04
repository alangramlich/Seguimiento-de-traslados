# Seguimiento-de-traslados

# 🚑 Seguimiento Automatizado de Traslados Médicos  
**Automatización de procesos con Power Automate, SharePoint y Outlook**

---

## 🧩 Contexto

En entornos hospitalarios y de atención médica, los traslados de pacientes entre sedes o instituciones deben registrarse cuidadosamente.  
Tradicionalmente, estos registros se reciben por correo electrónico y se gestionan manualmente, lo que dificulta el control de los viajes incluidos dentro del abono convenido con el proveedor y el seguimiento de horarios y tarifas.

---

## ⚙️ Solución Implementada

Desarrollé un flujo de **automatización completa** con **Power Automate**, integrado a **Outlook** y **SharePoint**, capaz de:

1. **Detectar automáticamente correos de traslado** entrantes desde Outlook.  
2. **Extraer la información clave** (fecha, hora, origen, destino, tipo de traslado, proveedor, etc.) utilizando un **modelo de lenguaje (LLM)** que interpreta texto libre del correo.  
3. **Registrar los datos estructurados** en una **lista de SharePoint**, generando un historial centralizado de traslados.  
4. **Realizar seguimiento en tiempo real** del número de traslados realizados dentro del abono mensual convenido.  
5. **Clasificar automáticamente las tarifas** según el horario del traslado (diurno/nocturno/feriado) para el cálculo correcto de pagos.

---

## 🧠 Tecnologías y Componentes

- **Power Automate** – Orquestación del flujo y lógica de negocio.  
- **Outlook Connector** – Lectura automática de correos con criterios de búsqueda.  
- **SharePoint Lists** – Almacenamiento estructurado de registros.  
- **Custom HTTP Request** – Interacción avanzada con la API de SharePoint (GET/POST/UPDATE).  
- **JSON Transformations** – Conversión de salidas del modelo LLM a formato compatible con SharePoint.  
- **IA LLM** – Extracción de información relevante desde correos en lenguaje natural.  

---

## 🧱 Arquitectura del Flujo

```plaintext
📩 Outlook (Correo recibido)
      │
      ▼
🤖 IA LLM → JSON estructurado
      │
      ▼
🔗 Power Automate
      ├── Procesamiento y validación
      ├── Envío HTTP a SharePoint
      └── Notificación de éxito/error
      │
      ▼
📊 SharePoint List (Seguimiento centralizado)
## 🚀 Valor Agregado

- **Automatización total** del registro de traslados, eliminando tareas manuales repetitivas.  
- **Control financiero preciso**, al mostrar en tiempo real cuántos viajes quedan disponibles dentro del abono.  
- **Transparencia operativa**, al visualizar fácilmente horarios y tarifas aplicadas.  
- **Escalabilidad**, permitiendo incorporar nuevos proveedores o sedes sin cambiar la lógica base.  

---

## 📈 Impacto

| Métrica | Antes | Después |
|----------|--------|----------|
| Registro de un traslado | 5–10 min manuales | <1 min automático |
| Control de abonos | Manual, con riesgo de error | Automático y en tiempo real |
| Clasificación por tarifa | Manual, basada en interpretación | Automática, basada en hora |

---

## 🧩 Ejemplo de Registro (datos simulados)

| Fecha | Hora | Origen | Destino | Proveedor | Tipo | Tarifa | Abono restante |
|-------|------|---------|----------|------------|-------|---------|----------------|
| 03/11/2025 | 14:45 | Sede Central | Clínica Norte | Transporte Salud S.A. | Urgente | Diurna | 7/20 |

---

## 💡 Aprendizajes Técnicos

- Diseño de **expresiones complejas en Power Automate** (`Filter Array`, `Parse JSON`, `Compose` dinámicos).  
- Uso de **HTTP Requests personalizados** para manipular listas SharePoint más allá de los conectores estándar.  
- Integración de **modelos LLM** para la interpretación de texto sin formato.  
- Manejo de **control de errores y registros** dentro de flujos productivos.  

---

## 🔮 Próximos Pasos

- Implementar un **panel de Power BI** conectado a la lista SharePoint para visualizar métricas mensuales.  
- Incluir un **sistema de alertas automáticas** cuando se esté por superar el límite del abono.  
- Evaluar integración con **Microsoft Teams** para notificaciones directas.  

---

📘 *Este proyecto fue diseñado como una solución reproducible con datos simulados para proteger la confidencialidad de los procesos internos.*
