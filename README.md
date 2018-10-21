# MSDS686-Seedlings-Classification-CNN
## Summary

This paper decribes the process for developing and comparing convolutional neural networks (CNN) in a classification problem for a deep learning course. The data used in this project is the "Plant Seedling Data" from a Kaggle competition. The goal of the classification problem is to predict the species of plant seedling based on images.

The process for this project includes several components. The plant seedling training and testing data were obtained from the Kaggle website and loaded in Colab for processing. The Kaggle images are "labeled" by placement of each image in a folder with the designated label. The images were retrieved from these folders, placed into an array with the name of the folder set as the "label." Once the images are obtained, the training data is separated into images and labels. The training data is then processed as input for CNN in Keras.

Six CNN models were tested and compared to identify the most accurate model to use for the Kaggle submission. I included six of the many models I tried to show the results of simple to complex CNN models. Most of the code for this project was modified from NikKonst (2018) which along with the Chollett (2018) textbook served as a guide for the entire process. Helpful information was also obtained from classmates posting their experiences on the course discussion board.

The project was performed on Colab's tensorflow deep learning software running on Google's Tensor Processing Unit.

The model with the lowest error rate was model_N, designed by NikKonst (2018) which can be found on Kaggle at https://www.kaggle.com/nikkonst/plant-seedlings-with-cnn-and-image-processing.  Although model2 had the second best baseline error rate, it was used for the Kaggle submission due to little overfitting which hopefully would generalize well to new data. The Kaggle submission achieved a score of 0.89.  A chart comparing the models is shown below.

Overall, this project was extremely educational and fun. Going through the entire process of developing and comparing CNN models from start to finish was very beneficial.


| Model | Conv Layers | % Error | % Valid. Acc. | Seconds | Train. Parameters |
|------ | ----------- | ------- | ------------- | ------- | ----------------- | 
|model_N |  [64,64, 128,128, 256,256] | 8 | 92 | 26,586 | 3,317,580
| model2 | inception2 layers | 12 | 88 | 330 | 4,823,436
| model_A | [32,64,128,128] | 13 | 87 | 259 | 274,444
| model_B | [80,80,160,160,240] | 13 | 87 | 355 | 784,076
| model1 | inception1 layers | 17 | 83 | 301 | 7,329,548
| VGG16 | VGG16 layers | 19 | 81 | ? | 15,242,316

### References

Chollet, F. (2018). Deep Learning with Python. Shelter Island, NY. Manning Publications Co.

CoLab Drive FUSE example.ipynb (2018) Retrieved from https://colab.research.google.com/drive/1srw_HFWQ2SMgmWIawucXfusGzrj1_U0q.

Kaggle (2018). Retrieved from https://www.kaggle.com/c/plant-seedlings-classification/data.

Kazachok, M. (2018). Keras simple model (0.97103 Best Public Score). Retrieved from https://www.kaggle.com/miklgr500/keras-simple-model-0-97103-best-public-score

Kim, G. (2018). Regis Course 686 Deep Learning Class homework solutions

NikKonst (2018). Plant seedlings with cnn and image processing. Retrieved from https://www.kaggle.com/nikkonst/plant-seedlings-with-cnn-and-image-processing
