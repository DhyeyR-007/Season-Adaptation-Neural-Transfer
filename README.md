# Season-Scene-Neural-Transfer
Here in order to extend the concept of scene transfer/style transfer into an unpaired image-to-image translation, we code cycleGAN netowork in Python using Tensorflow and Keras librarires for image data processing and neural network development.\
\
The entire programming is done in Google Colaboratory.\
\
This code here is my attempt to further undertand the concept of scene transfer. Earlier using Neural Style Transfer in a very detailed format I learned a lot about style transfer and domain adaptation. Being extremely fascinated by the intuition of domain adaptation, I felt working upon the concept of season transfer is a great segue to work further upon scene adaptative object segmentation and depth estimation.

#### The dataset used here is : https://people.eecs.berkeley.edu/~taesung_park/CycleGAN/datasets/summer2winter_yosemite.zip 

Inspired by the Horse2Zebra cycleGAN methodology (which was the analogy I used during initial phases of understanding) I use the network, with suitable hyperparameters for season transfer:

![image](https://user-images.githubusercontent.com/86003669/210071831-14c2f319-6bad-4e4b-be0d-f50a202af79c.png)

### <ins> The outputs obtained here are as follows: </ins>
*From training dataset where we go from Summer(Real image) ----> Winter (Generated image) ----> Summer (Reconstructed image) (i.e. A ----> B ----> A')*

![image](https://user-images.githubusercontent.com/86003669/210072611-5991c2a7-4c0b-466d-9c7f-8f45a8bfdfd2.png)



*Now if we test the generators using data from testing dataset where we go from Summer(Real image) ----> Winter (Generated image) ----> Summer (Reconstructed image) (i.e. A ----> B ----> A')*

![image](https://user-images.githubusercontent.com/86003669/210072535-ef26703f-84ab-4e9c-a504-0e4e1c81a565.png)

The epochs, batch size, number of samples and all in all number of iterations mentioned in the code are memory intensive, i.e. fro quick training and understanding of th neural networks.\
Here to obtain the above depicted results in training, I have use approximately 7200 iterations to get the generated image and reconstructed image this good. The output may vary based upon the conditions and user requirements.
