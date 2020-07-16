# Pandoc Letter Template (DIN 5008)

## Description

This template allows you to write simple letters in Markdown and convert them
into nice looking PDFs. The template is based on Koma Script and satisfies
the German DIN 5008 norm for letters.


## Example

A simple letter in Markdown looks like the following:

```markdown
---
author: Max Mustermann
phone: +49 1234 56789
email: max.mustermann@beispiel.de
date: 01.08.2016
place: Musterstadt
subject: Titel vom Brief
return-address:
 - Musterstraße
 - 12345 Berlin
address:
 - Musterfirma GmbH
 - Max Mustermann
 - Musterstraße
 - 12345 Musterstadt
opening: Sehr geehrte Damen und Herren,
closing: Mit freundlichen Grüßen
encludes: Muster, Muster, Muster
...
Far far away, behind the word mountains, far from the countries
Vokalia and Consonantia, there live the blind texts. Separated
they live in Bookmarksgrove right at the coast of the Semantics,
a large language ocean. A small river named Duden flows by their
place and supplies it with the necessary regelialia. 

When she reached the first hills of the Italic Mountains, she
had a last view back on the skyline of her hometown Bookmarksgrove,
the headline of Alphabet Village and the subline of her own road,
the Line Lane.
```

The compiled result will then look like this:

![alt Letter](https://github.com/benedu/pandoc-letter/raw/master/example/letter.png)

You can also download the compiled PDF [here](https://github.com/benedu/pandoc-letter/raw/master/example/letter.pdf).


## Requirements

In order to use the template you must have installed the following components:

- [Pandoc](http://pandoc.org/installing.html)
- [LaTeX](https://latex-project.org/ftp.html)


## Usage

Before you can make use of the template you need to move the LaTeX template file
into Pandocs template directory:

```
mkdir ~/.pandoc
mv your-repo-path/letter.latex ~/.pandoc/templates
```

After creating a letter written in Markdown you can compile it into PDF with the
following line:

`pandoc letter.md -s -o letter.pdf --template="letter"`


## Configuration

The following yaml variables are supported:

- `opening`
- `closing`
- `encludes`
- `author`
- `phone`
- `email`
- `place`
- `subject`
- `return-address`
- `address`
