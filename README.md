# background-remover
This Notebook has been created for removing backgrounds fron images, using primarily two methods


1.   Deep Learning (Facebook's Detectron2 Pre-Trained Models)
2.   Classical Computer Vision (Experimental)

## Instructions for Use `Deep Learning` based solution - 

### PLEASE OPEN THE NOTEBOOK IN GOOGLE COLAB

1. Switch to a GPU Runtime offered by Google Colab (Runtime-> Change Runtime Type -> GPU )
2. Install the libraries by running the `Install (Run Once) (USE GPU RUNTIME)` Tab
3. The runtime **WILL Crash**, let it ,as it is required to restart the runtime.
4. Expand the `Import Libraries and Upload Images` Tab
5. Upload the foreground and background images as prompted by the cell which is running, and let it upload.
6. Expand the `Approach 1 - Detectron2` Tab
7. Expand the `Input Area - Play with these parameters`, and edit the parameters accordingly. For a good baseline to start working with tick the `USE_DEFAULT` check-box and run the cell.
8. Run all the cells within the `Functions` Tab, no need to open.
9. Expand the Display and run all cells. Enjoy the output.

## Instructions for Use `Classical CV` based solution - 
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

## Tech Stack Used
<img src="https://cdn.worldvectorlogo.com/logos/python-5.svg" alt="Python Logo" height="100"/> <img src="https://camo.githubusercontent.com/c04e16c05de80dadbdc990884672fc941fdcbbfbb02b31dd48c248d010861426/68747470733a2f2f7777772e74656e736f72666c6f772e6f72672f696d616765732f74665f6c6f676f5f736f6369616c2e706e67" alt="TF Logo" height="100"/> <img src="http://cms.ipressroom.com.s3.amazonaws.com/219/files/20149/NVIDIA_CUDA_V_2C_r.jpg" alt="CUDA Logo" height="100"/> <img src="https://raw.githubusercontent.com/valohai/ml-logos/master/numpy-simple.svg" alt="Numpy" height="100"/> <img src="https://upload.wikimedia.org/wikipedia/commons/5/53/OpenCV_Logo_with_text.png" alt="OpenCV" height="100"/> 
