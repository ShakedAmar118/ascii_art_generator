# ASCII Art Generator 🎨☕

**Language:** Java
**Core Concepts:** OOP, Design Patterns, Algorithms, Image Processing

## 📖 Description
The **ASCII Art Generator** is a modular Java application that converts digital images into detailed text-based art.
Unlike simple pixel-converters, this engine utilizes a **sub-image processing algorithm** that divides images into grids based on dynamic resolution, calculates the average brightness using a weighted RGB formula, and maps each grid to the best-matching character from a normalized custom charset.

## 🚀 Key Features
* **Smart Resolution Scaling:** Dynamic control over output detail using `res up/down` commands (powers of 2), automatically constrained by image boundaries.
* **Custom Charset Management:** Full CLI support for adding/removing characters, ranges (`a-z`), or predefined sets (`all`, `space`).
* **Optimized Brightness Mapping:** Implements **linear contrast stretching** to maximize visual clarity and distinctions between characters.
* **Dual Output Modes:** Renders art directly to the **Console** or generates zoomable **HTML** files for high-resolution viewing.
* **Algorithmic Efficiency:** Utilizes **Caching / Memoization** to store brightness calculations, significantly reducing processing time for repeated renders.

## 🛠️ Technical Highlights
* **Architecture:** Built with strict adherence to **SOLID Principles**, decoupling the image processing logic (`image` package) from the user interface (`Shell`).
* **Design Patterns:** Implements modular design allowing for easy extension of character matching strategies.
* **Error Handling:** Robust Java Exception handling system for managing invalid user inputs and file I/O issues.

## 💻 Usage
The application runs an interactive Shell. Common commands include:
* `image <filename>`: Load a new image.
* `chars`: View current character set.
* `add <char|range>`: Add characters (e.g., `add a-z`, `add 0-9`).
* `output html/console`: Adjust output.
* `res up/down`: Adjust resolution.
* `asciiArt`: Generate the output.

### Run Command:
```bash
java -cp out/production/ex3 ascii_art.Shell