# How to Learn Computer Vision
This is a collection of materials I used to start learning and using computer vision for my internship.

Before going through the resources, I'd like to note that you’ll find that computer vision and artificial intelligence has a lot of painful, fun math behind it. Fortunately, the libraries abstract this math into easy-to-use functions. If you're focused on the application aspect of computer vision as I was, it could save you time to just have an overview of what tools you have at your disposal instead of worrying about learning about the math of each and every function you use (as I was). 

A simplified version of the path I used to learn computer vision started off with learning:
- **traditional image processing with [OpenCV](https://github.com/SeanKenRuiz/how-to-learn-computer-vision/blob/main/README.md#OpenCV)**,
- then **neural networks with [PyTorch](https://github.com/SeanKenRuiz/how-to-learn-computer-vision/blob/main/README.md#pytorch)**,
- and finally **[YOLOv8](https://github.com/SeanKenRuiz/how-to-learn-computer-vision/blob/main/README.md#YOLOv8) (You Only Look Once version 8) computer vision model and framework**.
![Learning Computer Vision Tools](https://github.com/user-attachments/assets/b73e8a0f-2019-43a9-a3be-2d7f008966fe)

## Traditional Image Processing
Before I started using OpenCV, I started going through Shree Nayar's course on the "First Principles of Computer Vision" as it is very theory heavy. It covers a large portion of computer vision so I had to end up skimming the course. However, do not let yourself get stuck here and move onto OpenCV as soon as you can. 
| Course | Description |
| --- | --- |
| "First Principles of Computer Vision" | [Website](https://fpcv.cs.columbia.edu/) (the one I used) <br> [Coursera](https://www.coursera.org/specializations/firstprinciplesofcomputervision?utm_medium=sem&utm_source=gg&utm_campaign=B2C_NAMER__coursera_FTCOF_courseraplus_pmax-namer-npls-and-search-themes-country-US-country-CA&campaignid=21019068954&adgroupid=6490842751&device=c&keyword=&matchtype=&network=x&devicemodel=&adposition=&creativeid=6490842751&hide_mobile_promo&gad_source=1&gclid=Cj0KCQiAire5BhCNARIsAM53K1hYO0ofRQ7X_OlYZd8BuB4QcSi7TEI7Q6-NHg7Tn4CNJbCtcSe3jQoaAghuEALw_wcB) <br> [YouTube](https://www.youtube.com/channel/UCf0WB91t8Ky6AuYcQV0CcLw)|

### OpenCV
OpenCV gives you a good amount of tools for traditional image processing. 

Just a warning that once you get to neural networks, a bulk of traditional image processing techniques will not need to be used again as the only part from the OpenCV library I used in the internship project was to capture and display the video feed from my camera, and a line drawing function. **However** it is very good to understand them as a foundation. 

For **learning**, I straight up used the [OpenCV-Python Tutorials](https://docs.opencv.org/4.x/d6/d00/tutorial_py_root.html) however there are other resources available such as this [**tutorial video series by Tech With Tim**](https://www.youtube.com/watch?v=wlYPhdTbRmk&list=PLzMcBGfZo4-lUA8uGjeXhBUUzPYc6vZRn&index=2&ab_channel=TechWithTim) which lets you know about errors you will potentially run into. Another good resource is from the original documentation is the [GeeksForGeeks OpenCV Tutorial](https://www.geeksforgeeks.org/opencv-python-tutorial/). These none resources may not resonate with your learning style so I highly recommend to look at other resources online. 

Before going into PyTorch, make sure you:
- know the data type of an image from OpenCV,
- capture and save your video with OpenCV,
- draw or apply a transformation to an image,
- used traditional object detection with a variety of methods
- have at least skimmed through the entirety of OpenCV-Python Tutorials
- have looked online for potentially better resources (computer vision tutorials, OpenCV tutorials, etc)

## Image Classification with Neural Networks
### PyTorch
[PyTorch](https://en.wikipedia.org/wiki/PyTorch) is a popular machine learning library known for its ease of use. The building block of PyTorch is the tensor (a fancy array that you can send to your GPU for the faster processing needed for neural networks). You'll usually have to convert Python arrays or the images from OpenCV (numpy arrays) to tensor form.

To learn PyTorch, I used [Zero to Mastery | Learn PyTorch for Deep Learning](https://www.learnpytorch.io/00_pytorch_fundamentals/) and ["Learn PyTorch for deep learning in a day. Literally." video series by Daniel Bourke](https://www.youtube.com/watch?v=Z_ikDlimN6A&t=50417s) that goes alongside the website format. I highly recommend the video format as I switched to it for clarity and following along the tutorial in a Google Colab notebook. In my Learning-OpenCV-and-PyTorch repository, you can see I did it in a normal file on Visual Studio Code, which was not very efficient for learning purposes.

I personally stopped at chapter 6 of the course as I've gained knowledge of how to use PyTorch's tensor, the general model architecture of a neural network, how to train a neural network, and how normal neural networks differ from convolutional neural networks.

Again I recommend to look for other resoures on your own, but here's some other resources I used to help me understand neural networks.

Additional resources:
- [Stanford Computer Vision Lectures Youtube playlist](https://www.youtube.com/watch?v=vT1JzLTH4G4&list=PLf7L7Kg8_FNxHATtLwDceyh72QQL9pvpQ&index=1&ab_channel=StanfordUniversitySchoolofEngineering)
- [Neural Networks / Deep Learning" YouTube playlist by StatQuest](https://youtube.com/playlist?list=PLblh5JKOoLUIxGDQs4LFFD--41Vzf-ME1&si=DyyrWTpcXlsY8_Uz) 

## Transfer Learning with the YOLO object detection model
### YOLO
The [YOLO (You Only Look Once) models](https://docs.ultralytics.com/) are currently some of the best neural network models for real-time object detection at the moment. It is also a framework of tools made by Ultralytics that has made it very easy to use a deep-learning based computer vision model with [less than 20 lines of code](https://docs.ultralytics.com/modes/track/#tracker-selection:~:text=Python%20Examples-,Persisting%20Tracks%20Loop,-Here%20is%20a). Once you get to it, [https://docs.ultralytics.com/modes/](https://docs.ultralytics.com/modes/), [https://docs.ultralytics.com/tasks/](https://docs.ultralytics.com/tasks/) and [https://docs.ultralytics.com/guides/](https://docs.ultralytics.com/guides/) are your best friends. Tutorials from the Ultralytics Youtube channel such as ["Object Detection with Pre-trained Ultralytics YOLOv8 Model | Episode 1"](https://www.youtube.com/watch?v=5ku7npMrW40&ab_channel=Ultralytics) are also decent.

Again, don't pidgeonhole yourself with using just these materials. Learning using these materials is what helped me and you can find a bunch of other resources on Google, Reddit, Github (like the [awesome computer vision repo](https://github.com/jbhuang0604/awesome-computer-vision?tab=readme-ov)), etc.
Additionally, familarize yourself with finding research papers (using Google Scholar or your college's research database) and reading them.
