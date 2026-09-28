# Plantilla y Paquete LaTeX - IES IBAI (`iesibai.sty`)

**Versión:** 1.0.0  
**Fecha:** 2026-09-27  
**Autor:** TheBiotechScientist  
**Licencia:** LPPL v1.3c

## Descripción
Paquete de estilo en LaTeX para la redacción de documentos académicos del IES IBAI, configurado con soporte para **XeLaTeX**, formato **APA 7ma edición** e identidades visuales institucionales. El paquete `iesibai` proporciona macros, configuración de formato y elementos de portada para la generación de documentos académicos e institucionales ajustados a los requisitos del IESIBAI.

## Contenido del paquete
- `iesibai.sty`: Archivo de estilo principal.
- `iesibai-doc.pdf`: Documentación oficial compilada.
- `iesibai-doc.tex`: Código fuente de la documentación.
- `ejemplo.tex`: Documento de ejemplo mínimo.
- `README.md`: Readme con esta información.
- `LICENSE`: Licencia del paquete.
- `assets/`: Recursos gráficos predeterminados (logos y fondos).

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
## Instalación desde CTAN
- Desde el instalador/gestor de paquetes de su distribución instalada (MikTeX, TeXLive, MacTeX, etc.)
- Desde el repositorio de *CTAN*, buscar el paquete `iesibai.sty` y descargar.
- Seguir las instruciones para descarga y correcta isntalación de un paquete desde CTAN.

## Características
1. Incluye un fondo de portada predefinido.
2. Campos de datos opcionales para la portada.
3. Formato predefinido de portada, tabla de contenidos, capítulos y secciones acorde a los colores del instituto IESIBAI
4. Incluye logos de la institución en formatos `.jpeg`, `.png` y `.svg`.

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
    alumno={TheBiotechScientist},
    profesor={Dr. IESIBAI},
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