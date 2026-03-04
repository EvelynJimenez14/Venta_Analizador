# Reporte

## 1. Introducción
El presente proyecto documenta el diseño e implementación de una aplicación modular orientada al análisis de datos de ventas. El sistema se fundamenta en el paradigma de Programación Orientada a Objetos (POO) para garantizar una arquitectura escalable, mantenible y reproducible, cumpliendo con los estándares requeridos en la asignatura de Desarrollo de Aplicaciones para Análisis de Datos.

## 2. Objetivos del Sistema
- Implementar un pipeline de procesamiento que incluya la extracción, limpieza y transformación de datos.
- Asegurar la integridad de la información mediante mecanismos de encapsulamiento y validación de atributos.
- Facilitar la toma de decisiones a través de un módulo de visualización y generación de reportes estadísticos.

## 3. Arquitectura de Software
La aplicación se organiza bajo una estructura modular que separa las responsabilidades de la siguiente manera:

### 3.1. Modelado de Entidades (`modulos/modelos.py`)
Contiene las definiciones de las clases base y derivadas. Se hace uso de clases abstractas para establecer plantillas de productos y clientes, asegurando que cada objeto cumpla con una estructura predefinida.

### 3.2. Lógica de Procesamiento (`modulos/procesamiento.py`)
Módulo encargado de la ingesta de datos desde fuentes externas (archivos CSV). Incluye algoritmos para la limpieza de registros, tratamiento de valores nulos y cálculos de indicadores clave de rendimiento (KPIs).

### 3.3. Utilidades y Control de Flujo (`modulos/utils.py`)
Espacio dedicado a la implementación de decoradores de Python. Estos se utilizan para establecer precondiciones de seguridad, auditoría de procesos y validación de tipos de datos en tiempo de ejecución.

### 3.4. Orquestación (`main.py`)
Punto de entrada único de la aplicación que coordina la interacción entre los modelos, los procesadores y la capa de salida.

## 4. Metodología de Implementación de POO
Para el desarrollo de este sistema se han aplicado los siguientes pilares:
- **Abstracción**: Modelado de las características esenciales de los activos comerciales.
- **Encapsulamiento**: Protección del estado interno de los objetos mediante atributos privados y métodos controladores (Setters/Getters).
- **Polimorfismo**: Redefinición de métodos para adaptar el cálculo de totales y descuentos según el tipo de producto o categoría de cliente.

