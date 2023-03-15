# Image Recognition of Pests Bitten Photo Using Convolutional Neural Network of Deep Learning

At first we collected the images of three pests and the wounds bitten by them to build an insect image dataset and a wounds image dataset. 
Data augmentation is necessary to enhance features of datasets. After data preprocess is done, model training comes in handy. 
The deep learning model we adopted is CNN with high-quality performance on image recognition. 
Last but not least, the user interface of software application is key to make the concept of our study popular. 
We developed 3 versions of user interface under PC, server, and mobile-phone to meet all requirements shown below. 

<img width="533" alt="image" src="https://user-images.githubusercontent.com/109503040/225416820-15e97bc1-83b2-46f7-aa5b-c16d56a6a438.png">


## Data Preprocessing
First, we composed two dataset, one is for insects, the other is for wounds.
Second, We applied noise process on the images with complicated background, 
meaning that we screened the main characteristics out of these images and removed all the noise that might be the obstacle for our model training.
Third, it’s necessary to make them in the same condition for the model training in easier way. 
Thus, we resized them into the size of 256 256 pixels and converted all the images file format into .png or .jpg.

## Data Augmentation
Lack of high-quality dataset will give rise to poor performance for model training. 
However, collecting enough quality data to train a model to perform well is often prohibitively difficult. 
So, there's where data augmentation comes into use.

## Model Training
The modern existing model training is supported by ten-thousands of data in database. 
In comparison with the mature CNN training, hundreds of images dataset in this study has low compatibility with the existing CNN model. 
Therefore, we researched on better architecture of CNN model to match the small-scale dataset. 
The following steps are the model training being carried out: data division-> normalization-> neural network

## Model Architecture
Overall, the convolutional layers were comprised of 3x3 filters with the number of kernels increasing from 16 in first layer, to 32 in the second, up to 64 in the third layer. 
Then, the third pooling layer was connected to one ‘dropout’ layer which was main to refrain the accuracy curve from overfitting. 
After that, a ‘flatten’ layer was applied behind dropout. The main function of flatten layer is to reshape the tensor into the shape equaling to the number of elements contained in tensor non-including the batch dimension. 
Finally, network was completed by adding 2 fully connected layers, with 128 neurons in the second-last layer and 3 neurons for prediction of our analysis in the last layer. 
For activation function, we used ‘rectified linear unit (ReLU)’ in all the layers.

<img width="608" alt="image" src="https://user-images.githubusercontent.com/109503040/225416936-da29b854-bae6-4218-99e6-b837697c057b.png">


## Training Result
After adjusting the model to the above-mentioned type (3 convolution layers with pooling, one dropout layer, one flatten layers, and two fully connected layers), we got the improvement in the performance of accuracy.  

<img width="432" alt="image" src="https://user-images.githubusercontent.com/109503040/225417056-db895293-4ceb-431d-ac5d-eea66b6b4f28.png">


## User Interface
We designed 3 versions of user interface( PC , Server, Mobile-phone version ) on the basis of PC and mobile phone to  meet all requirements.
### 1.PC version
We constructed the user interface of MS Window OS by C#.
<img width="711" alt="image" src="https://user-images.githubusercontent.com/109503040/225417279-3443e885-889f-437c-82de-caac3a8ffcf8.png">


### 2.Server version- 
Different from the PC version, the server version is developed with Flask, a web development tool of Python, and ngrok. 
With the function of ngrok, we could build a public HTTPs URL for users to upload their wound images via internet. 
Web server is comprised of ‘Apache’, ‘uWSGI’, and ‘Flask’. 
 ‘Apache’ as a backward agency server is responsible for replying the request and response between users and our system.
  
  <img width="781" alt="image" src="https://user-images.githubusercontent.com/109503040/225417413-d1d166ab-e924-4f03-90c8-5cd2b38d749d.png"> <img width="526" alt="image" src="https://user-images.githubusercontent.com/109503040/225417507-b33f84de-b60d-46aa-98e8-11d710bfef19.png">


### 3.mobile-phone vesion
Allows users to use camera to take the picture and upload it to recognize the wounds in our system.

<img width="574" alt="image" src="https://user-images.githubusercontent.com/109503040/225417568-d4f0ef00-a082-465d-bdba-0d9b4cf8c02a.png">


