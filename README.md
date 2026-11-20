<div align="center">

<img src="https://upload.wikimedia.org/wikipedia/commons/3/3e/UEES_logo.png" alt="Logo UEES" width="130">

# UNIVERSIDAD DE ESPECIALIDADES ESPÍRITU SANTO
### FACULTAD DE INGENIERÍA

---

# 🏭 Control de Producción de una Fábrica
**Proyecto de Ensamblador MIPS — Arquitectura de Computadores**

[![Universidad](https://img.shields.io/badge/Universidad-UEES-blue?style=flat-square)](https://uees.edu.ec)
[![Asignatura](https://img.shields.io/badge/Asignatura-UCOM250%20--%20Organización%20y%20Arquitectura%20de%20Datos-darkblue?style=flat-square)](#)
[![Docente](https://img.shields.io/badge/Docente-Marcos%20López-blueviolet?style=flat-square)](#)
[![Lenguaje](https://img.shields.io/badge/Lenguaje-MIPS%20Assembly-orange?style=flat-square)](#)
[![Grupo](https://img.shields.io/badge/Grupo-03-brightgreen?style=flat-square)](#)

</div>

---

## 📌 Datos Informativos

* **Asignatura:** UCOM250 - Organización y Arquitectura de Datos
* **Docente:** ALLAN ROBERTO AVENDANO SUDARIO
* **Grupo:** Grupo 3 
* **Integrantes:**
  * 👤 Marcos López *
* **Fecha de entrega:** 19/11/2026
* **Año académico:** 2026

---

## 📖 Descripción del Problema

Una fábrica de componentes electrónicos requiere un programa que procese información de su producción diaria. El sistema registra inicialmente 24 unidades fabricadas y 40 unidades correspondientes a un segundo registro de producción. A partir de estos datos, se realizan operaciones de suma y resta para obtener valores intermedios relacionados con cantidades acumuladas y diferencias de producción. Algunas instrucciones utilizan resultados generados anteriormente, mientras otras modifican registros que ya han sido consultados.

Después de realizar las operaciones, el sistema verifica el resultado de una suma para establecer el estado del procesamiento. Si el valor calculado es distinto de cero, se almacena el código 303, que identifica un proceso de producción registrado; si el resultado es cero, se almacena cero. El programa utiliza una posición específica de memoria para conservar este estado y permitir su posterior consulta.


---

## 📊 Análisis

> Identificación de datos proporcionados, variables en memoria, operaciones requeridas y resultados esperados.

### Tabla 1. Datos del programa

| Elemento | Descripción / Propósito | Operación Requerida | Instrucción MIPS |
| :--- | :--- | :---: | :---: |
| **Dato 1** | Primer registro de producción (24 unidades) | Carga | `lw` |
| **Dato 2** | Segundo registro de producción (40 unidades) | Carga | `lw` |
| **Resultado 1** | Cantidades acumuladas / operaciones intermedias | Multiplicación | `mul` |
| **Resultado 2** | Comparación de condición / estado de proceso | Comparación | `seq` |
| **Resultado 3** | Almacenamiento del código de estado (303 o 0) | Almacenamiento | `sw` |

---

## 💻 Implementación

### Código Fuente en Ensamblador MIPS

```mips
.data
    dato1:      .word 24         # Registro inicial de 24 unidades fabricadas
    dato2:      .word 40         # Segundo registro de 40 unidades
    resultado1: .word 0          # Resultado intermedio
    resultado2: .word 0          # Comparación de estado
    resultado3: .word 0          # Almacenamiento de código de estado (303 o 0)

.text
.globl main

main:
    # 1. Cargar datos desde memoria
    lw $t0, dato1                # Carga dato1 (24) en $t0
    lw $t1, dato2                # Carga dato2 (40) en $t1

    # 2. Realizar las operaciones correspondientes
    # [Escribe aquí las operaciones de suma, resta y multiplicación de tu algoritmo]
    
    # 3. Verificación de estado (Suma != 0 -> 303, else 0)
    # [Escribe aquí las instrucciones de salto/comparación]

    # 4. Almacenamiento en memoria
    sw $t2, resultado3           # Guarda el estado final en resultado3

    # Finalizar el programa de forma limpia
    li $v0, 10
    syscall
