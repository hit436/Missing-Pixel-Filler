# Image Data Gap Filler

empty-image-filler is a python package that takes in input images, and if missing data regions are found, the function returns the images with these regions filled. These regions of missing data are filled with non-null neighboring pixels where the probability of a pixel being chosen is inversely proportional to its distance to the pixel it is filling, i.e. closer points get chosen more often. This creates a natural, dynamic filling method for the image.

Our command-line tool is intended to obscure regions of null or missing data from machine learning pattern-recognizing algorithms. More information on our work with this function can be found [here](https://drive.google.com/file/d/18LSWDsXX9PdDLoYNuzKGLzKUZEuGzAo_/view?usp=sharing). However, this package can be used to fill in an image's missing data or a given RGB value in the image for any purpose.

## Installation

Here we detail how to install our package.

## Usage

Here we explain how to use our package.

### Example

Below are some examples with missing data regions filled by our python function:

**Pre-fill:**
![beachImagesPreFill](beachImagesPreFill.png)

**Post-fill:**
![beachImagesPostFill](beachImagesPostFill.png)

## FAQs

#### What type of images can be used with the python package?

Our package works best if less than 25% of the image data is missing.

#### How does empty-image-filler recognize "missing data"?

By default, our code recognizes "missing data" as [0,0,0] RGB, i.e. black, pixels. However, the user has the option to change what RGB values are recognized as "missing data" by ..............

#### How has empty-image-filler been used before?

Our code was created as a part of research done under SpaceML and alongside NASA's Impact Team. Our goal was to reduce the effects of swath gaps found in NASA Terra and Aqua satellite images in unsupervised machine learning. More information on our work can be found [here](https://drive.google.com/file/d/18LSWDsXX9PdDLoYNuzKGLzKUZEuGzAo_/view?usp=sharing).

## Citation

If empty_image_filler is useful in your research, please consider citing
```
@article{cao2020swathgaps,
  title={Reducing Effects of Swath Gaps in Unsupervised Machine Learning},
  author={Chen, Sarah and Cao, Esther and Koul, Anirudh and Ganju, Siddha and Praveen, Satyarth and Kasam, Meher Anand},
  journal={Committee on Space Research Machine Learning for Space Sciences Workshop},
  year={2021}
}
```

https://guides.github.com/features/mastering-markdown/
