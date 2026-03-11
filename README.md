[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Px-uYaj2)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=22872135&assignment_repo_type=AssignmentRepo)
# Lab02 - Sumador/Restador de 4 bits

## # Integrantes


---

## # Informe

### Indice:
1. [Documentación](#documentación-del-diseño-implementado)
2. [Simulaciones](#simulaciones)
3. [Evidencias de implementación](#evidencias-de-implementación)
4. [Preguntas](#preguntas)
5. [Conclusiones](#conclusiones)
6. [Referencias](#referencias)

---

## ## Documentación del diseño implementado

### ### 1. Sumador/Restador

#### #### 1.1 Descripción
El diseño consiste en una unidad aritmética capaz de realizar sumas y restas de números binarios de 4 bits. Para optimizar el hardware, se utiliza la técnica de Complemento a 2, lo que permite emplear la misma estructura de un sumador para ambas operaciones de forma eficiente.

El funcionamiento se rige por la señal de control Sel:
* Suma (Sel = 0): Las entradas pasan directamente al sumador y el acarreo inicial (Cin) se mantiene en 0.
* Resta (Sel = 1): Se activan las compuertas XOR para invertir los bits de la entrada B (Complemento a 1) y se introduce un '1' lógico a través del acarreo de entrada (Cin), completando así la operación de Complemento a 2.

#### #### 1.2 Diagramas


---

## ## Simulaciones

### ### 1. Simulación del sumador/restador

#### #### 1.1 Descripción
Se realizaron pruebas funcionales en software para verificar que la lógica aritmética fuera correcta. Se probaron casos de suma simple, restas con resultados positivos y restas con resultados negativos para observar el comportamiento de los bits de salida (S) y el acarreo (Cout).

#### #### 1.2 Diagrama

---

## ## Evidencias de implementación


---

## ## Conclusiones

* Optimización de Hardware: Se comprobó que el método de Complemento a 2 es la técnica más eficiente para el diseño de ALUs, ya que permite que un mismo hardware realice múltiples operaciones aritméticas simplemente modificando la lógica de entrada.
* Manejo de Señales de Control: La práctica permitió validar cómo una señal binaria (Sel) puede actuar como una instrucción básica, cambiando dinámicamente el comportamiento de un bloque de hardware en tiempo real.
* Propagación de Acarreo: Se determinó que en un sumador de acarreo en serie (Ripple Carry), el tiempo de respuesta total está limitado por la propagación del bit de acarreo desde el bit menos significativo hasta el más significativo.
* Validación mediante Simulación: El proceso de verificación en software es un paso crítico en la ingeniería electrónica. Permite asegurar que la lógica booleana sea correcta antes de realizar la programación física en la FPGA, minimizando errores en el hardware.
* Escalabilidad: El diseño basado en bloques (instanciando sumadores de 1 bit) demuestra la modularidad de los sistemas digitales, permitiendo que esta misma lógica se extienda fácilmente a sumadores de mayor capacidad (8, 16 o 32 bits).

---

## ## Referencias
