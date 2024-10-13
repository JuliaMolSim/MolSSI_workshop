# Pre-Workshop: Julia, Jupyter, and VS Code Setup Guide for Julia Programming

## 1. Install Julia (via JuliaUp)
`JuliaUp` is a convenient way to install and manage Julia versions.

### Install JuliaUp
1. **Windows**:
    - Go to the Microsoft Store and search for **Julia**.
    - Install **Julia** from the official Julia team (this uses `JuliaUp` for easy version management).
2. **Linux**:
    - Open your terminal and run the following command to install `JuliaUp`:
    ```bash
    curl -fsSL https://install.julialang.org | sh
    ```
3. **macOS**:
    - Open your terminal and run:
    ```bash
    brew install juliaup
    ```
    - Make sure you have [Homebrew](https://brew.sh/) installed first.
    
### Manage Julia Versions
Once installed, you can manage Julia versions easily with `juliaup`. For example:
- To install the latest stable Julia version:
    ```bash
    juliaup add stable
    ```
- To set a specific version as default:
    ```bash
    juliaup default <version>
    ```
- To launch Julia:
    ```bash
    julia
    ```

## 2. Install Jupyter (with Julia Kernel)
Jupyter allows you to write and run Julia code interactively.

### Install Jupyter
1. Install Python and `pip` if you don't have them. You can get Python from the [official website](https://www.python.org/downloads/).
2. Use `pip` to install Jupyter:
    ```bash
    pip install jupyterlab
    ```

Alternatively, you can install Jupyter via [Anaconda](https://www.anaconda.com/products/individual), which bundles Python and other scientific packages.

### Install Julia Kernel in Jupyter
1. Open Julia and add the IJulia package, which integrates Julia with Jupyter:
    ```julia
    using Pkg
    Pkg.add("IJulia")
    ```

2. After installation, run the following command to build the Jupyter kernel for Julia:
    ```julia
    using IJulia
    notebook()
    ```
    This will open Jupyter in your browser, and you'll now have the option to create a Julia notebook.

## 3. Install VS Code
Visual Studio Code (VS Code) is a lightweight and powerful code editor that supports many languages, including Julia.

1. Go to the [Visual Studio Code website](https://code.visualstudio.com/) and download the latest version for your operating system.
2. Install VS Code by following the platform-specific instructions.

### 4. Install Julia Extension for VS Code
1. Open VS Code.
2. Go to the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of the window, or use the shortcut `Ctrl + Shift + X` (Windows/Linux) or `Cmd + Shift + X` (macOS).
3. In the Extensions search bar, type **Julia**.
4. Find the **Julia** extension by **Julia Language Support** and click **Install**.
5. VS Code should automatically detect the Julia installation. If not, go to the VS Code settings (`Ctrl + ,`) and set the path for Julia manually by searching for "Julia: Executable Path" and specifying the path to the `julia` binary.

### 5. Install Jupyter Extension in VS Code
1. In VS Code, go to the Extensions view again.
2. Search for **Jupyter** and install the **Jupyter** extension.
3. Once installed, you can open Jupyter notebooks (`.ipynb` files) directly within VS Code and execute Julia code.

### 6. Using Julia with Jupyter in VS Code
1. Create a new Jupyter notebook by pressing `Ctrl + Shift + P` to open the Command Palette, then search for **Jupyter: Create New Blank Notebook**.
2. Select Julia as the kernel (if it doesn't appear, ensure you have followed the steps above to install IJulia).
3. You can now run Julia code in the notebook cells inside VS Code.

## 7. Additional Tools
- **Linting and Static Analysis**: The Julia extension for VS Code also provides linting, syntax highlighting, and static analysis features to help with code quality.
- **Debugger**: The Julia extension also comes with a built-in debugger. You can access it via the debug icon on the side panel in VS Code.

---

With these steps completed, you should now have a fully functional Julia environment within VS Code, with Jupyter support for interactive computing!

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
