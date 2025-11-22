# Stats Exam Cheat Sheet

This repository contains a LaTeX-based cheat sheet template designed for statistics exams. It is configured for easy editing and building within VS Code.

## 🚀 Getting Started

### Prerequisites

1.  **LaTeX Distribution**: You need a TeX distribution installed on your system.
    *   **macOS**: [MacTeX](https://www.tug.org/mactex/) (or BasicTeX via Homebrew: `brew install --cask basictex`)
    *   **Windows**: [MiKTeX](https://miktex.org/) or [TeX Live](https://www.tug.org/texlive/)
    *   **Linux**: TeX Live (`sudo apt-get install texlive-full` or similar)

2.  **VS Code**: [Visual Studio Code](https://code.visualstudio.com/)

3.  **VS Code Extension**:
    *   [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) (Recommended)

### 🛠️ Setup

1.  **Clone the repository**:
    ```bash
    git clone <your-repo-url>
    cd StatsExam4
    ```

2.  **Open in VS Code**:
    ```bash
    code .
    ```

3.  **Install Extensions**:
    VS Code should recommend installing the LaTeX Workshop extension. If not, search for "LaTeX Workshop" in the Extensions view (`Cmd+Shift+X`) and install it.

## 📝 Usage

### Building the PDF

**Method 1: VS Code (Recommended)**
1.  Open `stats_cheat_sheet.tex`.
2.  Open the Command Palette (`Cmd+Shift+P` or `Ctrl+Shift+P`).
3.  Type `Tasks: Run Task` and select **"Build LaTeX Resume"** (or the default build task).
4.  Alternatively, use the LaTeX Workshop sidebar to build.

**Method 2: Terminal**
You can compile the PDF directly from the terminal using `pdflatex`:
```bash
pdflatex -interaction=nonstopmode -file-line-error stats_cheat_sheet.tex
```

### Editing

*   **Main Content**: Edit `stats_cheat_sheet.tex`.
*   **Structure**: The file uses a 2-column layout with `multicols`.
*   **Formulas**: Use the `\formula{Description}{Math}` command for consistent formatting.
*   **Headers**: Use `\partheading{}` for major sections and `\subhead{}` for subsections.

## 🔧 Troubleshooting

*   **Missing Packages**: If the build fails due to missing packages (e.g., `geometry.sty` not found), you may need to install them using your TeX package manager.
    *   **macOS (BasicTeX)**: `sudo tlmgr install <package_name>` (e.g., `sudo tlmgr install geometry enumitem titlesec`)
*   **Build Errors**: Check the `stats_cheat_sheet.log` file for detailed error messages.
*   **Formatting**: The project is configured to use `latexindent` for formatting. Ensure you have the necessary Perl dependencies installed if formatting fails.

## 📄 License

[MIT](LICENSE)
