# Introduction to Julia -- MolSSI Workshop

This repo houses the content for the Sunday afternoon Intro to Julia session of the [MolSSI workshop](https://juliamolsim.github.io/molssi_workshop/) to be hosted at CMU on October 20, 2024. Below find the agenda, with relevant notebooks linked and a summary of topics to expect in each section.

## 0. Pre-workshop setup instructions

### 0.1. Install Julia (via JuliaUp)
[Juliaup](https://github.com/JuliaLang/juliaup) is a convenient way (and also now the officially recommended one) to install and manage Julia versions. As with most things, the installation process depends on your operating system:

#### Windows: 
Two options: Either
1.  In the command prompt, run 
    ```bat
    winget install julia -s msstore
    ```
    Or, if you don't like the Windows command prompt,

2. Go to the Microsoft Store and search for **Julia**. Install the offering from the official Julia team.

#### Linux or macOS:
On either platform, you can open a terminal and run
```bash
curl -fsSL https://install.julialang.org | sh
```

As a Mac-only alternative, if you have [Homebrew](https://brew.sh/) installed, you can also open your terminal and run `brew install juliaup`.
    

### 0.2. Install VS Code
Visual Studio Code (VS Code) is now the recommended IDE to use with Julia. To install it:

1. Go to the [Visual Studio Code website](https://code.visualstudio.com/) and download the latest version for your operating system.
2. Install VS Code by following the platform-specific instructions.

### 0.3. Install Julia Extension for VS Code
1. Open VS Code.
2. Go to the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of the window, or use the shortcut `Ctrl + Shift + X` (Windows/Linux) or `Cmd + Shift + X` (macOS).
3. In the Extensions search bar, type **Julia**.
4. Find the **Julia** extension by **Julia Language Support** and click **Install**.
5. VS Code should automatically detect the Julia installation. If not, go to the VS Code settings (`Ctrl + ,`) and set the path for Julia manually by searching for "Julia: Executable Path" and specifying the path to the `julia` binary.

### 0.4. Install Jupyter Extension in VS Code
1. In VS Code, go to the Extensions view again.
2. Search for **Jupyter** and install the **Jupyter** extension.
3. Once installed, you can open Jupyter notebooks (`.ipynb` files) directly within VS Code and execute Julia code.

NOTE: We will mostly be demonstrating notebooks from within VS Code. If you prefer to run Jupyter notebooks in your browser instead of in VS Code, you can do that too. For this, you will need the [IJulia](https://github.com/JuliaLang/IJulia.jl) to give Jupyter access to a Julia kernel.

### 0.5 Download this repository!
To run things locally, clone this repository with your favorite git client. Or, just download the repo directly using the button on the top right.

## 1. Introduction to Julia

A nice resource to be aware of in this general category is the [first post of Modern Julia Workflows](https://modernjuliaworkflows.org/writing/), which covers many similar topics: installing Julia, the REPL, IDE setup, environments, etc., as well as a few we likely won't have time to go into in much depth such as debugging tools.

* Making sure everyone completed the pre-setup and has a working environment
* Introduction to the Julia REPL and its various modes, particularly `pkg>` mode for managing environments and packages

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
