<img src="https://rawgit.com/karansikka1/Foodx/master/assets/banner.png?invert_in_darkmode" align=middle/> 

# iFood-211 2018 Challenge
Being able to automatically identify the food items in an image can assist towards food intake monitoring to maintain a healthy diet. Food classification is a challenging problem due to a large number of food categories, high visual similarity between different food categories, as well as limited datasets for training deep models. In this competition, we introduce a novel dataset of 211 fine-grained (prepared) food categories with 101733 training images collected from web search engines. We provide a manually cleaned subset of 10323 images for validation and and 24088 images for testing. The goal is to learn a model to classify a given image into these food-categories. 

The main challenges are:

* Fine-grained Classes: The classes are fine-grained and visually similar. For example, the dataset has 15 different type of cakes, and 10 different types of pastas.

* Noisy Data: Since the training images are crawled from web search engines, they often include images of raw ingredients or processed and packaged food items. This is refered to as cross-domain noise. Further, due to fine-grained nature of food-categories, a training image may either be incorrectly labeled into a visually similar class or have multiple food items but is annotated with a single label. 

This competition is part of the fine-grained visual-categorization workshop ([FGVC5 workshop](https://sites.google.com/view/fgvc5/home)) at [CVPR 2018](http://cvpr2018.thecvf.com/). The winners of the challenge will be invited to present their work at the FGVC5 workshop.

## Updates
The Github page for the challenge is online

## Dates
|||
|------|---------------|
Data Released|April 25, 2018|
Submission Deadline|June, 2018|
Winners Announced|June, 2018|

## Data
There are a total of 211 food categories in the dataset. A complete list of classes is available [here](https://rawgit.com/karansikka1/Foodx/master/class_list.txt).


### Training Data
The training data consists of 101733 images from 211 classes. The training data is collected from web images and consists noisy labels.

### Validation Data
The validation data consists of 10323 images from 211 classes. The test data is collected from web images and then annotated. It does not contain noisy labels.

### Test Data
The training data consists of 24088 images from 211 classes. The test data is collected from web images and then annotated. It does not contain noisy labels.

## Evaluation
Submissions are evaluated on top 3 error rate of the predictions on test images. For each image in the test set, you must produce the top 3 confident class label. The file should contain a header as shown in the example submission file below. Besides header, there should be a row for each test image. Each row has four columns: image_name,predicted class_id 1,predicted class_id 2,predicted class_id 3, where predicted class_id 1 is the most confident class label. 

Error rate of a test image <img src="https://rawgit.com/karansikka1/Foodx/master/assets/i.png?invert_in_darkmode" width=4pt height=15pt/> with true label <img src="https://rawgit.com/karansikka1/Foodx/master/assets/g_i.png?invert_in_darkmode" width=8pt height=20pt/> and predicted labels <img src="https://rawgit.com/karansikka1/Foodx/master/assets/p_ij.png?invert_in_darkmode" align=middle width=5.642109pt height=21.60213pt/>  is:
<img src="https://rawgit.com/karansikka1/Foodx/master/assets/eq_1.png?invert_in_darkmode" align=middle width=190pt height=50pt/> 
where 
 <img src="https://rawgit.com/karansikka1/Foodx/master/assets/eq_2.png?invert_in_darkmode" align=middle width=190pt height=50pt/>.
 
The overall error score of the test dataset with <img src="https://rawgit.com/karansikka1/Foodx/master/assets/N.png?invert_in_darkmode" align=middle width=5.642109pt height=21.60213pt/> test images is computed as:

 <img src="https://rawgit.com/karansikka1/Foodx/master/assets/eq_3.png?invert_in_darkmode" align=middle width=190pt height=50pt/>.


## Submission File
image_name,pred1,pred2,pred3 </br>
test_0001,0,1,10 </br>
test_0002,1,3,5 </br>
test_0003,0,5,1 </br>

This file will have N+1 rows where N = number of test images.

## Rules

* Participants should use only the provided training and validation images for training models. No additional data is allowed. Validation data should only be used for validation.

* Collecting additional annotations for the test images is not allowed.

* Hand labeling is forbidden.

* Pretrained models (such as, trained on ImageNet) are allowed but should be properly acknowledged and cited.
 

## Terms of Use
By downloading this dataset you agree to the following terms:

* You will use the data only for non-commercial research and educational purposes.
* You will NOT distribute the above images.
* The organizers makes no representations or warranties regarding the data, including but not limited to warranties of non-infringement or fitness for a particular purpose.
* You accept full responsibility for your use of the data and shall defend and indemnify the  organizers, including its employees, officers and agents, against any and all claims arising from your use of the data, including but not limited to your use of any copies of copyrighted images that you may create from the data.

## DATA
Need to be filled

## Organizers
Karan Sikka, SRI International </br>
Parneet Kaur, Johnson and Johnson </br>
Weijun Wang, Google </br>
Ajay Divakaran, SRI International </br>

For any further inquiries please contact us at xyz@FIXME.com
