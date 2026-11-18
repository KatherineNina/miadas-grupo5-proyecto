# Mi proyecto · De la teoría a la práctica (Sesiones 1 a 3)

**Plantilla espejo del caso guiado Olist** · Módulo: Preparación, Recopilación y Análisis Exploratorio de Datos · MIADAS – UMSA

---

## 👥 Información del Grupo y Autora
* **Grupo:** 5
* **Repositorio del Proyecto:** [GitHub - miadas-grupo5-proyecto](https://github.com/KatherineNina/miadas-grupo5-proyecto)
* **Integrantes:** 
* Katherine Deina Nina Alejo
* Carlos Pacha Cordova
* Boris Ivan  Cruz Torrico
* Gabriel Marcelo Alejo Nina

---

## 📊 Descripción del Conjunto de Datos
Este proyecto utiliza el **E-Commerce Sales Analytics Dataset**, enfocado en el análisis de transacciones, comportamiento de clientes y rendimiento de productos en una plataforma de comercio electrónico.

* **Fuente y URL original:** [Kaggle - E-Commerce Sales and Customer Analytics](https://www.kaggle.com/datasets/datascikhan/e-commerce-sales-and-customer-analytics?select=order_items.csv)

El proyecto trabaja con múltiples tablas relacionadas:
1. **Pedidos (`ecommerce_sales_customer_analytics_150k.csv.gz`):** Contiene la información transaccional y demográfica de cada orden (138,116 registros, 46 columnas).
2. **Clientes (`customer_master.csv`):** Datos maestros de los clientes (25,000 registros, 11 columnas).
3. **Ítems (`order_items.csv.gz`):** Detalle de los productos por cada ítem de pedido (397,569 registros, 12 columnas).
4. **Productos (`product_catalog.csv`):** Catálogo de productos disponibles (1,175 registros, 9 columnas).
5. **Estadísticas (`dataset_statistics.csv`):** Métricas generales del dataset.

---

## 🛠️ Contenido y Estructura del Proyecto

El notebook recorre las fases iniciales de la tubería de datos (*Data Pipeline*), abarcando desde la ingesta hasta la validación de tipos de datos:

### **Paso 0 · Cargar los datos**
* Configuración de la ruta base desde GitHub.
* Importación de las librerías necesarias (`pandas`, `math`) y lectura de los archivos comprimidos y en formato CSV mediante Pandas.
* Verificación inicial de las dimensiones de cada tabla.

### **S1 · Tipos de datos y escalas (Sesión 1)**
* **S1.1 · Primera mirada a los pedidos:**
  * Exploración inicial utilizando los métodos `.head()` y `.info()` para comprender la estructura de las 46 columnas.
  * Identificación automática de columnas con componentes temporales (`order_date`).
  * Conversión de cadenas de texto a formato fecha (`datetime64[ns]`) y validación del rango temporal cubierto por los datos (desde enero de 2021 hasta diciembre de 2025).
* **S1.2 · Corrección de tipos de datos:**
  * Revisión de identificadores y códigos postales (`customer_id`, `order_id`, `customer_postal_code`).
  * Análisis conceptual sobre la diferencia entre variables numéricas cuantitativas y variables cualitativas o de identificación (que aunque contengan dígitos, operan como códigos o categorías).

---

## 🚀 Requisitos e Instalación

Para clonar y explorar el repositorio completo, puedes utilizar el siguiente comando en tu terminal:

```bash
git clone [https://github.com/KatherineNina/miadas-grupo5-proyecto.git](https://github.com/KatherineNina/miadas-grupo5-proyecto.git)
