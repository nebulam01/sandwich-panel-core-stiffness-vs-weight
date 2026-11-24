# Sandwich Panels — Core Patterns & Stiffness vs. Weight

An interactive **Google Colab** engineering tool built with `ipywidgets`, `NumPy`, `Pandas`, and `Matplotlib` to visualize 2D sandwich panel cross-sections across different core patterns and plot **bending stiffness (`EI_eq`) against panel weight (`N`)**.

## Overview

Sandwich panels pair thin, stiff face sheets with a lightweight core so that increasing core thickness raises bending stiffness rapidly with a modest weight penalty[cite: 7]. This notebook lets you explore how different core topologies and face-sheet materials affect total weight, equivalent bending stiffness, and stiffness-to-weight efficiency.

### Supported Core Patterns
- **Honeycomb**
- **Corrugated (Wave)**
- **Truss Core**
- **Foam Core**

### Supported Face Sheet Materials
- **Aluminum 6061-T6**
- **Carbon Fiber (UD)**
- **PLA (3D Print)**

## Key Features

- **Interactive English UI (`ipywidgets`):** Adjust face material, core pattern, face thickness, core thickness, cell/pitch size, and panel length/width, then update the view live or via button.
- **2D Sandwich Panel Cross-Section Drawing:** Displays a schematic 2D cross-section of the selected core pattern sandwiched between top and bottom face sheets.
- **Stiffness vs. Weight Trade-Off Graph:** Plots bending stiffness (`EI_eq [N·m²]`) against panel weight (`[N]`) across core thicknesses (`4–40 mm`) for all four core patterns and marks the active operating point.
- **Efficiency & Design Summary Card:** Reports panel mass (`g`), weight (`N`), equivalent bending stiffness (`EI_eq`), stiffness-to-weight ratio (`N·m²/N`), and core-specific design notes.

## How to Run in Google Colab

1. Open a new notebook in [Google Colab](https://colab.research.google.com/).
2. Paste the sandwich panel code into a code cell and run it.
3. Adjust the sliders and dropdowns to inspect the 2D core geometry and the stiffness-vs.-weight curves.

## Engineering Notes

- Equivalent bending stiffness combines face-sheet parallel-axis stiffness with core shear/bending contribution across the panel width.
- Conceptual trade-off studies help compare core architectures early in design and should be paired with detailed shear/buckling checks and FEA for structural hardware.
