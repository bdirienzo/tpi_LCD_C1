# Sistema de Procesamiento de Compras del Supermercado

**Materia:** Computación I  
**Carrera:** Licenciatura en Ciencia de Datos (LCD)  
**Año:** 3er año  
**Alumno:** Bernardo Di Rienzo  
**Fecha de entrega:** 10 de junio de 2026

Sistema desarrollado en Python para el procesamiento y análisis de datos de compras de un supermercado. Implementa un flujo de trabajo con Integración Continua mediante GitHub Actions.

## Estructura del Proyecto

```
├── app/
│   └── main.py               # Código fuente del sistema
├── data/
│   └── compras_desordenado.csv  # Dataset de compras
├── test/
│   └── test_main.py          # Tests unitarios
├── .github/
│   └── workflows/
│       └── ci.yml            # Pipeline de CI
├── conftest.py               # Configuración de pytest
└── requirements.txt          # Dependencias
```

## Funcionalidades

- Lectura de datos de compras desde archivos CSV
- Ordenamiento de registros por sucursal y producto
- Procesamiento con corte de control por sucursal
- Cálculo de totales, producto más vendido y peor vendido por sucursal
- Reporte consolidado de ventas

## Requisitos

- Python 3.12+
- pytest

## Instalación

```bash
pip install -r requirements.txt
```

## Ejecución

```bash
python app/main.py
```

## Tests

```bash
python -m pytest test/ -v
```

## Integración Continua

El pipeline de CI se ejecuta automáticamente en cada Pull Request hacia `main`. Instala las dependencias y corre la suite de tests. El merge está bloqueado si algún test falla.
