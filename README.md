# Classification Of Plants Using CNN
This project is part of the exam of Artificial Neural Networks and Deep Learning course at Politecnico
di Milano, and it corresponds to the first challenge. The aim of the project is to classify species of
plants, which are divided into categories according to the species of the plant to which they belong.
Being a classification problem, given an image, the goal is to predict the correct class label.


The typical deep learning pipeline will be used, building a CNN from scratch and implementing
transfer learning and fine tuning with 6 CNN: ResNet152V2, InceptionV3 InceptionResNetV2, VGG16, DenseNet201, Xception, EfficientNetB0. Tensorflow and in particular
Keras framework will be used.


It is possible to check all the details of the project from the pdf in this repository, together with the notebooks of the models.

## Data
The dataset consists of 3543 images of plants distributed in 8 different species.

## Preprocessing
In order to solve the unbalanceness of the classes, the initial dataset has been oversampled. An alternative of this approach could have been undersampling, but for the current dataset this option is not efficient because the dataset contains few images.

The splitting of the initial dataset has been performed obtaining 2 sets: a training set with 80% of the initial data and a validation
set with 20% of the initial data. The test set was not created and splitted because the model will
be tested on a hidden and private test set.

Data augmentation is a technique used to increase the diversity of the training set by applying
random (but realistic) transformations. It has been the first technique used in order to increase the
number of images in the training set. Many transformations have been used: Height Shift Range, Width Shift Range, Zoom Range, Horizontal Flip, Shear Range, Fill Mode.

## Models
The models proposed are 7: a network from scratch, ResNet152V2, InceptionV3, InceptionResNetV2,
VGG16, DenseNet201, Xception, EfficientNetB0. All the model except the network from scratch have
been used as feature extractor, using the transfer learning paradigm.

## Results
Implementing a network from scratch helped to explore the problem and understand what are the most
suitable structures for a network based on this specific problem of classification. The performances
where not low, since the accuracy on the validation reached 78%.
Transfer learning was the tool that obtained the best result, since very powerful model has been
used to extract in an optimized and efficient way the features form the images, being already trained
with a hige corpus of images.
All the models that ahve been used as feature extractor plus a fully connected part related to the
problem performed quite well, having accuracy above 85%. EfficientNet was the best among the other,
with high performances, around 91% in the accuracy of the validation set, and 82% on the hidden test
set. 

## Conclusions
Starting from scratch, it was hard to make a good network, due to the limited number of images.
Therefore, using transfer learning was a good choice in terms of training time, as well as initialization,
since those networks already had optimized weights. However, very powerful networks are not always
the way to go because they really depend on the problem faced.

## Group Components
| Cognome | Nome | e-mail | Codice Persona |
| --- | --- | --- | --- |
| La Greca  | Michele Carlo | michelecarlo.lagreca@mail.polimi.it | 10864460 |
| Giuffrida |  Andrea | andrea.giuffrida@mail.polimi.it | 10643540 |
| Nicolis |  Nicholas | nicholas.nicolis@mail.polimi.it | 10867841 |


