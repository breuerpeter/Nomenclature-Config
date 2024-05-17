# Nomenclature-Config

### How to use

1. Add this repo to your project by cloning its contents to `PROJECT_ROOT_DIR/nomenclature/config/`
2. Include the config file in your project's main `.tex` file `PROJECT_MAIN.tex` by adding the following line to the preamble
    ```
    \input{nomenclature/config/config.tex}
    ```
    
3. Include the file that prints the glossary in your project's main `.tex` file by adding the following line in the desired location
    ```
    \input{nomenclature/config/print.tex}
    ```
3. Build your project
    ```
    pdflatex PROJECT_MAIN
    bib2gls -g PROJECT_MAIN
    pdflatex PROJECT_MAIN
    pdflatex PROJECT_MAIN
    ```