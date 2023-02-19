# SAR_LPNET_Code
First of all import all required libraries
Then run the section Model
In model section you can chnage the below parameters as per your choice
num_pyramids = 7  # number of pyramid levels  ( Increasing levels can increase performance but there will be an increase in number of parameters)
num_blocks = 7    # number of recursive blocks
num_feature = 32  # number of feature maps
num_channels = 1  # number of input's channels ( incase of RGB images number of channels will be 3)
In Training section you can tune hyper parameters which may include learning rate, epoch and such other parameters
Also in training file there are two paths for saving model 
save_model_path = './model/realmodel/sp'  # path of saved model
model_name = 'model-epoch'    # name of saved model
In Training section also to load training images you will see below paths
input_path = '../SAR_LPNET_NEW/inp/' # Noisy images   (Create a directory like   *inp* and give that directory path to the input path, put noisy images in inp directory)
gt_path = '../SAR_LPNET_NEW/lab/'    # ground truth   (Create a directory like   *lab* and give that directory path to the input path, also place all your ground truth in this directory)
After doing above seeting start training your model on given set of images 
Once model is fully trained then its time to test images
For testing run the test section of colab file 
In testing section you do proper arrangement for the following paths
model_path = './model/pre_trained/with_attention_Real32'   ( This is the path of model that you have eralier mentioned in training section)
pre_trained_model_path = '/content/drive/MyDrive/SAR_LPNET_NEW/model/realmodel/sp/model-epoch-24000'

img_path = '../SAR_LPNET_NEW/testimages/'           (now craete a directory named with test images and put some test images in this directory)
results_path = './test_img/rez/' # the path of de-noised images  ( This is the path where your test images result will be save)
