<img src="https://rawgit.com/karansikka1/Foodx/master/assets/banner.png?invert_in_darkmode" align=middle/> 

# iFood 2018 Challenge @ [FGVC5](https://sites.google.com/view/fgvc5/home), [CVPR 2018](http://cvpr2018.thecvf.com/)
Being able to automatically identify the food items in an image can assist towards food intake monitoring to maintain a healthy diet. Food classification is a challenging problem due to the large number of food categories, high visual similarity between different food categories, as well as the lack of datasets that are large enough for training deep models. In this competition, we introduce a new dataset of 211 fine-grained (prepared) food categories with 101733 training images collected from the web. We provide human verified labels for both the validation set of 10323 images and the test set of 24088 images. The goal is to build a model to predict the fine-grained food-category label given an image.

The main challenges are:

* Fine-grained Classes: The classes are fine-grained and visually similar. For example, the dataset has 15 different types of cakes, and 10 different types of pastas.

* Noisy Data: Since the training images are crawled from web search engines, they often include images of raw ingredients or processed and packaged food items. This is refered to as cross-domain noise. Further, due to the fine-grained nature of food-categories, a training image may either be incorrectly labeled into a visually similar class or be annotated with with a single label despite having multiple food items. 

This competition is part of the fine-grained visual-categorization workshop ([FGVC5 workshop](https://sites.google.com/view/fgvc5/home)) at [CVPR 2018](http://cvpr2018.thecvf.com/). The winners of the challenge will be invited to present their work at the FGVC5 workshop.

## Updates
4/25/18: The Github page for the challenge is online

4/25/18: Training, validation and test data is available

## Dates
|||
|------|---------------|
Data Released|April 25, 2018|
Submission Deadline|June, 2018|
Winners Announced|June, 2018|

## Evaluation Server
(Will be updated soon)

## Data
There is a total of 211 food categories in the dataset. A complete list of classes is available [here](https://rawgit.com/karansikka1/Foodx/master/class_list.txt).


### Training Data
The training data consists of 101733 images from 211 classes. The training data is collected from web images and consists of noisy labels.

### Validation Data
The validation data consists of 10323 images from 211 classes. The test data is collected from web images and then annotated. It does not contain noisy labels.

### Test Data
The training data consists of 24088 images from 211 classes. The test data is collected from web images and then annotated. It does not contain noisy labels.

## Data Download and Format
[Annotations](https://food-x.s3.amazonaws.com/annot.tar) (2.6 MB)
* Running `md5sum annot.tar` on the tar file should produce `6a3934bd96c1bc1df4822c16a8191158`
* The tar contains 4 files
     * class_list.txt: Contains the names of 211 class labels. This can be used to map class_ids with class names.
     * train_info.csv: Each line of this csv containing the "image_name,label" pair for training data. For example, "train_00000.jpg,94" refers to image train_00000.jpg having class_id 94. The class_id can be mapped to class name using class_list.txt. 
     * val_info.csv: Same as train_info.csv for validation data.
     * test_info.csv: csv only provides the list of test images.
 * We provide separate tars for train, val and test images as mentioned below.

[Train Images](https://food-x.s3.amazonaws.com/train.tar) (2 GB)
* Running `md5sum train.tar` on the tar file should produce `8a8b099e158800f2bb4883992ef35230`
* Contains training images.
* For label information see annotation file train_info.csv. 

[Validation Images](https://food-x.s3.amazonaws.com/val.tar) (200 MB)
* Running `md5sum val.tar` on the tar file should produce `51d666f9ab34833c117dfe6c06e3bec3`
* Contains validation images.
* For label information see annotation file val_info.csv. 

[Test Images](https://food-x.s3.amazonaws.com/test.tar) (467 MB)
* Running `md5sum train.tar` on the tar file should produce `d7b89119c434b4b01868b7307cc22a94`
* Contains testing images.
* The label will be evaluation on the evaluation server.

## Evaluation
We follow a similar metric to the classification tasks of the [ILSVRC](http://image-net.org/challenges/LSVRC/2016/index#scene). For each image <img src="https://rawgit.com/visipedia/inat_comp/master/svgs/77a3b857d53fb44e33b53e4c8b68351a.svg?invert_in_darkmode" align=middle width=5.642109pt height=21.60213pt/>, an algorithm will produce 3 labels <img src="https://rawgit.com/visipedia/inat_comp/master/svgs/655bedbaf4a65f397b5041d0fdecde4c.svg?invert_in_darkmode" align=middle width=15.601905pt height=22.74591pt/>, <img src="https://rawgit.com/visipedia/inat_comp/master/svgs/946e592e2b2753a9272767ae3dd5b9a9.svg?invert_in_darkmode" align=middle width=82.4274pt height=21.60213pt/>. For this competition each image has one ground truth label <img src="https://rawgit.com/visipedia/inat_comp/master/svgs/681a37b53b66acbc455e39ca3e6f1c41.svg?invert_in_darkmode" align=middle width=12.444795pt height=14.10255pt/>, and the error for that image is:
<p align="center"><img src="https://rawgit.com/visipedia/inat_comp/master/svgs/7a42826f81c53c77e0fef3c827238d25.svg?invert_in_darkmode" align=middle width=123.403665pt height=24.865665pt/></p>
Where
<p align="center"><img src="https://rawgit.com/visipedia/inat_comp/master/svgs/7a45c501d5042bd031a267f008fa2ae6.svg?invert_in_darkmode" align=middle width=190.2021pt height=49.13139pt/></p>

The overall error score for an algorithm is the average error over all <img src="https://rawgit.com/visipedia/inat_comp/master/svgs/f9c4988898e7f532b9f826a75014ed3c.svg?invert_in_darkmode" align=middle width=14.94405pt height=22.38192pt/> test images:
<p align="center"><img src="https://rawgit.com/visipedia/inat_comp/master/svgs/444adcac0c7cbb4a8419ee1484625349.svg?invert_in_darkmode" align=middle width=118.05123pt height=41.069655pt/></p>


## Submission File Format
```
image_name,label1 label2 label3 
test_0001.jpg,0 1 10 
test_0002.jpg,1 3 5 
test_0003.jpg,0 5 1 
```

Please include the header as shown above for correct parsing. Each line will correspond to one test image and will be identified by the id (e.g test_0001.jpg refers to image test_0001.jpg) for computing accuracy.

## Rules

* Participants should use only the provided training and validation images for training models. Validation data should only be used for validation. 
* We do not allow augmentation with any prior datasets or additional data during training. Pretraining with additional data (such as ImageNet) is allowed as long as participants do not actively collect additional data for the target categories in iFood 2018 challenge. 
Use of any external data should be properly acknowledged and cited. The general rule is that we want participants to use only the provided training and validation images to train a model to classify the test images.
* Collecting additional annotations for the train images is not allowed. 
* Hand labeling of test data is not allowed and will lead to disqualification.
 


## Terms of Use
By downloading this dataset you agree to the following terms:

* You will use the data only for non-commercial research and educational purposes.
* You will NOT distribute the above images.
* The organizers make no representations or warranties regarding the data, including but not limited to warranties of non-infringement or fitness for a particular purpose.
* You accept full responsibility for your use of the data and shall defend and indemnify the  organizers, including its employees, officers and agents, against any and all claims arising from your use of the data, including but not limited to your use of any copies of copyrighted images that you may create from the data.

## Acknowledgement
We would like to thank [CVDF Foundation](http://www.cvdfoundation.org/) and Tsung-Yi Lin for helping us with hosting the data.

## Organizers
Karan Sikka, SRI International </br>
Parneet Kaur\*, Johnson and Johnson </br>
Weijun Wang, Google </br>
Ajay Divakaran, SRI International </br>
Serge Belongie, Cornell University and Cornell Tech </br>

\*work done while Parneet was an intern at SRI International

For any further inquiries please contact us at ifoodcvpr18@gmail.com
