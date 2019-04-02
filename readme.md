## Deep Video Deblurring for Hand-held Cameras
This is the demo code for [Deep Video Deblurring for Hand-held Cameras](http://www.cs.ubc.ca/labs/imager/tr/2017/DeepVideoDeblurring/). Given a stack of pre-aligned input frames, our network predicts a sharper central image. 

### Prepare data
- Download and unzip test videos to `dataset`, from this [link](http://www.cs.ubc.ca/labs/imager/tr/2017/DeepVideoDeblurring/DeepVideoDeblurring_Dataset.zip), or place your own test video frames under `dataset/qualitative_datasets/[video_file_name]/input`.

- Align frames in Matlab, by running
```Shell
	preprocess/launcher.m
```
Outputs should be stored at `data/testing_real_all_nostab_[alignment]` under structure
```Shell
	/image_-2
	/image_-1
	/image_0
	/image_1
	/image_2
```
Alternatively, you can download the pre-aligned qualitative videos from [here](http://www.cs.ubc.ca/labs/imager/tr/2017/DeepVideoDeblurring/testing_real_all_nostab_OF.zip), [here](http://www.cs.ubc.ca/labs/imager/tr/2017/DeepVideoDeblurring/testing_real_all_nostab_homography.zip), and [here](http://www.cs.ubc.ca/labs/imager/tr/2017/DeepVideoDeblurring/testing_real_all_nostab_nowarp.zip).

### Download pretrained weights
- Download and unzip pretrained weights into `logs`, from [here](http://www.cs.ubc.ca/labs/imager/tr/2017/DeepVideoDeblurring/pretrained.zip).

### Run prediction script
- Run script: `sh run_pred.sh`
- Results will be saved to `outImg`. 

### FAQ
- split of the training/test sets: https://github.com/shuochsu/DeepVideoDeblurring/issues/2#issuecomment-312954167

### Citation
If you find this code useful for your research, please cite:
```
@inproceedings{su2017deep,
  title={Deep Video Deblurring for Hand-held Cameras},
  author={Su, Shuochen and Delbracio, Mauricio and Wang, Jue and Sapiro, Guillermo and Heidrich, Wolfgang and Wang, Oliver},
  booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition},
  pages={1279--1288},
  year={2017}
}
```
