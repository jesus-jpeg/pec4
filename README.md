# PEC4 - Programación para la Ciencia de Datos

## Descripción

Este proyecto implementa un análisis del volumen de agua en el pantano de La Baells a partir de datos abiertos. Se incluyen funcionalidades como carga de datos, limpieza, análisis, visualización y detección de periodos de sequía.

## Estructura del proyecto
Algunos directorios se generarán al correr el código, como son src/img/, doc/ y venv/. Aún así se entregan en la carpeta zip.
```
PEC4_project/
├── src/                            # Código fuente principal
│   ├── main.py                     # Punto de entrada del proyecto
│   ├── img/                        # Gráficas generadas por visualization.py
│   └── modules/                    # Módulos funcionales
│       ├── eda.py
│       ├── cleaning.py
│       ├── analysis.py
│       └── visualization.py
├── tests/
│   ├── test_eda.py
│   ├── test_cleaning.py
│   ├── test_analysis.py
│   └── test_visualization.py
├── doc/                  # Documentación generada con docstrings
├── screenshots/          # Capturas de pantalla de tests, linter y doc
├── data/                 # Dataset descargado manualmente
│   └── quantitat_aigua_embassaments.csv
├── requirements.txt
├── LICENSE
├── README.md
└── .pylintrc
```

## Instalación

1. Crear entorno virtual (una vez dentro de la raíz del proyecto):

```bash
python3 -m venv venv
```

2. Activar el entorno virtual:

- En Linux/macOS:
  ```bash
  source venv/bin/activate
  ```
- En Windows:
  ```bash
  venv\Scripts\activate
  ```

3. Instalar dependencias (ubicándonos en la carpeta del proyecto):

```bash
pip install -r requirements.txt
```

## Ejecución del proyecto

```bash
python src/main.py
```

También se pueden ejecutar ejercicios individualmente con:

```bash
python src/main.py -ex 3
```

## Tests

Para ejecutar los tests:

```bash
cd src
python -m pytest ../tests

### Medir la cobertura de código

Para medir la cobertura y ver un resumen en la terminal (salir de src primero):

```bash
coverage run --source=src/modules -m pytest tests/
```

Para visualizarlo:

```bash
coverage report
```

### Ayuda del script

Puedes ver la ayuda del script principal con:

```bash
python src/main.py --help
```

Esto mostrará las opciones disponibles:

```text
usage: main.py [-h] [-ex EX]

PEC4 - Programación para la Ciencia de Datos

optional arguments:
  -h, --help  show this help message and exit
  -ex EX      Ejecutar un ejercicio específico (1-5). Si no se indica, se ejecutan todos
```
```

## Documentación

Para generar documentación HTML desde los docstrings:

```bash
pdoc src/modules --output-dir doc
```

Para visualizarla en el navegador (elegir submódulos en la barra lateral):

```bash
pdoc src/modules
```

## Linter

Para comprobar el estilo del código con pylint:

```bash
pylint src/modules/*.py src/main.py
```

---

© 2025 Jesús Cabezas Fernández  
Licencia: Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International
