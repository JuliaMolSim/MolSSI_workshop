# Introduction to Julia -- MolSSI Workshop

This repo houses the content for the Sunday afternoon Intro to Julia session of the [MolSSI workshop](https://juliamolsim.github.io/molssi_workshop/) to be hosted at CMU on October 20, 2024. Below find the agenda, with relevant notebooks linked and a summary of topics to expect in each section.

## 1. Introduction to Julia

A nice resource to be aware of in this general category is the [first post of Modern Julia Workflows](https://modernjuliaworkflows.org/writing/), which covers many similar topics: installing Julia, the REPL, IDE setup, environments, etc., as well as a few we likely won't have time to go into in much depth such as debugging tools.

### Install Julia

Windows: 
```sh
winget install julia -s msstore
```
MacOS\Linux: 
```sh
curl -fsSL https://install.julialang.org | sh
```

### Setting Up an IDE:

Step-by-step guide to setting up Julia in different environments:
  - **VSCode**: Installing the Julia extension and configuring the workspace.
  - **Jupyter**: Setting up Julia kernels for interactive computing.
  - **REPL**: Introduction to Julia’s command-line interface for quick tests and explorations.

## 2. [Julia Syntax Essentials:](syntax.ipynb)
  - **Variables & Types**: Declaring variables (including with fun Unicode symbols!), introduction to Julia’s type system, variable scope, and immutability.
  - **Functions**: Defining and calling functions, using multiple return values.
  - **Loops & Conditionals**: Understanding control flow with for, while, if, and else.
  - **Structs**: Creating custom types with struct for more complex data structures.
  - **Broadcasting**: Efficiently applying functions across arrays and other collections.
  - **File I/O**: Basics of reading from and writing to files.
    
## 3. [Leveraging Julia’s Power](whyjulia.ipynb)
  - Why Julia?
    - Overview of Julia’s key features: speed, ease of use, and suitability for scientific computing.
    - Comparison with other languages like Python and MATLAB in terms of performance and syntax.
  - Multiple Dispatch:
    - Explanation of Julia’s unique multiple dispatch system, with examples to showcase its flexibility and performance benefits.
    - Interfaces (demo, examples)
  - Package Manager (Pkg):
    - Introduction to managing Julia packages: adding, updating, and removing packages.
    - Quick look at useful development tools provided by the package manager.

## 4. [Working with Numerical Data](numericaldata.ipynb)
Key Packages:
  - **LinearAlgebra**: Essential functions for matrix operations and linear algebra.
  - **DataFrames**: Handling tabular data, similar to pandas in Python.
  - **Unitful**: Managing physical units in calculations to avoid errors.
  - **Distributions**: Working with statistical distributions for simulations and data analysis.
  - **DelimitedFiles**: for handling file I/O with simple formats such as CSV
    
## 5. Plotting:
Introduction to plotting in Julia using Plots.jl, with examples of common plots and constructs like plot recipes (may be integrated into prior section).

## 6. [Benchmarking and Optimizing Code:](optimization.ipynb)
  - BenchmarkTools.jl: How to measure code performance accurately.
  - Array Views & Memory Allocations: Techniques to reduce memory usage and improve performance.
  - Type Stability: Understanding and ensuring type stability for faster execution.

## 7. [Advanced Topics:](advanced.ipynb)
  - **Basic Parallelization**: Introduction to multi-threading in Julia, with simple examples to parallelize loops and tasks.
  - **Basic GPU Programming**: Overview of high-level interfaces for GPU computing, making it accessible without deep GPU programming knowledge.
  - **Automatic Differentiation (AD)**:Brief introduction to automatic differentiation and some of its implementations in Julia

## 8. Conclusion & Next Steps
What to expect in the rest of the workshop: If time, some teasers of more advanced topics like Molecular Dynamics (using Molly) and Density Functional Theory (using DFTK).
