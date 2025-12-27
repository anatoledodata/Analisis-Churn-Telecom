# 📉 Análisis de Evasión de Clientes (Churn) - TelecomX

![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Latest-informational.svg)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualización-orange.svg)

## 🎯 1. Propósito del Análisis
El objetivo de este proyecto es identificar los factores críticos que influyen en la pérdida de clientes (**Churn**) en la empresa TelecomX. Mediante técnicas de Análisis Exploratorio de Datos (EDA), transformamos datos brutos en estrategias accionables para:
* Entender el perfil del cliente que abandona el servicio.
* Identificar umbrales de tiempo críticos (fuga temprana).
* Cuantificar el impacto del precio y los servicios adicionales en la retención.



---

## 📂 2. Estructura del Proyecto
La organización del repositorio garantiza la reproducibilidad y el orden del flujo de trabajo:

* `TelecomX_Data.json`: Dataset original con información demográfica y financiera de los clientes.
* `Analisis_Churn_Telecom.ipynb`: Notebook principal que contiene todo el proceso de limpieza, análisis y visualización de datos.
* `README.md`: Documentación completa del proyecto (este archivo).

---

## 📊 3. Gráficos e Insights Clave

### A. El "Muro de los 10 meses"
Mediante un análisis de distribución de la antigüedad (`tenure`), descubrimos que el **50% de las cancelaciones ocurren antes de los 10 meses**.
> **Insight:** Existe una "fuga infantil". La estrategia de retención debe enfocarse agresivamente en el primer año de vida del cliente.



### B. Sensibilidad al Precio
El análisis de cajas (Boxplots) reveló una diferencia significativa en los cargos mensuales:
* **Clientes Leales (No Churn):** Media de $61.27.
* **Clientes Fugados (Churn):** Media de $74.44.
> **Insight:** El precio alto es un factor directo de expulsión. Los clientes con facturas superiores a los $70 presentan un riesgo de fuga significativamente mayor.

### C. Escudos de Retención
Calculamos un diferencial de servicios para identificar "Servicios Ancla":
* **Seguridad Online y Soporte Técnico:** Los clientes que cuentan con estos servicios presentan una tasa de fuga drásticamente inferior al promedio.
* **Alerta:** Los métodos de pago manuales (Electronic Check) están altamente correlacionados con el abandono.

* 

---

## 🛠️ 4. Instrucciones de Ejecución

Este proyecto está diseñado para ejecutarse de forma sencilla en la nube:

1. **Abrir en Google Colab:** Haz clic en el botón "Open in Colab" que aparece en la parte superior del archivo `.ipynb`.
2. **Conexión de Datos:** El notebook consume automáticamente el archivo `TelecomX_Data.json` desde este repositorio mediante una URL Raw, eliminando la necesidad de cargas manuales.
3. **Ejecución:** En el menú superior de Colab, selecciona `Entorno de ejecución` > `Ejecutar todas`.
4. **Dependencias:** El entorno utiliza las librerías estándar de Ciencia de Datos: `pandas`, `seaborn` y `matplotlib`.

---

## 💡 5. Recomendaciones Estratégicas
1. **Programa de Fidelización Temprana:** Implementar campañas proactivas entre los meses 6 y 10 para cruzar el umbral crítico de abandono.
2. **Promoción de Servicios Ancla:** Incentivar la adopción de `OnlineSecurity` y `TechSupport` como herramientas de retención.
3. **Optimización de Pagos:** Ofrecer incentivos para migrar a clientes de "Cheque Electrónico" hacia métodos de pago automáticos para reducir la fricción mensual.

---
**Proyecto desarrollado como parte de un análisis de Ciencia de Datos para la optimización de retención de clientes.**
