# Usage

This patch installs a couple of new logic gates for you to use in CircuiTikZ. The supported gates are:
* `din or gate`
* `din not gate`
They work much the same as the `american *` gates. Just try it.

| Before (US gates) | After (DIN 40700 gates) |
| ------ | ----- |
| ![US gates](http://fceschmidt.github.io/public/assets/2016-11-07-din-40700-gates-in-circuitikz/american_gates.png) | ![DIN gates](http://fceschmidt.github.io/public/assets/2016-11-07-din-40700-gates-in-circuitikz/din_gates.png) |

# How to install this patch

1. Install CircuiTikZ on your system
    - Hint: If you have a TeX distribution, chances are you already have it in your file system.
2. Locate your existing circuitikz installation. It should contain a file called pgfcirc.defines.tex and some other files.
    - Hint: For Arch Linux with TeXLive, look under `/usr/share/texmf-dist/tex/generic/circuitikz`.
3. Copy the file pgfcirccustomlogic.tex (you can find it in the `src/` folder) into this directory
4. Now you need to register this file in the latex registry, otherwise you will not be able to use it:
    1. Locate the file "circuitikz.sty" in your LaTeX installation (there may be multiple!) and put "pgfcirccustomlogic.tex" in there after all the other pgfcirc\*.tex files.
    2. Open the file "ls-R" in the root of your LaTeX installation and find the line which contains "pgfcirctripoles.tex". Now add "pgfcirccustomlogic.tex" below that one.

Now you can compile files using this patch.

# Motivation

You can read [this article](http://fceschmidt.github.io/foss/2016/11/07/din-40700-logic-gates-in-circuitikz.html).
