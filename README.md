# CoffeeLeafDiseaseDetectionSystem

# **Project Description**

**Name: Coffee Leaf Disease Detetction System**

### <b> Description of the Project </b>

This project is basically performed to detect 4 different types of disease in the coffee plant and they are:
1. **Cercospora**
2. **Miner**
3. **Coffee Rust**
4. **Phoma**



#### Technology Used

* I have used the concept of **Convolutional Neural Network** to train the model. 

The model is divided into two parts:

1. **Feature Extraction part**

##Feature Extraction
                                    keras.layers.Conv2D(filters=16, kernel_size=3,activation='relu', input_shape=[224, 224, 3]),
                                    
                                    keras.layers.Conv2D(filters=32, kernel_size=3,activation='relu'),
                                    keras.layers.MaxPooling2D(pool_size=(2,2)),
                                    keras.layers.Dropout(0.25),

                                    keras.layers.Conv2D(filters=64, kernel_size=3,activation='relu'),
                                    keras.layers.MaxPooling2D(pool_size=(2,2)),
                                    keras.layers.Dropout(0.25),

                                    keras.layers.Conv2D(filters=128, kernel_size=3,activation='relu'),
                                    keras.layers.MaxPooling2D(pool_size=(2,2)),
                                    keras.layers.Dropout(0.25),

                                    keras.layers.Flatten()
      
 The feature extraction part takes in the 224 by 224  image and pass it through 4 filters, 3 Maxpooling layers and has three dropout layers that offers 25% of dropout of the internal layers.
                                    
2. **Classification Part**

                                    ## Classification part

                                    keras.layers.Dense(units = 500, activation='relu'),
                                    keras.layers.Dropout(0.4),
                                    keras.layers.Dense(units = 250, activation='relu'),
                                    keras.layers.Dropout(0.3),
                                    # output layer
                                    keras.layers.Dense(units =5, activation='softmax')
       
The classification part is pretty simple I have just implemented **Artificial Neural Network** and final layer result in 5 classification layer.
              
                                    

#### Comparing the accuracy and loss for the Training and Validation Data


![image](https://user-images.githubusercontent.com/57294417/140088511-3d62ae05-ae7b-4265-a09b-8c67944c694a.png)



**Dataset used in the project can be downloaded from below link:**

https://drive.google.com/file/d/15YHebAGrx1Vhv8-naave-R5o3Uo70jsm/view

**I followed https://www.sciencedirect.com/science/article/abs/pii/S0168169919313225 paper that highly supported me doing this project.
