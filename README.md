# Fruits-360: A dataset of images containing fruits, vegetables, nuts and seeds #

## Version: 2025.03.09.1 ##

## Branch: original-size ##

A high-quality dataset of images containing fruits, vegetables, nuts and seeds.

## Dataset properties ##

Total number of images: 20976.

Training set size: 10492 images.

Validation set size: 5252 images

Test set size: 5232 images.

Number of classes: 38 (fruits, vegetables and nuts).

Image size: various (original, captured, size) pixels.

## Filename format ##

r?_image_index.jpg (e.g. r2_31.jpg)

where "r" stands for rotated fruit. "r2" means that the fruit was rotated around the 3rd axis. 

Different varieties of the same fruit (apple for instance) are stored as belonging to different classes.

## Repository structure ##

Folders [Training](Training), [Validation](Validation) and [Test](Test) contain images for training, validation and testing purposes.

## Alternate download ##

The Fruits-360 dataset can be downloaded from: 

**Kaggle** [https://www.kaggle.com/moltean/fruits](https://www.kaggle.com/moltean/fruits)

**GitHub** [https://github.com/fruits-360](https://github.com/fruits-360)

## How to cite ##

Mihai Oltean, __Fruits-360 dataset__, 2017-.

## How the Fruits-360 dataset was created ##

Fruits and vegetables were planted in the shaft of a low speed motor (3 rpm) and a short movie of 20 seconds was recorded. 

A Logitech C920 camera was used for filming the fruits. This is one of the best webcams available.

Behind the fruits I placed a white sheet of paper as background. 

However due to the variations in the lighting conditions, the background was not uniform and I wrote a dedicated algorithm which extract the fruit from the background. This algorithm is of flood fill type: 
we start from each edge of the image and we mark all pixels there, then we mark all pixels found in the neighborhood of the already marked pixels for which the distance between colors is less than a prescribed value. We repeat the previous step until no more pixels can be marked.

All marked pixels are considered as being background (which is then filled with white) and the rest of pixels are considered as belonging to the object.

The maximum value for the distance between 2 neighbor pixels is a parameter of the algorithm and is set (by trial and error) for each movie.

## History ##

Fruits were filmed at the dates given below (YYYY.MM.DD):

2017.02.25 - First fruit filmed.

2023.12.30 - Official Github repository is now [Fruits-360 on Github](https://github.com/fruits-360)

## License ##

MIT License

Copyright (c) 2017- [Mihai Oltean](https://mihaioltean.github.io)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.