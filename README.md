# background-remover

## ```Background_Removal.ipynb```
This Notebook has been created for removing backgrounds fron images, using primarily two methods

1.   Deep Learning (Facebook's Detectron2 Pre-Trained Models)
2.   Classical Computer Vision (Experimental) (This approach is more of an experimental one, intended to not be the baseline, but as a method to understand more about basics of computer vision)

## PLEASE OPEN THE SOLUTION IN GOOGLE COLAB
- Preview the `Background_Removal.ipynb` in GitHub 
- Click `Open In Colab`

## Instructions for using `Deep Learning` based solution - 

1. Switch to a GPU Runtime offered by Google Colab (Runtime-> Change Runtime Type -> GPU )
2. Install the libraries by running the `Install (Run Once) (USE GPU RUNTIME)` Tab
3. The runtime **WILL Crash**, let it ,as it is required to restart the runtime.
4. Expand the `Import Libraries and Upload Images` Tab
5. Upload the foreground and background images as prompted by the cell which is running, and let it upload.
6. Expand the `Approach 1 - Detectron2` Tab
7. Expand the `Input Area - Play with these parameters`, and edit the parameters accordingly. For a good baseline to start working with tick the `USE_DEFAULT` check-box and run the cell.
8. Run all the cells within the `Functions` Tab, no need to open.
9. Expand the Display and run all cells. Enjoy the output.

NOTE - The first run of every model takes more time than usual, because the notebook downloads each model the first time it is required. The subsequent calls to the model don't require downloading.

## Instructions for using `Classical CV` based solution - 
1. Restart the Runtime `Ctrl+M` and repeat step 2
2. Repeat Steps 4 and 5
3. Expand the `Approach 2 - Classical CV (Experimental)` Tab
4. Repeat Step 7, but for the current expanded Tab.
5. Repeat Step 8, but for the current expanded Tab.
6. Repeat Step 9, but for the current expanded Tab.

## Theoretical Concepts and Code Inspirations - 
For Deeep Learning Based solution - 
1. https://ai.facebook.com/blog/-detectron2-a-pytorch-based-modular-object-detection-library-/
2. https://github.com/facebookresearch/detectron2
3. https://www.jeremyjordan.me/semantic-segmentation/

For the Computer Vision Based Solution - 
1. https://docs.opencv.org/3.4/d4/d73/tutorial_py_contours_begin.html#:~:text=Contours%20can%20be%20explained%20simply,and%20object%20detection%20and%20recognition.&text=In%20OpenCV%2C%20finding%20contours%20is,white%20object%20from%20black%20background.
2. https://docs.opencv.org/master/d4/d13/tutorial_py_filtering.html
3. https://radiant-brushlands-42789.herokuapp.com/towardsdatascience.com/background-removal-with-python-b61671d1508a
4. https://pillow.readthedocs.io/en/stable/reference/PixelAccess.html


## About the Parameters in Deep Learning Method- 
1. `YAML` - This contains a plethors of models pre-trained on the `COCO` dataset - https://cocodataset.org/#home
- To know more about these models and their metrics - https://github.com/facebookresearch/detectron2/blob/main/MODEL_ZOO.md
- TLDR - We have included both instance and panoptic segmentation

## About the Parameters in Classical CV Approach- 
1. `Blur` - This provides the kernel size of the gaussian blur that you want to use in order to *smoothen* out the prediction mask.
2. `Erode Iter` - This is used as a morphological transformation method, in order to *sharpen* out the mask acquired.
3. `Dilate Iter` - This is used as a morphological transformation method, in order to *expand* out the mask acquired.
4. `Min Area` and `Max Area` - As per the edges detected, it is used to specify the minimum area and the maximum area of the them, so as to transform them into contours after filling them.


## ```Flask_BG_Remove.ipynb```

This Notebook has been created for removing backgrounds using a Flask Web App, where this notebook acts as a back-end.

METHOD - Detectron2 (Facebook)
MODEL USED - mask_rcnn_X_101_32x8d_FPN_3x

## Instructions for using `Flask Deployment` based solution - 

1. Switch to a GPU Runtime offered by Google Colab (Runtime-> Change Runtime Type -> GPU )
2. Install the libraries by running the `Install (Run Once) (USE GPU RUNTIME)` Tab
3. Restart the runtime **manually** (it is required, yes.)
4. Expand the `Import Libraries and Upload Images` Tab
5. Run the code till the end. 
6. In the second last cell, you can see something like this 
`` * Running on http://2b55-35-223-110-102.ngrok.io``, the URL can be different slightly, but open it as this is where the Web App has been deployed.
7. In order to do more iterations of the images, you have to close the web-app, and stop the running cell, and run the last cell, then proceed to running the webapp again.


## Tech Stack Used
<img src="https://cdn.worldvectorlogo.com/logos/python-5.svg" alt="Python Logo" height="100"/> <img src="https://upload.wikimedia.org/wikipedia/commons/9/96/Pytorch_logo.png" alt="PyTorch Logo" height="100"/> <img src="http://cms.ipressroom.com.s3.amazonaws.com/219/files/20149/NVIDIA_CUDA_V_2C_r.jpg" alt="CUDA Logo" height="100"/> <img src="https://raw.githubusercontent.com/valohai/ml-logos/master/numpy-simple.svg" alt="Numpy" height="100"/> <img src="https://upload.wikimedia.org/wikipedia/commons/5/53/OpenCV_Logo_with_text.png" alt="OpenCV" height="100"/> <img src="https://cdn.icon-icons.com/icons2/2699/PNG/512/pocoo_flask_logo_icon_168045.png" alt="Flask" height="100"/>




## TO-DO
- Choice for the user to provide color/background (FIX ERRORS) (FLASK)
- Clear the output image. (FLASK)
- A loop of retraining and fine-tuning the model is under-development.
- A Script to do the detectron task on CPU and use it in real time background replacement, is under-development.
- A YOLO and a GrabCut based approach is also under-development.
- A code to retrain DeepLab model on the MS COCO Dataset, which provides excellent results, is also under-development. 
