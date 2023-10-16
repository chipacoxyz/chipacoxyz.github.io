---
title: "Cómo aprender LaTeX, rápido"
summary: Quiero aprender LaTeX, si bien ya lo conocía, nunca lo aprendí bien, me pongo en campaña de re-aprender.
date: 2023-10-13
tags: ["LaTeX"]
draft: true
---

LaTeX siempre me llamó la atención, poder escribir sin que te importe el formato, su completa sintaxis matemática, el carácter libre y sus extensiones.

Sin embargo, nunca me detuve a aprenderlo detenídamente.

Eso tiene que cambiar...

## De dónde pienso aprender

Abundan recursos cortos, vendibles y bonitos en internet, pero como no soy fan de ello, me decanto por la vieja escuela... un libro como principal recurso.

[LaTeX Cookbook - Stefan Kottwitz](https://www.packtpub.com/product/latex-cookbook/9781784395148)

Existe [otro](https://www.packtpub.com/product/latex-beginners-guide-second-edition/9781801078658) para principiantes también.

## Extensiones y requisitos

Existen varias extenciones en el universo LaTeX, entre ellas se encuentran:

| Extensión | Descripción |
| --- | --- |
| **Document class** | Archivo de estilos con opciones por defecto, define la estructura del documento. |
| **Package** | Archivo de estilos también, puede agregar cosas adicionales al document, `\usepackage`. |
| **Bundle** | Conjunto de paquetes relacionados. |
| **Template** | Texto sin sentido, sirve como punto de inicio al empezar un nuevo documento. |

Y para usar esto se necesitaría: una distribución de LaTeX, [texlive](http://tug.org/texlive/) es buena opción, un editor de texto, y un visor de pdf.

También existen editores de LaTeX, que traen todo integrado, además de las herramientas online, todas estas también son válidas.

## Escribiendo un texto corto

En el caso de que nececitemos hacer una tarea para la escuela o escribir artículos simples, sin usar el complicado formato de un libro.

``` latex
\documentclass[paper=a4, oneside, fontsize=12pt, parskip=full]{scrartcl}

% scrartcl es del KOMA-Script bundle
% Desconozco la diferencia entre las clases estandard y KOMA.

% parskip es para no arrancar con sangría.

\begin{document}

\tableofcontents

\addsec{Introducción}
Este documento nos sirve como base para los documentos simples, puede contener una página o una banda más.

El texto se va a dividir en secciones.

\section{La primer sección}
El primer texto que contendrá

\begin{itemize}
\item Una tabla de contenidos,
\item Una lista punteada,
\item Títulos y algo de texto, y algo de matemática,
\item Referenciando como a la sección \ref{sec:maths} y la ecuación (\ref{eq:integral}).
\end{itemize}

Podemos usar este documento como template para llenar nuestro propio contenido

\section{Algo de matemática}
\label{sec:maths}
Cuando escribimos documentos científicos o técnicos, usualmente incluimos fórmulas matemáticas. Para dar un vistaso a cómo se ven las matemáticas, veremos una aproximación integral de la función
$f(x)$ como la suma con pesos $w_i$:

\begin{equation}
  \label{eq:integral}
  \int_a^b f(x)\,\mathrm{d}x \approx (b-a)
  \sum_{i=0}^n w_i f(x_i)
\end{equation}

\end{document}
```

Acá cómo quedó el [archivo pdf](images/texto-corto.pdf).