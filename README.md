# TP Final — Minería y Modelizado de Datos
**IFTS N° 24 | Tecnicatura en Inteligencia Artificial Aplicada | 1° Cuatrimestre 2026**

---

## Descripción

Trabajo práctico final de la materia **Minería y Modelizado de Datos**. Aplica la metodología **CRISP-DM** sobre un dataset de transacciones de una tienda argentina de artículos del hogar (velas, cocina, decoración, aromatización, regalería).

**Objetivos:**
- Segmentar clientes según su comportamiento de compra usando **K-Means**
- Descubrir qué productos se compran juntos usando **APRIORI** (market basket analysis)
- Formular recomendaciones accionables de negocio a partir de los hallazgos

---

## Algoritmos

| Algoritmo | Objetivo | Resultado |
|---|---|---|
| **K-Means** (K=4) | Segmentación de clientes | 4 perfiles: VIP, Activos Frecuentes, Ocasionales, en Riesgo |
| **APRIORI** | Reglas de asociación entre productos | 70 reglas · Lift máximo: 11.86 |

---

## Estructura del repositorio

```
TP_Final/
├── TP_Final_MMD_2026.ipynb           # Notebook fuente (sin outputs)
├── TP_Final_MMD_2026_ejecutado.ipynb # Notebook con todos los outputs
├── online_retail_hogar.csv           # Dataset (9.363 registros, 400 clientes)
├── TP_Final_Informe_v2.pdf           # Informe formal (5 secciones CRISP-DM)
├── TP_Final_Pauta.pdf                # Enunciado original del TP
├── requirements.txt                  # Dependencias del proyecto
└── grafico_*.png                     # Gráficos generados por el notebook
```

---

## Requisitos

- Python 3.10+
- Ver `requirements.txt` para las dependencias exactas

---

## Instalación y uso

### 1. Clonar el repositorio

```bash
git clone https://github.com/hbarrabasqui/MMD_1Q_2026.git
cd MMD_1Q_2026
```

### 2. Crear el entorno virtual

```bash
python -m venv .venv
```

Activar el entorno:

- **Windows (PowerShell):**
  ```powershell
  .\.venv\Scripts\Activate.ps1
  ```
- **Windows (CMD):**
  ```cmd
  .venv\Scripts\activate.bat
  ```
- **Linux / macOS:**
  ```bash
  source .venv/bin/activate
  ```

### 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 4. Ejecutar el notebook

Abrí `TP_Final_MMD_2026.ipynb` en Jupyter Lab o VS Code y ejecutá todas las celdas en orden.  
El notebook genera los gráficos automáticamente en la misma carpeta.

> También podés abrir `TP_Final_MMD_2026_ejecutado.ipynb` para ver los resultados sin necesidad de ejecutar nada.

---

## Dataset

`online_retail_hogar.csv` — dataset sintético generado para este TP.

| Campo | Descripción |
|---|---|
| `NroFactura` | ID de factura |
| `IDCliente` | ID de cliente |
| `Descripcion` | Nombre del producto |
| `Categoria` | Categoría (Velas, Cocina, Decoracion, etc.) |
| `Cantidad` | Unidades compradas |
| `PrecioUnitario` | Precio en ARS |
| `PrecioTotal` | Importe total en ARS |
| `FechaFactura` | Fecha de la transacción |
| `Ciudad` | Ciudad argentina del cliente |

---

## Librerías principales

`pandas` · `numpy` · `matplotlib` · `seaborn` · `scikit-learn` · `mlxtend`
