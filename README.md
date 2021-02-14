# CMActivities-DataSet

## More Details about the Dataset
See the following publication for more details on the data processing and collection process. Please cite the following paper when using the dataset. We have provided the sample training scripts to show the usage of the dataset along with the model architectures.

```
@inproceedings{xing2018enabling,
  title={Enabling Edge Devices that Learn from Each Other: Cross Modal Training for Activity Recognition},
  author={Xing, Tianwei and Sandha, Sandeep Singh and Balaji, Bharathan and Chakraborty, Supriyo and Srivastava, Mani},
  booktitle={Proceedings of the 1st International Workshop on Edge Systems, Analytics and Networking},
  pages={37--42},
  year={2018},
  organization={ACM}
}
```

## Data Collection Procedure
CMActivities dataset contains video, audio, and IMU modalities collected using two smartphones from users performing activities. We refer to the users performing activities as performers hereafter. An observer is holding the first smartphone which is used to record and timestamp the video (along with audio) of the performers. In this way, the first smartphone is acting as an ambient sensor which is recording (video and audio) of the performer. The second smartphone was in the trouser’s front pocket of the performers. The second smartphone was used to timestamp the IMU data captured from the left and right wrist sensors worn by the performers. Both smartphones were synchronized using NTP.

CMActivities dataset is collected from two performers doing seven activities (upstairs, downstairs, walk, run, jump, wash hand and jumping jack). Every data collection session roughly lasted for 10 seconds, where the performer performed a singular activity. The training split is generated from the 624 training sessions. The test split is generated from the 71 test sessions. Each split contains the data from both performers. The validation split is generated by using a part of the training sessions. 


## Released Data
- The audio and IMU windowed samples are released. Audio samples are processed, and 193 features are extracted. IMU samples are available in raw form.
- The training, validation, and test samples are available below.
- [Training samples download](https://drive.google.com/file/d/1S9yFuHarB6jPD11Ddv87oG30TgY5ivDN/view?usp=sharing)
- [Validation samples download](https://drive.google.com/file/d/12s-eaw5w-X1jN2uS0x0DYM9CFAicwmnj/view?usp=sharing)
- [Test samples download](https://drive.google.com/file/d/1A5SW8ttsYzYKTvoqWdRJ_e5gQLJ67C2I/view?usp=sharing)
- More data processing details are in the publication.
- We plan to release the video samples using the intermediate representation soon. 

## Sample Model Training Scripts
### Audio Model
- [Audio Model Training Notebook](https://github.com/nesl/CMActivities-DataSet/blob/master/Audio_Model_Example.ipynb)
- Training accuracy: 99.9%
- Validation accuracy: 99.5%
- Test accuracy: 90.9%

### IMU Model
- [IMU Model Training Notebook](https://github.com/nesl/CMActivities-DataSet/blob/master/IMU_Model_Example.ipynb)
- Training accuracy: 99.8%
- Validation accuracy: 95%
- Test accuracy: 90.5%

## Time-shift Data Augmentation Code
```
@inproceedings{sandha2020time,
  title={Time awareness in deep learning-based multimodal fusion across smartphone platforms},
  author={Sandha, Sandeep Singh and Noor, Joseph and Anwar, Fatima M and Srivastava, Mani},
  booktitle={2020 IEEE/ACM Fifth International Conference on Internet-of-Things Design and Implementation (IoTDI)},
  pages={149--156},
  year={2020},
  organization={IEEE}
}
```
## The following notebooks are written with comments for Time-shift data augmentation

- Fusion_Training_Vanilla.ipynb: Vanilla fusion training code with audio and IMU modalities synced.
- Augmentation_Data_generation.ipynb: Create augmented training data by introducing artificial errors between audio and IMU modalities.
- Fusion_Training_Augmented_1000ms.ipynb: Training fusion model with 1000ms time-shift augmentation.
- Testing_Time_Shifting_1000ms.ipynb: Tests the vanilla model and augmented model on the testing data by introducing errors in the test data.
