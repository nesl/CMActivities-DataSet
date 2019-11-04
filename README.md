# CMActivities-DataSet

## More details about the dataset
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

## Released data
- The audio and IMU windowed samples are released. Audio samples are processed, and 193 features are extracted. IMU samples are available in raw form.
- The training, validation, and test samples are available.
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
