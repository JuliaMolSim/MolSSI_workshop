# Introduction to Julia -- MolSSI Workshop

## Install Julia

- Windows : 
```sh
winget install julia -s msstore
```
- MacOS\Linux: 
```sh
curl -fsSL https://install.julialang.org | sh
```


### [Syntax Tutorial](syntax.ipynb)

# Agenda

### Introduction to Julia

#### Setting Up a Julia Environment:

1. Step-by-step guide to setting up Julia in different environments:
  - VSCode: Installing the Julia extension and configuring the workspace.
  - Jupyter Notebooks: Setting up Julia kernels for interactive computing.
  - REPL: Introduction to Julia’s command-line interface for quick tests and explorations.

2. Julia Syntax Essentials
  - Core Syntax:
    - Functions: Defining and calling functions, using multiple return values.
    - Loops & Conditionals: Understanding control flow with for, while, if, and else.
    - Variables & Types: Introduction to Julia’s type system, variable scope, and immutability.
    - Structs: Creating custom types with struct for more complex data structures.
    - Broadcasting: Efficiently applying functions across arrays and other collections.
    - Unicode Characters: Using Unicode for clearer and more readable code.
    - File I/O: Basics of reading from and writing to files.
    
3. Leveraging Julia’s Power
  - Why Julia?
    - Overview of Julia’s key features: speed, ease of use, and suitability for scientific computing.
    - Comparison with other languages like Python and MATLAB in terms of performance and syntax.
  - Multiple Dispatch:
    - Explanation of Julia’s unique multiple dispatch system, with examples to showcase its flexibility and performance benefits.
  - Package Manager (Pkg):
    - Introduction to managing Julia packages: adding, updating, and removing packages.
    - Quick look at useful development tools provided by the package manager.

4. Working with Numerical Data
  - Key Packages:
    - LinearAlgebra: Essential functions for matrix operations and linear algebra.
    - DataFrames: Handling tabular data, similar to pandas in Python.
    - Unitful: Managing physical units in calculations to avoid errors.
    - Distributions: Working with statistical distributions for simulations and data analysis.
        - Focus on the main functions related to stats.
    
5. Plotting:
  - Introduction to plotting in Julia using Plots.jl, with examples of common plots.

6. Benchmarking and Optimizing Code
  - BenchmarkTools.jl: How to measure code performance accurately.
  - Array Views & Memory Allocations: Techniques to reduce memory usage and improve performance.
  - Type Stability: Understanding and ensuring type stability for faster execution.

7. Advanced Topics
  - Basic Parallelization:
    - Introduction to multi-threading in Julia, with simple examples to parallelize loops and tasks.
  - Basic GPU Programming:
    - Overview of high-level interfaces for GPU computing, making it accessible without deep GPU programming knowledge.
  - AutoDiff:
    - Brief introduction to automatic differentiation using FastDifferentiation.jl for optimization and machine learning applications.

8. Conclusion & Next Steps
  - What to Expect in the Next Workshop:
    - Teasers of more advanced topics like Molecular Dynamics (using Molly) and Density Functional Theory (using DFTK).
