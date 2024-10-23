# PRÁCTICA 2: Sistema Basado en Conocimiento con Lógica Difusa

Este proyecto implementa un Sistema Basado en Conocimiento (SBC) con un motor de inferencia que utiliza lógica difusa para deducir hechos a partir de una base de reglas. El sistema permite agregar hechos, imprimir la base de conocimiento y realizar consultas mediante razonamiento hacia atrás.

## Requisitos

Antes de ejecutar el proyecto, asegúrate de tener instalado lo siguiente:

- **Python 3.7 o superior** (Python 3.11 recomendado para compatibilidad con `tomllib`)
- Las siguientes bibliotecas de Python:
  - `click`
  - `tomllib` (para Python 3.11+) o `tomli` (para versiones anteriores a Python 3.11)

### Instalación de dependencias

Puedes instalar las dependencias necesarias ejecutando:
pip install click tomli  # Para Python 3.10 o versiones anteriores

## Ejecución del código

El código se puede ejecutar de dos maneras diferentes: con un archivo de configuración `config.toml` o utilizando la configuración por defecto.

### Ejecución con archivo de configuración

Puedes proporcionar un archivo TOML de configuración utilizando la opción `--config`. Esto es útil si deseas personalizar los parámetros de la lógica difusa y los rangos de respuesta:
python p2.py <archivo_bc> --config <archivo_config.toml>
  - `<archivo_bc>`: Nombre del archivo que contiene la base de conocimiento.
  - `<archivo_config.toml>`: Archivo de configuración en formato TOML.

### Ejecución sin archivo de configuración

Si no deseas utilizar un archivo de configuración, el programa aplicará una configuración predeterminada:
python p2.py <archivo_bc>

### Interacción en la consola

Después de ejecutar el programa, puedes interactuar con él utilizando los siguientes comandos en la consola:

  - Agregar un hecho: Para agregar un nuevo hecho a la base de conocimiento. 
    - Formato: add <hecho> [grado_de_verdad]
    - Ejemplo: add profesor [0.8]

  - Realizar una consulta: Para preguntar si un hecho es cierto.
    - Formato: <hecho>?
    - Ejemplo: lluvia?

  - Imprimir la base de conocimiento: Para mostrar todas las reglas y hechos cargados en la base de conocimiento.
    - Comando: print
      
  - Salir del programa: Para finalizar la ejecución.
    - Comando: quit
