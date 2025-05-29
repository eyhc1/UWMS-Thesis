# Programmable System for Laser Control of Trapped-Ion Experiments

This repository contains the LaTeX source code for my Master's thesis.

## Thesis Overview

This thesis presents an FPGA-based laser control system designed for trapped-ion quantum computing experiments. The system delivers precise pulse waveforms using a Xilinx Zynq platform, providing 32 pulsed and 32 static voltage signals with sub-microsecond timing accuracy.

## Building the PDF

### Prerequisites

You'll need a LaTeX distribution installed on your system:

#### Windows
- Install [MiKTeX](https://miktex.org/) or [TeX Live](https://www.tug.org/texlive/)

#### macOS
- Install [MacTeX](https://www.tug.org/mactex/)

#### Linux (Ubuntu/Debian)
```bash
sudo apt-get install texlive-full
```

#### Linux (Fedora/RHEL)
```bash
sudo dnf install texlive-scheme-full
```

### Required LaTeX Packages

The thesis uses the following packages (most are included in full LaTeX distributions):
- `amsmath` - Mathematical typesetting
- `hyperref` - Hyperlinks and PDF metadata
- `graphicx` - Image inclusion
- `float` - Float positioning
- `tabularx` - Enhanced table formatting
- `multirow` - Multi-row table cells
- `alltt` - Verbatim text with LaTeX commands

### Building Instructions

#### Method 1: Command Line Using latexmk (Recommended)

1. **Clone or download the repository**
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Compile the thesis**
   ```bash
   latexmk -auxdir=_build -xelatex
   ```

   **Note:** This project must use xelatex to compile

3. **Clean up auxiliary files (optional)**
   ```bash
   # Remove temporary files
   rm *.aux *.bbl *.blg *.log *.toc *.lof *.lot *.out
   ```

#### Method 2: Using a LaTeX Editor

Popular LaTeX editors with GUI:
- **TeXstudio** (Cross-platform)
- **TeXworks** (Cross-platform)
- **Overleaf** (Web-based)
- **VS Code** with LaTeX Workshop extension

1. Open `uwthesis.tex` in your preferred editor
2. Build using the editor's build function (usually F5 or Ctrl+R)
3. The editor should automatically handle multiple compilation passes

### Troubleshooting

#### Missing Figures
If you encounter errors about missing figures, ensure all image files are present in the `figures/` directory as referenced in the chapter files.

#### Font or Package Errors
If you encounter missing package errors:
```bash
miktex-console # Use package manager to install missing packages
```

## Document Structure

The thesis is organized into the following chapters:

1. **Introduction** - Project motivation and overview
2. **Background** - Laser trapped-ion experiments and hardware description
3. **Block Architecture** - Detailed system design and implementation
4. **Metrics for Evaluation** - Testing methodology and validation
5. **System Integration** - Complete system architecture
6. **Outcome and Results** - Simulation and experimental results
7. **Discussion** - Analysis of limitations and future improvements
8. **Conclusion** - Summary and contributions

## Customization

### Modifying Content
- Edit individual chapter files in the `chapters/` directory
- Update bibliography entries in `uwthesis.bib`
- Add new figures to the `figures/` directory and reference them in the text

### Thesis Metadata
Key thesis information is defined in `uwthesis.tex`:
```latex
\Title{Programmable System for Laser Control of Trapped-Ion Experiments}
\Author{Haochen "Eric" Yu}
\Year{2025}
\Program{Electrical and Computer Engineering}
\Chair{Scott Hauck}{}{Department of Electrical and Computer Engineering}
\Signature{Sara Mouradian}
```

### University of Washington Formatting
This thesis uses the official UW thesis class (`uwthesis.cls`) which ensures compliance with university formatting requirements.

## License

This thesis document is subject to University of Washington academic regulations. The LaTeX class file (`uwthesis.cls`) is licensed under the Apache License, Version 2.0.