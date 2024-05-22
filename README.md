# Nomenclature-Config

### How to use

1. Add this repo to your project by cloning its contents to `PROJECT_ROOT_DIR/nomenclature/config/`
2. Include the config file in your project's main `.tex` file `PROJECT_MAIN.tex` by adding the following line to the preamble

    ```
    \input{nomenclature/config/config.tex}
    ```

3. Insert glossary entries in your project using the following syntax

    | Syntax        | Function                       |
    | ------------- | ------------------------------ |
    | `\gls{KEY}`   | Print in lowercase             |
    | `\glspl{KEY}` | Print plural form in lowercase |
    | `\Gls{KEY}`   | Print in uppercase             |
    | `\Glspl{KEY}` | Print plural form in uppercase |

    Note: see [below](#key-naming-convention) for key conventions
    
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

## Key naming convention

Note: components are separated by an underscore `_`

### Symbols

#### 1. Quantity descriptor

| Prefix       | Meaning        |
| ------------ | -------------- |
| `pt`         | Point          |
| `vec`        | Vector         |
| `mat`        | Matrix         |

Note: the prefix is followed by the name of the quantity (in a lowerCamelCase fashion)

#### 2. (Optional) quantity details

| Abbreviation | Meaning                           |
| ------------ | --------------------------------- |
| `compXXX`    | `XXX` component of quantity       |
| `hom`         | Homogeneous coordinates          |

#### 3. (If applicable) reference frame

Syntax: `frXXX` to indicate reference frame `XXX`

### Terms

#### 1. `DEF`

#### 2. Term in lowerCamelCase

