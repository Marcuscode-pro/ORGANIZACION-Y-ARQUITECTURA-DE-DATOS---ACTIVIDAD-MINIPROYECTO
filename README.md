<div align="center">

<img src="logo_uees.png" alt="Logo UEES" width="180">

### UNIVERSIDAD DE ESPECIALIDADES ESPÍRITU SANTO
#### FACULTAD DE INGENIERÍA

---

# Control de producción de una fábrica

**Asignatura:** UCOM250 - Organización y Arquitectura de Datos  
**Docente:** Marcos López  
**Grupo:** 3

**Integrantes:**  
MARCOS LOPEZ 

**Fecha:** 19/11/2026  
**2026**

</div>

---

## Descripción

Una fábrica de componentes electrónicos requiere un programa que procese información de su producción diaria. El sistema registra inicialmente **24 unidades** fabricadas y **40 unidades** correspondientes a un segundo registro de producción. A partir de estos datos, se realizan operaciones de suma y resta para obtener valores intermedios relacionados con cantidades acumuladas y diferencias de producción. Algunas instrucciones utilizan resultados generados anteriormente, mientras otras modifican registros que ya han sido consultados.

Después de realizar las operaciones, el sistema verifica el resultado de una suma para establecer el estado del procesamiento. Si el valor calculado es distinto de cero, se almacena el código **303**, que identifica un proceso de producción registrado; si el resultado es cero, se almacena cero. El programa utiliza una posición específica de memoria para conservar este estado y permitir su posterior consulta.

---

## Análisis

*(Identifique los datos proporcionados y almacenados en memoria, indicando qué representa cada uno dentro del escenario y los resultados esperados al finalizar la ejecución).*

<p align="center"><strong>Tabla 1.</strong> Datos del programa</p>

| Datos | Propósito | Operación requerida | Instrucción MIPS |
| :--- | :--- | :--- | :--- |
| **Dato 1** | *(Completar propósito)* | Carga | `lw` |
| **Resultado 1** | *(Completar propósito)* | Multiplicación | `mul` |
| **Resultado 2** | *(Completar propósito)* | Comparación | `seq` |
| **Resultado 3** | *(Completar propósito)* | Almacenamiento | `sw` |

---

## Implementación

```mips
.data
    dato1:      .word 24
    dato2:      .word 40
    resultado1: .word 0
    resultado2: .word 0
    resultado3: .word 0

.text
.globl main

main:
    # Cargar datos desde memoria
    lw $t0, dato1
    lw $t1, dato2

    # Realizar las operaciones correspondientes
    # ...

    # Finalizar ejecución
    li $v0, 10
    syscall

Citas APA - Normas APA. (s.f.). Recuperado el 24 de septiembre de 2026, de https://normas-apa.org/citas/

CiteMaker Cite Web | APA 7th Edn. - Chrome Web Store. (s.f.). Recuperado el 24 de septiembre de 2026, de https://chromewebstore.google.com/detail/citemaker-citeweb-apa-7th/naankklphfojljboaokgfbheobbgenka
