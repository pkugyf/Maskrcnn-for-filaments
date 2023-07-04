# Maskrcnn-for-filaments

Please download the code through the following link:
https://www.icloud.com.cn/iclouddrive/0ddKjaLvZxXBR6nrhsgu8eo0w#maskrcnn%5Ffor%5Ffilament

The code is base on mask RCNN and is a pre-trained model (savedweights_good.h5) to detect large-scale filaments in the Milky Way is contained. To learn about mask RCNN and how to install the environment, please refer to the mask RCNN official github:
https://github.com/matterport/Mask_RCNN
We did some changes to the original mask RCNN code:
1. The loss function is replaced by focal loss
2. We add augmentation containing flipping (both horizontal and vertical) and rotating (90˚, 180˚, 270˚)

## Usage
You can you train_test.ipynb to detect filaments or train your own model.
If you only want to use our trained model to detect filaments, you can drag your iamges to the folder "images" and run the "detect only" cell. The results will be in the folder "detect".
If you want to train your own model, you should firstly label your image with labelme (https://github.com/wkentaro/labelme) and drag the labeled data to the folder "mydata". Then download the pretrained COCO model (https://github.com/matterport/Mask_RCNN/releases/tag/v2.0) and run the "Train" cell to train your model. Parameter in the "Train" cell may be adjusted depending on your data. After finishing training, you can run the "Have trained your own model and inspect the result" cell to inspect the results.
