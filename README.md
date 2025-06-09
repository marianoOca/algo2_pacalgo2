# 🕹️ Pacalgo2 – Algorithms and Data Structures II

This repository contains the fourth practical assignment for the course **Algorithms and Data Structures II** at the **University of Buenos Aires (UBA), Faculty of Exact and Natural Sciences**, completed during the first semester of 2021.

The project implements the core game logic and data structures for a Pacman-inspired simulation in C++, based on a modular design defined in a previous assignment (TP3).

---

## 📌 Project Summary

The goal of this assignment was to:

- Implement all modules from the TP3 design in C++
- Ensure each module meets complexity requirements
- Respect the given module interfaces, adapting them to the course's test framework
- Organize the project using a modular structure with `.cpp`, `.h`, and `.hpp` files
- Optionally integrate a graphical user interface (GUI)

---

## 🧠 Key Concepts

- Modular programming in C++
- Abstract Data Types (ADTs)
- STL containers (`std::list`, `std::stack`, `std::map`, etc.)
- Template programming (`.hpp` files)
- Interface adaptation and façade patterns
- Algorithmic complexity management

---

## 🗂️ Project Structure

```
📁 src/
├── Fichin.hpp / Fichin.cpp         # Implementation of the main game logic
├── aed2_Fichin.hpp / .cpp          # Interface wrapper for integration/testing
├── Tipos.h                         # Definitions of Coordenada, Direccion, etc.
📁 tests/
├── Unit tests and integration tests
📄 CMakeLists.txt                   # Build configuration
📄 enunciado.pdf                    # Original assignment description (in Spanish)
```

---

## 🚀 How to Build

This project uses **CMake**. You’ll need:
- A C++ compiler (e.g., `g++`)
- CMake 3.10+ installed

Steps to build:

```bash
mkdir build
cd build
cmake ..
make
```

> 💡 The graphical interface is supported only on Linux and includes separate build instructions at the end of this README.

---

## 📚 Academic Context

- 📘 Course: *Algoritmos y Estructuras de Datos II*  
- 🏛️ University: Universidad de Buenos Aires, Facultad de Ciencias Exactas y Naturales  
- 📅 Term: 1st semester of 2021  
- 🧑‍💻 Language: C++

---

## 📎 Notes

- `aed2_Fichin` acts only as a façade. All game logic resides in your own `Fichin` class.
- STL containers were used to model fundamental ADTs (list, stack, queue, map, set).
- Code adheres to complexity and memory safety constraints defined in TP3 and the assignment statement.

---

## 🪪 License

This project is intended for academic and educational purposes only.  
Do not reuse without appropriate attribution.



## Para los tests

### Opción 1: Compilar y Ejecutar desde CLion

### Opción 2:

Compilación:

1. `mkdir build`
2. `cd build`
3. `cmake ..`
4. `make`

Ejecución (desde el inicio del proyecto):

1. `cd build/`
2. `./correrTests`

## Para la interfaz gráfica

### Dependencias

Se necesitan dependencias que pueden ser instaladas en Ubuntu corriendo el siguiente comando en una terminal:

    sudo apt install libsdl2-dev


Las instrucciones no están probadas en Mac OS pero pueden funcionar. Para
Windows, se puede probar instalando la dependencia como se indica arriba dentro
del WSL. En caso de usar Mingw, es necesario instalar la dependencia
`libsdl2-dev` usando la herramienta de dependencias.

Otra opción en Windows (usando MinGW) es descargar SDL desde:
https://www.libsdl.org/download-2.0.php
(En la sección "Development Libraries:" -> "Windows:" -> "SDL2-devel-2.0.14-mingw.tar.gz (MinGW 32/64-bit)")
Luego descomprimir los archivos descargados y copiarlos en la carpeta de instalación de MinGW.

### Para compilar con la interfaz gráfica, descomentar la línea 7 del archivo CMakeLists.txt

#### Opción 1: Compilar y Ejecutar desde CLion

#### Opción 2:

Compilación:

Si ya se creó la carpeta `build`, es necesario borrarla:

    `rm -r build`

Luego:

1. `mkdir build`
2. `cd build`
3. `cmake ..`
4. `make`

## Ejecución:

Desde el inicio del proyecto:

1. `cd build/`
2. `./pacalgo2GUI`

## Solución de problemas

En caso de encontrase con errores al hacer `cmake ..` refiriendo a no encontrar el archivo `FindSDL2.cmake`, puede probarse el proceso anterior luego de descomentar la línea 28 del archivo `CMakeLists.txt`.
