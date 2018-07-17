# Face_recognition_OpenCV

In this repository helpful to understand some of the key part of the face recognition technique of Opencv.
Accracy of this program is 86%.
you can add and update the training data when you want at a time and train it and test it.


# How to use it

# simple steps i explain here below just perform it and you are successfully got the result
  # Steps to download environment
  # 1. you can download the opencv, numpy and pillow library of python
       ex : pip install [Library name] 
  # 2. downlaoad or clone the zip file from here 
       then after important step is that 
       1.go to your current working virtual environment where you are working now from there
        /lib/site-packages/cv2/data
        you can copy the whole folder  "data" and paste it in to the you current project(in this project)
       2.then change the file address in file "dataset.py" and "face_rec.py" in line 3
       face_detect=cv2.CascadeClassifier("this project address"/data/haarcascade_frontalface_default.xml")
       
       ex: this is look like this but in #your case its diffrent address of project 
        face_detect=cv2.CascadeClassifier('C:/Users/Bond/Desktop/faceRec/testFace/cascades/data/haarcascade_frontalface_default.xml')
        
  # 3. after that you can run the dataset file for updating the database
  # make dataset by below command
      1. python dataset.py
        ---> it will require the any integer value to respective user to identify
        and this file caputre the images 21 images of perticular user.
  # then train it using below command
      2. python trainner.py
      ---> it will train the data model and make the yml and generate the trainingData.yml for testing perpose
  # now its time to recognize of face
      3. python face_rec.py
      ---> this file will be responsible to detact face based on the training data 
      ---> if its find it the match data then it will print the user id on prompt and if not the it print "unknown"
