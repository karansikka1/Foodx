FIXME: Add figure for banner

# iFood-211 2018 Challenge
Being able to automatically identify the food items in an image can assist towards food intake monitoring to maintain a healthy diet. Food classification is a challenging problem due to a large number of food categories, high visual similarity between different food categories as well as limited datasets for training deep models. In this competition, we introduce a novel dataset of 211 fine-grained food categories (prepared, not raw) with FIXME training images collected from web. We also provide manually cleaned data for validation and test sets. The goal is to learn a model from training data and correctly classify a test image.

The main challenges are:

* Fine-grained Classes: The classes are fine-grained and visually similar. For example, the dataset has FIXME different type of cakes, FIXME different types of pastas and FIXME different types of seafood.

* Cross-domain Noise: Along with the images of cooked food items,
the training data includes images of raw ingredients or processed and packaged food items.

* Cross-category Noise: A training image may have multiple food items but it has only one label as its ground truth. 

This competition is part of the fine-grained visual-categorization workshop ([FGVC5 workshop](https://sites.google.com/view/fgvc5/home)) at [CVPR 2018](http://cvpr2018.thecvf.com/). The winners of the challenge will be invited to present their work at the FGVC5 workshop.

## Dates
|||
|------|---------------|
Data Released|April 15, 2018|
Submission Deadline|June FIXME, 2018|
Winners Announced|June FIXME, 2018|

## Data
There are a total of FIXME food items (classes) in the dataset. A complete list of classes is available [here](FIXME:add classes.txt with format class_id, class_name).


### Training Data
The training data consists of FIXME images from FIXME classes. Each class has FIXME(enter range 400-700) images. The training data is collected from web images and consists noisy labels.

### Validation Data
The training data consists of FIXME images from FIXME classes. The test data is collected from web images and then annotated. It does not contain noisy labels.

### Test Data
The training data consists of FIXME images from FIXME classes. The test data is collected from web images and then annotated. It does not contain noisy labels.

## Evaluation
Submissions are evaluated on top 3 error rate of the predictions on test images. For each image in the test set, you must produce the top 3 confident class label. The file should contain a header as shown in the example submission file below. Besides header, there should be a row for each test image. Each row has four columns: image_name,predicted class_id 1,predicted class_id 2,predicted class_id 3, where predicted class_id 1 is the most confident class label. 

Error rate of a single test image![equation](http://www.sciweavers.org/tex2img.php?eq=i&bc=White&fc=Black&im=jpg&fs=12&ff=modern&edit=0) with true label ![equation](http://www.sciweavers.org/tex2img.php?eq=t_i&bc=White&fc=Black&im=jpg&fs=12&ff=modern&edit=0) and predicted labels ![equation](http://www.sciweavers.org/tex2img.php?eq=t_ij&bc=White&fc=Black&im=jpg&fs=12&ff=modern&edit=0) is:

![equation](http://www.sciweavers.org/tex2img.php?eq=e_i%20%3D%20%5Cmin_j%20d%28t_i%2Cp_%7Bij%7D%29&bc=White&fc=Black&im=jpg&fs=12&ff=modern&edit=0), 


where ![equation](http://www.sciweavers.org/tex2img.php?eq=d%28x%2Cy%29%20%3D%5Cbegin%7Bcases%7D0%2C%20%26%20if%20x%20%3D%20y%5C%5C1%2C%20%26%20otherwise%5Cend%7Bcases%7D&bc=White&fc=Black&im=jpg&fs=12&ff=modern&edit=0).

The overall error score of the test dataset with ![equation](http://www.sciweavers.org/tex2img.php?eq=N&bc=White&fc=Black&im=jpg&fs=12&ff=modern&edit=0) test images is computed as:

![equation](http://www.sciweavers.org/tex2img.php?eq=score%20%3D%20%5Cfrac%7B1%7D%7BN%7D%20%5Csum_i%7Be_i%7D&bc=White&fc=Black&im=jpg&fs=12&ff=modern&edit=0)


## Submission File
image_name,pred1,pred2,pred3 </br>
test_0001,0,1,10 </br>
test_0002,1,3,5 </br>
test_0003,0,5,1 </br>

This file will have $N+1$ rows where $N$ = number of test images.

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
SRI International
Google 
