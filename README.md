# LaTeX CV Template

A LaTeX CV/resume template intended to be compiled locally with **XeLaTeX** using **LaTeX Workshop** in VS Code or VSCodium.

## Requirements

The template uses:

* XeLaTeX
* `latexmk`
* `fontspec`
* Liberation Sans
* Common TeX Live LaTeX packages
* LaTeX Workshop for editor integration

The main CV file is expected to be a `.tex` file such as:

```text
max_mustermann_cv_template.tex
```

If your CV includes a profile photo, keep the image file in the same directory as the `.tex` file or update the image path in the LaTeX source.

---

## Ubuntu / Debian Installation

Install the required TeX Live packages and font:

```bash
sudo apt update

sudo apt install \
    latexmk \
    texlive-xetex \
    texlive-latex-base \
    texlive-latex-recommended \
    texlive-latex-extra \
    texlive-fonts-recommended \
    texlive-lang-german \
    tex-gyre \
    fonts-liberation2
```

Verify the installation:

```bash
xelatex --version
latexmk -v
fc-match "Liberation Sans"
```

You can also check the installed executables:

```bash
command -v xelatex
command -v latexmk
```

Typical Ubuntu paths are:

```text
/usr/bin/xelatex
/usr/bin/latexmk
```

---

## Windows Installation

Install a LaTeX distribution that provides XeLaTeX and `latexmk`.

Recommended options:

* TeX Live
* MiKTeX

After installation, open PowerShell and verify:

```powershell
xelatex --version
latexmk -v
```

The CV uses the **Liberation Sans** font. Install Liberation Sans on Windows if it is not already available, or change the font in the LaTeX source.

The template currently expects:

```latex
\usepackage{fontspec}
\setmainfont{Liberation Sans}
```

---

## Install VS Code

Install Visual Studio Code.

VSCodium can also be used with the same project configuration if you prefer an open-source build of the editor.

Open the repository folder in the editor.

---

## Install LaTeX Workshop

Install:

```text
LaTeX Workshop
Publisher: James Yu
Extension ID: James-Yu.latex-workshop
```
