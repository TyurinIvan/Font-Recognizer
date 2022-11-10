# Font-Recognizer

## Description

This project was created to recognize the font from the uploaded image. After loading the image, it is run through 7 pre-trained neural networks in order to determine the typographic parameters of the font. The recognized parameters include:
  1) Is the font similar to Handwritten or Not Handwritten
  &emsp;<a href="./classificators/NonBinaryImageClassificator.ipynb"><img src="https://img.shields.io/badge/Not%20Handwritten-%E3%85%A4%20Handwritten%20%E3%85%A4-dfd.svg"></a><br />
  3) Does the font belong to the monospaced or display class
  &emsp;<a href="./classificators/NonBinaryImageClassificator.ipynb"><img src="https://img.shields.io/badge/Monospaced-%23FFFFCC"></a>
        <a href="./classificators/NonBinaryImageClassificator.ipynb"><img src="https://img.shields.io/badge/Display-%23CCCCFF"></a><br />
  3) Does the font contain serifs or does it not contain
  &emsp;<a href="./classificators/NonBinaryImageClassificator.ipynb"><img src="https://img.shields.io/badge/Sans--Serif-%E3%85%A4%20%20Serif%20%20%E3%85%A4-dfd.svg" ></a><br />
  4) Font thickness
  &emsp;<a href="./classificators/WeightClassificator.ipynb"><img src="https://img.shields.io/badge/Ultralight-%23FFCC77"></a>
        <a href="./classificators/WeightClassificator.ipynb"><img src="https://img.shields.io/badge/Thin-%23FFCC88"></a>
        <a href="./classificators/WeightClassificator.ipynb"><img src="https://img.shields.io/badge/Light-%23FFCC99"></a>
        <a href="./classificators/WeightClassificator.ipynb"><img src="https://img.shields.io/badge/Regular-%23FFCCAA"></a>
        <a href="./classificators/WeightClassificator.ipynb"><img src="https://img.shields.io/badge/Medium-%23FFCCBB"></a>
        <a href="./classificators/WeightClassificator.ipynb"><img src="https://img.shields.io/badge/SemiBold-%23FFCCCC"></a>
        <a href="./classificators/WeightClassificator.ipynb"><img src="https://img.shields.io/badge/Bold-%23FFCCDD"></a>
        <a href="./classificators/WeightClassificator.ipynb"><img src="https://img.shields.io/badge/Heavy-%23FFCCEE"></a>
        <a href="./classificators/WeightClassificator.ipynb"><img src="https://img.shields.io/badge/Black-%23FFCCFF"></a><br />
  5) Font tilt
  &emsp;<a href="./classificators/SlabClassificator.ipynb"><img src="https://img.shields.io/badge/Not%20Oblique-%E3%85%A4%20Oblique%20%E3%85%A4-dfd.svg"></a><br />
  6) Font width
  &emsp;<a href="./classificators/WidthClassificator.ipynb"><img src="https://img.shields.io/badge/Condensed-%23AA88AA"></a>
        <a href="./classificators/WidthClassificator.ipynb"><img src="https://img.shields.io/badge/Narrow-%23AA99AA"></a>
        <a href="./classificators/WidthClassificator.ipynb"><img src="https://img.shields.io/badge/Wide-%23AAAAAA"></a><br />
  7) Font contrast
  &emsp;<a href="./classificators/ContrastClassificator.ipynb"><img src="https://img.shields.io/badge/Not%20High%20Contrast-%E3%85%A4%20High%20Contras%20%E3%85%A4-dfd.svg" width="200" ></a><br />
  


## How to Use this Source

- You can navigate using the [table of content](./lab/Index.ipynb).
- You can watch final result of recognition in this repository's [tests](tests) directory.
- Launch executable versions of these notebooks using [Google Colab](http://colab.research.google.com): [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/Index.ipynb)

## What fonts we used
We used free fonts from [Google Fonts](https://fonts.google.com/) and [Font Squirrel](https://www.fontsquirrel.com/). For more fonts example you can visit [Font Tag page](https://www.fontsquirrel.com/fonts/list/tag). The parameters determined by the neural network were selected based on Font Squirrel tags.

<a href="https://www.fontsquirrel.com/"><img src="./lab/fs.png" height="40"></a>
<a href="https://fonts.google.com/"><img src="./lab/gf.png" height="40"></a>

## About

<a href="./lab/Index.ipynb"><img src="https://github.com/TyurinIvan/Font-Recognizer/raw/main/lab/Font-Recognizer.png"></a>
