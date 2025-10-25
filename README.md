# Fruits-360: A dataset of images containing fruits, vegetables, nuts and seeds #

## Version: 2025.10.25.0 ##

## Branch: original-size ##

A high-quality dataset of images containing fruits, vegetables, nuts and seeds.

## Dataset properties ##

Total number of images: 76134.

Training set size: 38122 images.

Validation set size: 19062 images

Test set size: 18950 images.

Number of classes: 110 (fruits, vegetables, nuts and seeds).

Image size: various (original, captured, size) pixels.

## Filename format ##

r?_image_index.jpg (e.g. r2_31.jpg)

where "r" stands for rotated fruit. "r2" means that the fruit was rotated around the 3rd axis. 

Different varieties of the same fruit (apple for instance) are stored as belonging to different classes.

## Repository structure ##

The images have been divided into 3 subsets: [Training](Training), [Validation](Validation) and [Test](Test).
_Training_ contains about 50% of images. _Validation_ and _Test_ each contains about 25% of images.

The set of images for each object is divided into _Training_, _Validation_ and _Test_ using the following rule:
_k_, _k + 2_ were moved to _Training_,
_k + 1_ was moved to _Validation_,
_k + 3_ was moved to _Test_.

_k_ is the index of the object ( _k_ is multiple of 4).

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

2017.02.25 - First fruit filmed.

2023.12.30 - Official Github repository is now [Fruits-360 on Github](https://github.com/fruits-360)

## License ##

CC BY-SA 4.0

Copyright (c) 2017-, [Mihai Oltean](https://mihaioltean.github.io)

You are free to:

*Share* — copy and redistribute the material in any medium or format for any purpose, even commercially.

*Adapt* — remix, transform, and build upon the material for any purpose, even commercially.

Under the following terms:

*Attribution* — You must give appropriate credit , provide a link to the license, and indicate if changes were made . You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

*ShareAlike* — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.