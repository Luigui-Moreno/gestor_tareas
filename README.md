# 🚀 Gestor de Tareas CLI

Una aplicación simple y eficaz para gestionar tus tareas diarias directamente desde la línea de comandos (CLI).

![Versión Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![Licencia](https://img.shields.io/badge/licencia-MIT-green)

## ✨ Características

* **CRUD Completo:** Crea, consulta, marca como completada y elimina tareas.
* **Búsqueda:** Encuentra tareas por texto en el título o la descripción.
* **Estadísticas:** Muestra total, completadas y pendientes con su porcentaje.
* **Persistencia de Datos:** Las tareas se guardan automáticamente en un archivo `tareas.json`.
* **Manejo de Errores:** Valida entradas, archivos corruptos y solicita confirmación ante un `Ctrl+C`.

## ⚙️ Instalación y Uso

### Requisitos

* Python 3.8 o superior.
* Sin dependencias externas: se usa únicamente la biblioteca estándar de Python.

### Clonar el repositorio

```bash
git clone https://github.com/Luigui-Moreno/gestor_tareas.git
cd gestor_tareas
```

### Ejecutar la aplicación

```bash
python -m src.main
```

> 💡 En Windows, si la consola muestra caracteres extraños, ejecuta primero `chcp 65001`
> para cambiar la codificación a UTF-8 (la aplicación ya lo hace automáticamente).

## 📖 Ejemplos de Uso

```
========================================
        GESTOR DE TAREAS - CLI
========================================
1. 📋 Ver todas las tareas
2. ➕ Agregar nueva tarea
3. ✅ Marcar tarea como completada
4. 🗑️ Eliminar tarea
5. 🔍 Buscar tarea
6. 📊 Ver estadísticas
7. 💾 Guardar y Salir
----------------------------------------
Selecciona una opción: 2

==================================================
        AGREGAR NUEVA TAREA
==================================================
Título de la tarea: Comprar víveres
Descripción (opcional): Leche, pan y frutas
✅ Tarea 'Comprar víveres' agregada exitosamente.
```

Marcar una tarea como completada (opción 3) o eliminarla (opción 4) se hace indicando
el número que aparece en la lista:

```
LISTA DE TAREAS
1. ⬜ Comprar víveres
   📝 Leche, pan y frutas
   📅 Creada: 2026-08-24

Número de tarea a completar: 1
✅ Tarea 'Comprar víveres' marcada como completada.
```

Al salir (opción 7), las tareas quedan guardadas en `tareas.json` y se cargan
automáticamente en la siguiente ejecución.

## 📁 Estructura del Proyecto

```
mi-gestor-tareas/
├── .gitignore               # Archivos a ignorar por Git
├── README.md                # Descripción del proyecto
├── requirements.txt         # Dependencias (biblioteca estándar)
└── src/                     # Código fuente de la aplicación
    ├── __init__.py          # Convierte src en un paquete
    ├── main.py              # Punto de entrada y orquestador
    ├── tareas.py            # Lógica de negocio de las tareas (CRUD)
    ├── storage.py           # Lectura/escritura del archivo JSON
    └── cli.py               # Interfaz de usuario (menú, inputs, outputs)
```

Responsabilidad de cada módulo:

| Módulo | Responsabilidad |
|--------|-----------------|
| `tareas.py` | Define y opera las tareas (crear, listar, completar, eliminar, buscar, estadísticas) |
| `storage.py` | Persistencia: guardar y cargar datos desde `tareas.json` |
| `cli.py` | Toda la interacción con el usuario (menú, entradas y salidas) |
| `main.py` | Orquesta el flujo principal de la aplicación |

## 🛠️ Conceptos Aplicados

Condicionales, ciclos, funciones, manejo de errores (`try...except`), módulos,
diccionarios, el módulo `json` y buenas prácticas de código (PEP 8).

## ✍️ Autor

Luigui Santiago Moreno Guerra

## 📄 Licencia

Este proyecto se distribuye bajo la licencia MIT.
