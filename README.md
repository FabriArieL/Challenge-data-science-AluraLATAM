# Análisis de Evasión de Clientes (Churn)

Este repositorio contiene un análisis completo del fenómeno de **Churn** (evasión de clientes) utilizando Python, pandas y matplotlib.  
El objetivo principal es **identificar patrones que expliquen el abandono** y generar **recomendaciones para mejorar la retención**.

---

## 📌 Contenido del Proyecto

1. **Introducción**
2. **Limpieza y Tratamiento de Datos**
3. **Análisis Exploratorio de Datos (EDA)**
4. **Conclusiones e Insights**
5. **Recomendaciones**
6. **Próximos pasos**

---

## 1️⃣ Introducción

El análisis se centra en entender las causas del **Churn**, es decir, el abandono de clientes, utilizando un dataset tipo Telco.  
Se define *Churn* como la variable binaria que indica si un cliente **abandonó** (1) o **permaneció** (0).

**Objetivos:**
- Explorar los datos y evaluar su calidad.
- Identificar variables clave asociadas al abandono.
- Proponer estrategias basadas en los hallazgos.

---

## 2️⃣ Limpieza y Tratamiento de Datos

Pasos principales:
- **Importación y revisión** de tipos de datos.
- **Tratamiento de valores nulos y duplicados**.
- **Estandarización** de categorías (Yes/No, Male/Female, etc.).
- **Conversión de datos** a formatos correctos (numéricos, categóricos, fechas).
- Creación de **variables derivadas** como *antigüedad en meses* y *ingresos totales*.
- Preparación de variables para el análisis exploratorio.

---

## 3️⃣ Análisis Exploratorio de Datos (EDA)

Incluye:
- **Balance de clases** (Churn vs No Churn).
- **Distribución de variables numéricas** segmentadas por Churn:
  - Tenure
  - MonthlyCharges
  - TotalCharges
- **Correlaciones numéricas** con Churn.
- **Gráficos de barras apiladas** para variables categóricas clave:
  - Contract
  - PaymentMethod
  - InternetService
  - TechSupport
  - OnlineSecurity

Ejemplo de gráfico:  

![Balance de Clases](images/balance_churn.png)

---

## 4️⃣ Conclusiones e Insights

- Los clientes con **menor antigüedad** tienen mayor probabilidad de churn.
- Contratos **mensuales** presentan mayor churn que los **anuales/bianuales**.
- El método **Electronic check** está asociado a mayor churn.
- Cargos mensuales altos sin servicios de valor añadido incrementan el riesgo.

---

## 5️⃣ Recomendaciones

1. **Retención de alto riesgo**: descuentos a clientes con baja antigüedad y contrato mensual.
2. **Migración a contratos largos**: beneficios al pasar a contratos anuales/bianuales.
3. **Mejorar valor percibido**: incluir TechSupport/OnlineSecurity en planes con alto costo mensual.
4. **Onboarding proactivo**: seguimiento intensivo los primeros 90 días.
5. **Alertas tempranas**: score de riesgo integrado en CRM.

---

## 🚀 Requisitos

Para ejecutar el notebook necesitarás:
- Python 3.8+
- pandas
- numpy
- matplotlib
- jupyter

Instalar dependencias:
```bash
pip install -r requirements.txt

📂 Estructura del repositorio
├── README.md
├── notebook.ipynb
├── images/
│   ├── balance_churn.png
│   ├── tenure_distribution.png
│   └── contract_churn.png
├── data/
│   └── churn_dataset.csv
└── requirements.txt
