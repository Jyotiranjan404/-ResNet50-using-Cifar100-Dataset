# Train a CNN using pretrained ResNet50 using Cifar100 Dataset.
Steps i followed here.
1. Importing some Libraries.
2. creating a fuction where i gonna perform data augmentation.
3. defining no of classes, as we know cifar 100 is having 100 no of classes.
4. loading cifar 10 model and spliting into train and test.
5. After that i Pre-processed the data.
6. creating datagen veribale to call ImageDataGenerator function to perform data augmentation operation.
7. After that i convered my output classes into categorical.
8. loading ResNet50 pre trained model.
9. in side this ResNet50 model i passed input shape 256.but my cifar 100 data set is having (32x32).i upsampled the image size.
10. Then, i called ResNet50 pretrained model.After that i created global average polling layer.
11. After that i created dense layer by using 256 nurons, activation function as "relu",Dropoout"0.25",batch normalization.
12. After that i created another dense layer to define my output by using activation function as "softmax"(for multiple classes)
13. Basically my model architecture is like 3 upsampling layers,pretrained model,1 global average pooling layer and 2 dense layer. 
14. After that i compiled my model by using loss function as "categorical_crossentropy",optimizer as "adam",metrics as "accuracy".
15. after that i started training for 5 epochs and results are below.
![rtyreyre](https://user-images.githubusercontent.com/84494071/130361767-e1020af9-eef8-4998-9cf4-816ccefe4ca2.JPG)
