# GIF Video Face Replacement

# About
For this project, we wanted to present our take on Snapchat's face filters. 
On social media platforms such as Snapchat, there are a variety of popular filters that users use on a daily basis. One of the most popular kinds of filters involve the pasting of a detected face onto dancing mascots. For the CS445 final project, we wanted to present our take on these face filters. The focus of this project is to understand how Snapchat engineers create such filters and gain the skills to create a unique filter.

# Contents
frames:
 - This folder was created to contain the output of cell 9. This was created to test the *video2imageFolder* function in utils.py.

samples:
 - This folder is used to store your input images and videos.

results:
 - This folder is the location of processed output video.
   
Final_project.ipynb
 - The main project file. Run this code to generate the output video.
   
utils.py
 - Python file containing helper functions from previous CS445 MPs.
   
haarcascade_frontalface_default.xml
 - Frontal face detection xml file.
   
**shape_predictor_68_face_landmarks.dat**
 - Face landmark detection data file. Download it here: https://github.com/italojs/facial-landmarks-recognition/blob/master/shape_predictor_68_face_landmarks.dat
 - Place this file in the same folder as haarcascade_frontalface_default.xml.

# Instructions
To build the project, be sure to download the following software and packages:
 - Python 3
 - Jupyter Lab/Notebook
 - cv2
 - ffmpeg
 - numpy
 - matplotlib
 - dlib

Once you open the project file, be sure to change the file path in cell 3 to the location of your downloaded repository.
<img width="544" alt="Screen Shot 2023-12-06 at 9 00 01 PM" src="https://github.com/phan603/CS445-final-project/assets/87063643/3f1eed54-448f-4efc-891d-c07cd8a0fd9b">

After this is done, you may run cells 1 through 7. In the 8th cell, this is where you will input your desired input images and .mp4 files for processing. 
<img width="983" alt="Screen Shot 2023-12-06 at 9 06 12 PM" src="https://github.com/phan603/CS445-final-project/assets/87063643/6017b52e-455d-42ee-a11b-fba223e39591">

Be sure to change the file path for the variables *cap* and *output_video_path*. In order to change your input video and image, you need to edit the filenames in the variables *face_image* and *cap*. As seen in the image above, the input image *face.png* and input video *snapchat.mp4* are currently loaded. Once you have changed these parameters, run the cell to generate your processed video. The output of this cell will be located in the samples folder in your computer's repository directory.

If you decide to use a video other than *snapchat.mp4*, then make sure to comment out this code:

top_quarter_height = filter_frame.shape[0] // 4 

if filter_face_bbox[1] + filter_face_bbox[3] // 2 > top_quarter_height:

continue  # Skip this frame if the face is not in the top quarter
