[English below ↓](#doctoral-thesis-template-with-quarto)

# Plantilla de tesis doctoral con Quarto

Este repositorio contiene una plantilla base para la elaboración de una tesis doctoral (o libro) utilizando [**Quarto**](https://quarto.org/). El objetivo principal es facilitar la estructura y el proceso de compilación, permitiendo centrarte en el contenido académico.

------------------------------------------------------------------------

## Objetivo

-   Proporcionar una estructura inicial para la escritura de una tesis o libro en formato Quarto.
-   Incluir archivos de ejemplo (`.qmd`) y un archivo `_quarto.yml` listo para configurar.
-   Simplificar el proceso de compilación a PDF (o HTML/EPUB) con unos pocos comandos.

------------------------------------------------------------------------

## Estructura del proyecto

La estructura mínima de archivos es la siguiente:

```         
├── _quarto.yml          # Configuración principal de Quarto
├── index.qmd            # Documento base o introducción
├── prefacio.qmd         # Ejemplo de prefacio sin numeración
├── capitulo1.qmd        # Ejemplo de capítulo 1
├── capitulo2.qmd        # Ejemplo de capítulo 2
├── resultados.qmd       # Ejemplo de apartado de resultados
├── referencias.qmd      # Sección de referencias si se desea separar
├── referencias.bib       # Archivo de bibliografía
├── estilo-citas.csl     # (Opcional) Estilo de citas
└── README.md            # Este archivo con instrucciones
```

> Nota: Puedes renombrar o añadir otros capítulos o secciones según tu esquema de trabajo.

------------------------------------------------------------------------

## Requisitos previos

1.  **Quarto**: Descárgalo e instálalo desde [quarto.org](https://quarto.org).
2.  **LaTeX**: Si deseas compilar a PDF, asegúrate de tener una distribución de LaTeX instalada:
    -   [TeX Live](https://www.tug.org/texlive/)
    -   [MiKTeX](https://miktex.org/)
    -   [TinyTeX](https://yihui.org/tinytex/) (instalable directamente en R).
3.  (Opcional) **R y RStudio**:
    -   Para un flujo de trabajo completo, puedes usar [RStudio](https://posit.co/products/open-source/rstudio/) y la integración con Quarto.

------------------------------------------------------------------------

## Cómo usar la plantilla

1.  **Clona este repositorio** o descárgalo como ZIP y descomprímelo.

    ``` bash
    git clone https://github.com/bHerreno/plantilla-quarto-tesis.git
    ```

2.  **Edita los archivos `.qmd`** con tu contenido:

    -   `index.qmd` puede funcionar como portada o introducción.
    -   `prefacio.qmd` está configurado como una sección sin numeración.
    -   `capitulo1.qmd`, `capitulo2.qmd`, etc., pueden ser capítulos con contenido académico.

3.  **Ajusta la configuración** en `_quarto.yml`:

    -   Título, autor, fecha y estructura de capítulos.
    -   Formato de salida (PDF, HTML, EPUB).
    -   Ajusta la bibliografía (`bibliography`) y el estilo de citas (`csl`) si corresponde.

------------------------------------------------------------------------

## Compilación

### Vía Terminal (CLI)

 Abre una terminal, navega hasta la carpeta del proyecto (donde se encuentra el archivo `_quarto.yml`) y ejecuta los siguientes comandos según tus necesidades:

    ```bash
    # 1) Navega a la carpeta raíz del proyecto
    cd /ruta/a/tu/proyecto
    # Ejemplos:
    #   macOS/Linux:  cd ~/repos/plantilla-quarto-tesis
    #   Windows:      cd "C:\Users\TuUsuario\Documents\plantilla-quarto-tesis"
    ```

    ```bash
    # 2) Renderiza el proyecto completo (detecta automáticamente _quarto.yml)
    quarto render
    # equivale a:
    # quarto render .
    ```

    ```bash
    # 3) Renderiza un archivo específico (por ejemplo, un capítulo)
    quarto render capitulo1.qmd
    ```

    ```bash
    # 4) Fuerza un formato de salida (requiere LaTeX si eliges PDF)
    quarto render --to pdf # Esto generará un archivo PDF (u otro formato) en la misma carpeta del proyecto.
    quarto render --to html
    quarto render --to epub
    ```

    ```bash
    # 5) (Opcional) Comprueba la instalación y los requisitos
    quarto check
    ```


### Vía RStudio

1.  Abre RStudio y selecciona `File > Open Project` para abrir la carpeta del proyecto.

2.  Asegúrate de que Quarto esté instalado y reconocido por RStudio (en la consola de R, prueba `system("quarto --version")`).

3.  Para compilar el libro, haz clic en el **botón "Render"** de la barra superior (si estás en un archivo `.qmd`) o ejecuta en la consola:

    ``` r
    quarto::quarto_render()
    ```

------------------------------------------------------------------------

## Personalización

-   **Portada**: Modifica `index.qmd` o crea un nuevo archivo `.qmd` para incluir portadas personalizadas.
-   **Dedicatorias y Agradecimientos**: Añade secciones sin numeración (`.unnumbered`) o ubícalas en `prefacio.qmd`.
-   **Estilo y Formato**: Ajusta parámetros en `_quarto.yml`, por ejemplo:
    -   `fontsize`, `papersize`, `geometry`, `classoption`, etc.
-   **Referencias y Bibliografía**:
    -   Ajusta `bibliography: referencias.bib` con tus propias referencias en formato BibTeX.
    -   Usa `[@nombreReferencia]` en el texto para citar.

------------------------------------------------------------------------

## Contribuciones y soporte

Si encuentras errores o deseas contribuir con mejoras, por favor abre un *issue* o envía un *pull request*. Toda sugerencia es bienvenida.

------------------------------------------------------------------------

¡Disfruta escribiendo tu tesis con Quarto y ahorra tiempo en la maquetación!

---

# Doctoral Thesis Template with Quarto

> **Note:** The examples and sample content are in **Spanish**, but they can be treated as *Lorem Ipsum* placeholders.

This repository provides a base template for writing a doctoral thesis (or a book) using [**Quarto**](https://quarto.org/).
The main goal is to simplify the structure and compilation process, allowing you to focus on the academic content.

------------------------------------------------------------------------

## Objective

* Provide an initial structure for writing a thesis or book in Quarto format.
* Include sample `.qmd` files and a preconfigured `_quarto.yml` file.
* Simplify the rendering process to PDF (or HTML/EPUB) with just a few commands.

------------------------------------------------------------------------

## Project Structure

```
├── _quarto.yml          # Main Quarto configuration
├── index.qmd            # Base document or introduction
├── prefacio.qmd         # Example of an unnumbered preface
├── capitulo1.qmd        # Example of Chapter 1
├── capitulo2.qmd        # Example of Chapter 2
├── resultados.qmd       # Example of results section
├── referencias.qmd      # Optional separate references section
├── referencias.bib      # Bibliography file
├── estilo-citas.csl     # (Optional) Citation style
└── README.md            # This file
```

> Note: You can rename or add other chapters or sections according to your own structure.

------------------------------------------------------------------------

## Requirements

1. **Quarto**: Download and install from [quarto.org](https://quarto.org).
2. **LaTeX**: To compile to PDF, make sure you have a LaTeX distribution installed:

   * [TeX Live](https://www.tug.org/texlive/)
   * [MiKTeX](https://miktex.org/)
   * [TinyTeX](https://yihui.org/tinytex/) (installable directly from R).
3. (Optional) **R and RStudio**:

   * For a complete workflow, use [RStudio](https://posit.co/products/open-source/rstudio/) with Quarto integration.

------------------------------------------------------------------------

## How to Use the Template

1. **Clone this repository** or download it as a ZIP and extract it.

   ```bash
   git clone https://github.com/bHerreno/plantilla-quarto-tesis.git
   ```

2. **Edit the `.qmd` files** with your own content:

   * `index.qmd` can serve as the cover or introduction.
   * `prefacio.qmd` is set as an unnumbered section.
   * `capitulo1.qmd`, `capitulo2.qmd`, etc., can be chapters with academic content.

3. **Adjust the configuration** in `_quarto.yml`:

   * Title, author, date, and chapter structure.
   * Output format (PDF, HTML, EPUB).
   * Update the bibliography (`bibliography`) and citation style (`csl`) if needed.

------------------------------------------------------------------------

## Rendering

### Using the Terminal (CLI)

Open a terminal, navigate to the project folder (where the `_quarto.yml` file is located), and run the following commands as needed:

   ```bash
   # 1) Navigate to the root folder of the project
   cd /path/to/your/project
   # Examples:
   #   macOS/Linux:  cd ~/repos/quarto-thesis-template
   #   Windows:      cd "C:\Users\YourUser\Documents\quarto-thesis-template"
   ```

   ```bash
   # 2) Render the entire project (automatically detects _quarto.yml)
   quarto render
   # same as:
   # quarto render .
   ```

   ```bash
   # 3) Render a specific file (for example, a single chapter)
   quarto render capitulo1.qmd
   ```

   ```bash
   # 4) Force an output format (requires LaTeX if you choose PDF)
   quarto render --to pdf # This will generate a PDF (or other format) in the same project folder.
   quarto render --to html
   quarto render --to epub
   ```

   ```bash
   # 5) (Optional) Check installation and requirements
   quarto check
   ```

### Using RStudio

1. Open RStudio and select `File > Open Project`.
2. Make sure Quarto is installed (`system("quarto --version")`).
3. Click **Render** or run in the console:

   ```r
   quarto::quarto_render()
   ```

------------------------------------------------------------------------

## Customization

* **Cover Page**: Modify `index.qmd` or create a new `.qmd` file for a custom cover.
* **Dedications and Acknowledgments**: Add unnumbered sections (`.unnumbered`) or include them in `prefacio.qmd`.
* **Style and Format**: Adjust parameters in `_quarto.yml`, e.g.:

  * `fontsize`, `papersize`, `geometry`, `classoption`, etc.
* **References and Bibliography**:

  * Update `bibliography: referencias.bib` with your own references.
  * Use `[@referenceName]` in the text to cite.

------------------------------------------------------------------------
## Contributions and Support

If you find any issues or wish to suggest improvements, feel free to open an *issue* or submit a *pull request*. All contributions are welcome.


Enjoy writing your thesis with Quarto — and save time on formatting!
