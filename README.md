FIXME: Add figure for banner

# iFood-211 2018 Challenge
Being able to automatically identify the food items in an image can assist towards food intake monitoring to maintain a healthy diet. Food classification is a challenging problem due to a large number of food categories, high visual similarity between different food categories as well as limited datasets for training deep models. In this competition, we introduce a novel dataset of 211 fine-grained food categories (prepared, not raw) with FIXME training images. The goal is to learn a model from training data to correctly classify the food class in a test image.

FIXME(ksikka-comment): Parneet mention that we crawl data from web images in the intro and also provide a manually cleaned set. Our future aim is to expand these categories and so on. 

The main challenges are:

* Fine-grained Classes: The classes are fine-grained and visually similar. For example, the dataset has FIXME different type of cakes, FIXME different types of pastas and FIXME different types of seafood.

* Cross-domain Noise: Along with the images of cooked food items,
the training data includes images of raw ingredients or processed and packaged food items.

* Cross-category Noise: A training image may have multiple food items but it has only one label as its ground truth. 

FIXME: add images for above

This competition is part of the fine-grained visual-categorization workshop ([FGVC5 workshop](https://sites.google.com/view/fgvc5/home)) at [CVPR 2018](http://cvpr2018.thecvf.com/). The winners of the challenge will be invited to present their work at the FGVC5 workshop.

## Dates
|||
|------|---------------|
Data Released|April 15, 2018|
Submission Deadline|June FIXME, 2018|
Winners Announced|June FIXME, 2018|

## Data
There are a total of FIXME food items (classes) in the dataset. A complete list of classes is available [here](FIXME:add classes.txt).


### Training Data
The training data consists of FIXME images from FIXME classes. Each class has FIXME(enter range 400-700) images. The training data is collected from web images and consists noisy labels.

### Validation Data
The training data consists of FIXME images from FIXME classes. The test data is collected from web images and then annotated. It does not contain noisy labels.

### Test Data
The training data consists of FIXME images from FIXME classes. The test data is collected from web images and then annotated. It does not contain noisy labels.

## Evaluation

## Submission File

## Rules

* Participants should use only the provided training and validation images for training models. No additional data is allowed.

* Collecting additional annotations for the test images is not allowed.

* Hand labeling is forbidden.

* Pretrained models (such as, trained on ImageNet) are allowed but should be properly acknowledged and cited.
 

## Terms of Use
KARAN: please check these based on the hosting platform of dataset and get it reviewed by Ajay as well. I used the same as iNaturalist

By downloading this dataset you agree to the following terms:

* You will use the data only for non-commercial research and educational purposes.
* You will NOT distribute the above images.
* The organizers makes no representations or warranties regarding the data, including but not limited to warranties of non-infringement or fitness for a particular purpose.
* You accept full responsibility for your use of the data and shall defend and indemnify the  organizers, including its employees, officers and agents, against any and all claims arising from your use of the data, including but not limited to your use of any copies of copyrighted images that you may create from the data.


## Co-organizers
FIXME: Add SRI and Google logos
