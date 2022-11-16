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

## Datasets
Initially, we planned to use the [Adobe VFR dataset](https://www.dropbox.com/sh/o320sowg790cxpe/AADDmdwQ08GbciWnaC20oAmna?dl=0). Here are some sample images:<br /><img src="./lab/AdobeDataEx1.png" alt="Example1" height="40"/>
<img src="./lab/AdobeDataEx2.png" alt="Example2" height="40"/>
<img src="./lab/AdobeDataEx3.png" alt="Example3" height="40"/>
<img src="./lab/AdobeDataEx4.png" alt="Example4" height="40"/><br />
But we are faced with the following problems:
1) Unbalanced dataset
2) The lack of fonts [we need](./lab/FontsBckgr.png) in the dataset
3) Inability to generate similar images of other fonts
4) Lack of uniformity in the font (some of the images have [light letters on a dark background](./lab/AdobeDataEx4.png), some of the images have [dark letters on a light background](./lab/AdobeDataEx1.png), while the other part of the images have [letters color similar to background color](./lab/AdobeDataEx2.png) (for example, gray and dark gray).

In this regard, it was decided to generate its own dataset as a set of dark letters on a white background:
<br /><img src="./lab/OurDataEx.png" alt="ExampleSlab"/><br />
With augmentation in the form of text tilt at small angles:
<br /><img src="./lab/OurDataExAugmentation.png" alt="ExampleAugmentation"/><br />
Example of distribution by Weight parameter taking into account balancing:
<br /><img src="./lab/AugmentationHist.png" alt="AugmentedHistogram" width="565"/><br />

## Network structure
Example of a neural network structure for contrast classification (binary feature): 
<br /><img src="./lab/Network structure.png" alt="ExampleSlab" width="565"/><br />

## About

<a href="./lab/Index.ipynb"><img src="https://github.com/TyurinIvan/Font-Recognizer/raw/main/lab/Font-Recognizer.png"></a>
