# Pandoc Letter Template (DIN 5008)

[Pandoc](https://pandoc.org/) template for writing letters in Markdown and converting them into PDFs
that follow the German national standard DIN 5008 for letter formatting. By using this
template, you can more efficiently create professional-looking letters in a
clean and organized manner. The template is customizable, so you can tailor it
to your specific needs.

## Preview

![alt Letter](https://github.com/benedu/pandoc-letter/raw/master/example/letter.png)

## Requirements

- [Pandoc](http://pandoc.org/installing.html)
- [LaTeX](https://latex-project.org/ftp.html)
  - [csquotes](https://ctan.org/pkg/csquotes)

## Usage

Clone this repository or download the template with the following command:

```bash
curl https://raw.githubusercontent.com/benedictdudel/pandoc-letter-din5008/master/letter.latex --create-dirs -o ~/.pandoc/templates/letter.latex
```

Write your letter in markdown, using the provided [`example/letter.md`](https://raw.githubusercontent.com/benedictdudel/pandoc-letter-din5008/master/example/letter.md) file as a
guide. You can download the example `letter.md` file with the following command:

```bash
curl https://raw.githubusercontent.com/benedictdudel/pandoc-letter-din5008/master/example/letter.md -o letter.md
```

To convert the markdown file to a PDF run:

```bash
pandoc letter.md -s -o letter.pdf --template="letter"
```

## Customization

You can customize the look and feel of the generated PDF by modifying the
variables. See [`example/letter.md`](https://raw.githubusercontent.com/benedictdudel/pandoc-letter-din5008/master/example/letter.md) for a full list of available variables.

## Contact

If you have any questions, feel free to open an issue [here](https://github.com/benedictdudel/pandoc-letter-din5008/issues) or contact me via twitter at [@benedictdudel](https://twitter.com/benedictdudel) 
