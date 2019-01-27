# Glimpse

<p align="center">
<img src="https://github.com/The313/Glimpse/blob/master/Images/glimpsegif.gif" height="170">
</p>

## Motivation

Singapore has a large number of recreational spaces in every neighbourhood that are free for everyone to use. These spaces include basketball courts, badminton courts, street soccer courts, and even playgrounds. However, the want to use these public spaces can be hindered by the lack of knowledge as to whether the space is occupied at any given time. This problem has yet to been solved even till today. Our project aims at solving this problem in an effective and convenient way.


## Our Solution

Our solution includes adding a small camera that overlooks each space. This camera, with the help of computer vision, will help identify the total number people using the facility at every given period of time. This information is then sent to a central database. The data is pulled by a phone application which can then be accessed by everyone with that application installed. Only the numerical capacity will be displayed on the app and not the pictures taken as to provide as much information as possible while still maintaining privacy.


<p align="center">
<img src="https://github.com/The313/Glimpse/blob/master/Images/javaposter.jpg" height="550">
</p>


## Implementation

As a proof of concept, we will be applying our solution on a smaller scale within our school campus. 

We will be using a small web camera to monitor two pool tables. A LattePanda will be used to simulate a back-end to carry out the people detection scripts and to push the final data to a common database. The camera will take a photo of the tables every 30 seconds. Once the detection is done on these photos, the detected number of people as well as the date and time is pushed to firebase.

The app consists of two main components:
- HomePage
- Public Space Page

## Team
- Chia Si Wei
- Koe Jia-Yee
- Michael Junaprasetya
- Tan Wei Jin
- Vieri Vincent


---
### HomePage


This page is a tabbed activity, which consists of three tabs:
- Categories
- Available
- Favourites   

<br>


<p float="left" align="middle">
  <img src="https://github.com/The313/Glimpse/blob/master/Images/homepageUI.PNG" height="300" hspace="30"/>
  <img src="https://github.com/The313/Glimpse/blob/master/Images/availableUI.PNG" height="300" hspace="30"/> 
  <img src="https://github.com/The313/Glimpse/blob/master/Images/favouritesUI.PNG" height="300" hspace="30"/>
</p>






#### Categories

This tab sorts all listed public spaces based on the intended type of usage. Examples include basketball courts or badminton courts.


#### Available

This tab lists all public spaces that are not at maximum capacity to serve as an easy method of filtering out spaces that are full.



#### Favourites

This tab lists the public spaces that have been favourited by the user before.

---

### Public Space Page

There is a different public space page for every public space, and provides information about the specific space such as the current capacity, the opening hours, the address, and the booking link if relevant.



<img align="right" src="https://github.com/The313/Glimpse/blob/master/Images/swimmingpoolUI.PNG" height="300" hspace="30"/>




Current list of spaces:

* Indoor Sports Hall 1
* Indoor Sports Hall 2
* Swimming Pool
* Fitness Centre
* Rock Climbing Wall
* Street Soccer Court
* Building 57 Level 1 Pantry
* Building 59 Level 4 Meeting Room

<br>


---

### OpenCV

##### Running build on LattePanda:

1. Run cmd and cd to <b> "C:Users\LatttePanda" </b>
2. Run command ``` "venv\Scripts\activate" ```
3. Cd to <b> "C:\Users\LattePanda\Desktop\opencv" </b>
4. Run ``` cnn_detection.py ```


To change the location update of the camera, edit ``` ref = db.reference(location) ``` in cnn_detection.py



