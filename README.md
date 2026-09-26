# Plantilla y Paquete LaTeX - IES IBAI (`iesibai.sty`)

Paquete de estilo en LaTeX para la redacción de documentos académicos del IES IBAI, configurado con soporte para **XeLaTeX**, formato **APA 7ma edición** e identidades visuales institucionales.

## Requisitos previos
- Distribución TeX (TeX Live, MiKTeX o MacTeX).
- Compilador **XeLaTeX**.
- Procesador de bibliografía **Biber**.
- Opcional *Zotero* para la gestión de referencias.

## Uso rápido
1. Clona este repositorio o descarga el archivo `iesibai.sty`.
2. Coloca `iesibai.sty` en la misma carpeta que tu archivo principal (trabajo, tesis, etc) `.tex`.
3. En el preámbulo de tu documento, incluye:
   ```latex
   \documentclass{article}
   \usepackage{iesibai}
   \addbibresource{referencias.bib}
   ```
## Características
1. Incluye un fondo de portada predefinido.
2. Capos de datos opcionales para la portada.
3. Formato predefinido para la portada, tabla de contenidos, capítulos y secciones acorde a los colores del instituto IESIBAI
4. Incluye logos en formatos `.jpeg`, `.png` y `.svg`.

## Ejemplo

```latex
\documentclass[12pt,letterpaper]{report}
\usepackage{iesibai}

% --- EJEMPLOS DE USO OPCIONALES ---
% 1. Para cambiar solo algunos valores de la portada, descomenta esto:
\iesibaisetup{
    institucion={Instituto de Estudios\\ Superiores de la\\ Red Iberoamericana de\\ Academias de Investigación},
    campus={Campus Virtual Hidalgo},
    programa={Maestría en Educación},
    materia={Tecnología e Innovación I},
    subtitulo={Un subtítulo interesante},
    alumno={Nombre del Alumno},
    profesor={Dr. TheBiotechScientist},
    ubicacion={San Luis Potosí, México},
    fecha={Septiembre, 2026}
}

% 2. Si para algún trabajo no deseas que se genere la portada, descomenta esto:
% \sinportadaiesibai

\begin{document}

\tableofcontents

\chapter{Primer capítulo}
Texto del primer capítulo

\section{Primera sección del capítulo 1}

\chapter{Segundo capítulo}
Aquí va el segundo capítulo

\secction{Primera sección del capitulo 2}

\chapter{Tercer capítulo}
Y seguimos


\end{document}
```