# LaTeX MATH MODE CHEAT SHEET

`LaTeX math mode` _is the math mode of LaTex. LaTeX is
an advanced typesetting system._

Documentation and reference,

* [LaTeX math mode document](https://www.overleaf.com/learn/latex/Mathematical_expressions)
* [LaTeX math mode reference](https://en.wikibooks.org/wiki/LaTeX/Mathematics)
* [mathurl.com to help build your formulas](http://mathurl.com/)

What LaTeX math mode functions can I use,

* [KaTeX Supported Functions](https://katex.org/docs/supported.html)
* [KaTeX Support Table](https://katex.org/docs/support_table.html)

View my entire list of cheat sheets on
[my GitHub Webpage](https://jeffdecola.github.io/my-cheat-sheets/).

## TeX

`TeX` is an advanced typesetting system which was
developed by Donald Knuth in 1978. It is a markup language
for describing a document.
LaTeX is designed for the content, not the look of the document.
TeX is mainly popular because of its ability to handle complex technical
text and in displaying mathematical formula.

## LaTeX

`LaTeX` is a set of macros built on top of TeX. Built back in the 80s.

The syntax can look something like,

```txt
    \documentclass{article}
    \title{Cartesian closed categories and the price of eggs}
    \author{Jane Doe}
    \date{September 1994}
    \usepackage{amsmath}
    \begin{document}
    \begin{equation}
        E=mc^2
    \end{equation}
    \end{document}
```

But I don't use any of this, I'm only interested in
the mathematical formulas of LaTeX (Math mode).

## INSTALL LaTeX

This is to install a full version with all the packages. I'm not sure
how to install a lighter version properly,

```bash
sudo apt-get update
sudo apt-get upgrade -y
sudo apt-get install texlive-full
```

check version,

```bash
latex -version
```

To test, lets use a LateX file
[latex-math-mode.txt](https://github.com/JeffDeCola/my-cheat-sheets/blob/master/software/development/languages/latex-math-mode-cheat-sheet/latex-example/latex-math-mode.txt)
which will invoke math mode and create a .pdf file,

```bash
cd latex-example
pdflatex latex-math-mode.txt
```

If everything worked correctly your .pdf should look like
[mine](https://github.com/JeffDeCola/my-cheat-sheets/blob/master/software/development/languages/latex-math-mode-cheat-sheet/latex-example/latex-math-mode.pdf).
This example outlines and basics of latex math mode and is explained below.

## USING LaTeX IN MATH MODE

I want to render this LaTeX math equation `E=mc^2`.

### DECLARING MATH MODE

First, there are three ways `declaring math mode` in LaTeX,

* In-line mode \$...\$
* Display mode (Newline, center) \$\$...\$\$
* Display mode (Newline, center with tag) begin{equation}...end{equation}

An example of LaTeX math in-line mode,

```txt
    Einstein's equation
    $E=mc^2$
    represent energy is equal to matter multiplied by the speed of light squared.
```

Einstein's equation
<img alt="$E=mc^2$" src="svgs/ccb175704c18ad5a81177f1274fcd39f.svg" align="middle" width="62.9013pt" height="26.70657pt"/>
represent energy is equal to matter multiplied by the speed of light squared.

An example of LaTeX math display mode,

```txt
    $$
    $E=mc^2$
    $$
```

<p align="center"><img alt="$$&#10;E=mc^2&#10;$$" src="svgs/3abb8c75967ebfdd6439c56912f3d75a.svg" align="middle" width="62.901135pt" height="14.175084pt"/></p>

An example of LaTeX math display mode (with tag),

```txt
    \begin{equation}
        E=mc^2
    \end{equation}
```

<p align="center"><img alt="\begin{equation}&#10;    E=mc^2&#10;\end{equation}" src="svgs/f334ebc0d2eff9a7f146c11edd071f96.svg" align="middle" width="382.01955pt" height="18.269295pt"/></p>

This is sometimes hard to render being{equation} correctly,
so I kind of stay away from it.  I have a way to make my own tags below.

### FORMATING MULTIPLE EQUATIONS

Second there are two main ways to format multiple equations in LaTeX math mode,

* `begin{gathered}...end{gathered}` - Every equation centered.
* `begin{aligned}...end{aligned}` - Will align on an ampersand.

An example of LaTeX math display mode (using aligned),

```txt
    $$
    \begin{aligned}
        a&=b+c \\
        d+e&=f
    \end{aligned}
    $$
```

<p align="center"><img alt="$$&#10;\begin{aligned}&#10;    a&amp;=b+c \\&#10;    d+e&amp;=f&#10;\end{aligned}&#10;$$" src="svgs/61e53b5569a8e3e0af95fdfbec895cdf.svg" align="middle" width="92.330205pt" height="39.21489pt"/></p>

An example of LaTeX math display mode (using gathered),

```txt
    $$
    \begin{gathered}
        a=b+c \\
        d+e=f
    \end{gathered}
    $$
```

<p align="center"><img alt="$$&#10;\begin{gathered}&#10;    a=b+c \\&#10;    d+e=f&#10;\end{gathered}&#10;$$" src="svgs/b81b3a8ee17288b65f2e80ae31ac2c24.svg" align="middle" width="67.843545pt" height="39.21489pt"/></p>

## HOW I CREATED THIS README.md

I use a program called [readme2tex](https://github.com/leegao/readme2tex).
I run everything on my local machine.

It works by taking your LaTeX math formula, rendering an image and
referencing that image using HTML.

First, I created and edit in README.tex.md.
I have my LaTeX for math markdown in there delimited by dollar signs.

Second, I run `readme2tex`. This will,

* Create a new README.md file.
* Creates *.svg images for each of the LateX for math formulas.
* Add those image links automatically in your README.md file.

It created the images using the latex program and geometry package you
must install on your machine.  See the end of this cheat sheet for how I installed.

I used to use a github app called
[TeXify](https://github.com/apps/texify),
but it is not that reliable and I don't like
other programs having write access to my repo.  I feel
like I loose control.

Here is an illustration on how it works,

![IMAGE - readme2tex-latex-math-mode-github - IMAGE](../../../../docs/pics/readme2tex-latex-math-mode-github.jpg)

## COMMON LaTeX MATH EQUATIONS

For brevity dollar sign delimiters are not shown.

You can use,

* [KaTeX Supported Functions](https://katex.org/docs/supported.html)
* [KaTeX Support Symbols](https://katex.org/docs/support_table.html)

Einsteins famous equation,

```txt
    E=mc^2
```

<p align="center"><img alt="$$&#10;E=mc^2&#10;$$" src="svgs/3abb8c75967ebfdd6439c56912f3d75a.svg" align="middle" width="62.901135pt" height="14.175084pt"/></p>

Pythagorean theorem,

```txt
    x^n + y^n = z^n
```

<p align="center"><img alt="$$&#10;x^n + y^n = z^n&#10;$$" src="svgs/238cd7abcefb8a6a256d0bec59744770.svg" align="middle" width="94.22292pt" height="14.9075025pt"/></p>

Pythagorean theorem (with box),

```txt
    \boxed{x^n + y^n = z^n}
```

<p align="center"><img alt="$$&#10;\boxed{x^n + y^n = z^n}&#10;$$" src="svgs/2dc0d735a1c4f4b4bb63782b8b4e8875.svg" align="middle" width="106.44249pt" height="26.116035pt"/></p>

Pythagorean theorem (numbered using begin{equation}),

```txt
    \begin{equation}
        x^n + y^n = z^n
    \end{equation}
```

<p align="center"><img alt="\begin{equation}&#10;    x^n + y^n = z^n&#10;\end{equation}" src="svgs/9c2c2ace77591d2c08d3ea86c859717c.svg" align="middle" width="397.69125pt" height="16.376943pt"/></p>

Pythagorean theorem (numbered using tag),

```txt
    \begin{equation}
        x^n + y^n = z^n\tag{6}
    \end{equation}
```

<p align="center"><img alt="\begin{equation}&#10;    x^n + y^n = z^n\tag{6}&#10;\end{equation}" src="svgs/508f5e725b18bed700d18ff1cea4238c.svg" align="middle" width="397.69125pt" height="16.376943pt"/></p>

Pythagorean theorem (another way to do numbers),

```txt
    \qquad \qquad
    x^n + y^n = z^n
    \qquad \qquad (4)
```

<p align="center"><img alt="$$&#10;\qquad \qquad&#10;x^n + y^n = z^n&#10;\qquad \qquad (4)&#10;$$" src="svgs/5b71346bca16eedf780a40e41ddef9e8.svg" align="middle" width="181.7541pt" height="16.376943pt"/></p>

Square root,

```txt
    \sqrt[3]{x}
```

<p align="center"><img alt="$$&#10;\sqrt[3]{x}&#10;$$" src="svgs/8375620ec7847ff048e565abd48c90cd.svg" align="middle" width="23.093565pt" height="16.379385pt"/></p>

Multiple equations (gathered),

```txt
    \begin{gathered}
        a=b+c \\
        d+e=f
    \end{gathered}
```

<p align="center"><img alt="$$&#10;\begin{gathered}&#10;    a=b+c \\&#10;    d+e=f&#10;\end{gathered}&#10;$$" src="svgs/b81b3a8ee17288b65f2e80ae31ac2c24.svg" align="middle" width="67.843545pt" height="39.21489pt"/></p>

Multiple equations (aligned on ampersand &),

```txt
    \begin{aligned}
        a&=b+c \\
        d+e&=f
    \end{aligned}
```

<p align="center"><img alt="$$&#10;\begin{aligned}&#10;    a&amp;=b+c \\&#10;    d+e&amp;=f&#10;\end{aligned}&#10;$$" src="svgs/61e53b5569a8e3e0af95fdfbec895cdf.svg" align="middle" width="92.330205pt" height="39.21489pt"/></p>

Alignment and spacing (on equal sign),

```txt
    \begin{aligned}
        f(x) =& x^2\! +3x\! +2 \\
        f(x) =& x^2+3x+2 \\
        f(x) =& x^2\, +3x\, +2 \\
        f(x) =& x^2\: +3x\: +2 \\
        f(x) =& x^2\; +3x\; +2 \\
        f(x) =& x^2\ +3x\ +2 \\
        f(x) =& x^2\quad +3x\quad +2 \\
        f(x) =& x^2\qquad +3x\qquad +2
    \end{aligned}
```

<p align="center"><img alt="$$&#10;\begin{aligned}&#10;    f(x) =&amp; x^2\! +3x\! +2 \\&#10;    f(x) =&amp; x^2+3x+2 \\&#10;    f(x) =&amp; x^2\, +3x\, +2 \\&#10;    f(x) =&amp; x^2\: +3x\: +2 \\&#10;    f(x) =&amp; x^2\; +3x\; +2 \\&#10;    f(x) =&amp; x^2\ +3x\ +2 \\&#10;    f(x) =&amp; x^2\quad +3x\quad +2 \\&#10;    f(x) =&amp; x^2\qquad +3x\qquad +2&#10;\end{aligned}&#10;$$" src="svgs/7e7e2b03aa45736c18ad92fa9b6f9b47.svg" align="middle" width="197.66175pt" height="205.1412pt"/></p>

An integral,

```txt
    \int_{a}^{b} x^2 dx
```

<p align="center"><img alt="$$&#10;\int_{a}^{b} x^2 dx&#10;$$" src="svgs/7434eb168b5dfced915545b6a422e7b8.svg" align="middle" width="60.399075pt" height="41.24901pt"/></p>

Limits,

```txt
    \lim_{x\to\infty} f(x)
```

<p align="center"><img alt="$$&#10;\lim_{x\to\infty} f(x)&#10;$$" src="svgs/b7ecb947fb5547679f1c7ab9a546d2ce.svg" align="middle" width="68.289045pt" height="22.14564pt"/></p>

Some trigonometry,

```txt
    \sin(a + b ) = \sin(a)\cos(b) + \cos(a)\sin(b)
```

<p align="center"><img alt="$$&#10;\sin(a + b ) = \sin(a)\cos(b) + \cos(a)\sin(b)&#10;$$" src="svgs/85b567a60b6ab8fbc319c720f66f8ae2.svg" align="middle" width="282.74565pt" height="16.376943pt"/></p>

Fractions (binomial coefficients),

```txt
    \binom{n}{k} = \frac{n!}{k!(n-k)!}
```

<p align="center"><img alt="$$&#10;\binom{n}{k} = \frac{n!}{k!(n-k)!}&#10;$$" src="svgs/9cc892f15c1314868714ad2b49649eb5.svg" align="middle" width="127.93704pt" height="39.30498pt"/></p>

Brackets,

```txt
    \left( \frac{x}{y} \right)
```

<p align="center"><img alt="$$&#10;\left( \frac{x}{y} \right)&#10;$$" src="svgs/2beb7431726139ffb37413b4031f73c1.svg" align="middle" width="37.49592pt" height="39.30498pt"/></p>

Bracket array,

```txt
    \left(
        \begin{array}{ccc}
            1 & 2 & 3\\
            4 & 4 & 9\\
            1 & -8 & 2
        \end{array}
    \right)
```

<p align="center"><img alt="$$&#10;\left(&#10;    \begin{array}{ccc}&#10;        1 &amp; 2 &amp; 3\\&#10;        4 &amp; 4 &amp; 9\\&#10;        1 &amp; -8 &amp; 2&#10;    \end{array}&#10;\right)&#10;$$" src="svgs/7192bf1b080bb1180da0295fcda68a71.svg" align="middle" width="115.47162pt" height="59.068185pt"/></p>

Arrays in Brackets with spacing (\qquad),

```txt
    \left(
        \begin{array}{ccc}
            1 & 2 & 3\\
            4 & 5 & 9\\
            1 & -8 & 2
        \end{array}
    \right)
    \qquad
    \left\{
        \begin{array}{ccc}
            1 & 5 & 8\\
            0 & 2 & 4\\
            3 & 3 & -8
        \end{array}
    \right\}
```

<p align="center"><img alt="$$&#10;\left(&#10;    \begin{array}{ccc}&#10;        1 &amp; 2 &amp; 3\\&#10;        4 &amp; 5 &amp; 9\\&#10;        1 &amp; -8 &amp; 2&#10;    \end{array}&#10;\right)&#10;\qquad&#10;\left\{&#10;    \begin{array}{ccc}&#10;        1 &amp; 5 &amp; 8\\&#10;        0 &amp; 2 &amp; 4\\&#10;        3 &amp; 3 &amp; -8&#10;    \end{array}&#10;\right\}&#10;$$" src="svgs/34937d1b68e46828a9241c64dd9c8c8a.svg" align="middle" width="267.069pt" height="59.12346pt"/></p>

Some cool arrows,

```txt
    A \xleftarrow{\text{this way}} B
    \xrightarrow[\text{or that way}]{ } C
```

<p align="center"><img alt="$$&#10;A \xleftarrow{\text{this way}} B&#10;\xrightarrow[\text{or that way}]{ } C&#10;$$" src="svgs/056bb44ae5a648c007f840c99bc3cbdf.svg" align="middle" width="192.2844pt" height="31.01538pt"/></p>

Cases,

```txt
    u(x) =
    \begin{cases}
        \exp{x} & \text{if } x \geq 0 \\
        1       & \text{if } x < 0
    \end{cases}
```

<p align="center"><img alt="$$&#10;u(x) =&#10;\begin{cases}&#10;    \exp{x} &amp; \text{if } x \geq 0 \\&#10;    1       &amp; \text{if } x &lt; 0&#10;\end{cases}&#10;$$" src="svgs/7cdb2cc12c0acb192d47b17946ace840.svg" align="middle" width="174.7581pt" height="49.13139pt"/></p>

Make some big text,

```txt
    $$
    \huge\text{Hello Jeff}
    $$
```

<p align="center"><img alt="$$&#10;\huge\text{Hello Jeff}&#10;$$" src="svgs/e352edc1951d2b05c08e5e2f08d50273.svg" align="middle" width="129.856485pt" height="23.58741pt"/></p>

## COLOR PACKAGE "xcolor"

If you want color, you must use the color package "xcolor".
So when you use `readme2tex make sure you add it in,

```bash
python -m readme2tex --usepackage "xcolor" ....etc...
```

As an example,

```txt
    \color{red} E=mc^2
```

<p align="center"><img alt="$$&#10;\color{red} E=mc^2&#10;$$" src="svgs/701e889902a8da29f6b7ca34bdd374d7.svg" align="middle" width="62.901135pt" height="14.175084pt"/></p>

## GRAPH PACKAGE "tikz"

`TikZ` is a LaTeX package that allows you to create high quality diagrams.
Tikz is probably the most complex and powerful tool to create
graphic elements in LaTeX.
When you use `readme2tex make sure you add it in,

```bash
python -m readme2tex --usepackage "tikz" ....etc...
```

As an example of a circle,

```txt
    \begin{tikzpicture}
        \draw (2,2) circle (3cm);
    \end{tikzpicture}
```

## LaTeX APPS

Some cool LaTeX apps I use.

### VISUAL STUDIO CODE APP - MARKDOWN + MATH

View LaTeX math formulas in Visual Studio Code preview window.

[MARKDOWN + MATH](https://marketplace.visualstudio.com/items?itemName=goessner.mdmath)

### BROWSER SUPPORT - KaTeX

Displays mathematical notation in web browsers.

[KaTeX](https://katex.org/docs/supported.html)

### BROWSER SANDBOX - mathurl.com

Sandbox to create your LaTeX math formulas online.

[mathurl.com](http://mathurl.com/)

### GITHUB APP - TeXify

[TeXify](https://github.com/apps/texify)
is a github app (on github) that Renders LateX to images in markdown.
Its built on
[readme2tex](https://github.com/leegao/readme2tex).

You write `README.text.md` and push.
At github, it will convert your LaTeX to `/tex/*.svg` images and
created a `README.md` file with links to those images.

This app is not that stable.

### APP - readme2tex

[readme2tex](https://github.com/leegao/readme2tex).

This cheat sheet is using this app.

You need Python 2.7 or above and pip installed.

Install full latex (I really only wanted latex and
latex geometry package) and dvisvgm,

```bash
sudo apt-get update
sudo apt-get upgrade -y
sudo apt-get install texlive-full
sudo apt install texlive-extra-utils
sudo apt install texlive-publishers
```

Install cairocffi and other dependencies you may need,

```bash
sudo apt-get install libffi6 libffi-dev
pip install --user cairocffi
pip install 'setuptools<36'
```

Now install readme2tex,

```bash
git clone https://github.com/leegao/readme2tex
cd readme2tex
sudo python setup.py develop
```

Again, I do not want to install the full version of latex
(3 gigs), but can't figure out how to install latex
and just the geometry package.

Usage,

```bash
python -m readme2tex --readme README.tex.md --output README.md --nocdn
```