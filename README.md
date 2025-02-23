# Project_310
#### HappieEE group project ####
$$
\{ \forall x \in \mathbf{Z} \vert \left( \frac{\frac{d}{dx}\frac{\int_{x^\sqrt{x}}^{3x^e}(3e^{2sin(x)})dx}{e^{\sqrt{sin(\int_0^{\sqrt{\pi}}(30+6x^2)dx)}}}\begin{bmatrix}
x & 3\pi & 8x\\
cos(x) & 3\sqrt{e} & x^6x\\
\sqrt{x} & 8 & 18\\
\end{bmatrix}\cdot \vec p }{x^t\cdot \frac{d}{dt}(5^t)\cdot(\int^{8x}_{90x+90x^2}(t^e)dt)}\right)>0 \}
$$

## //What is the project about? ###
The purpose of our app, “happieEE”, is to determine if someone is happy or not.happieEE is a social media platform 
that has a feed and can detect the emotions in a user’s posts.

It's main features are:
  * Account and Security system, protect against common attacks like SQL Injection, XSS, CSRF, etc)
  * Happiness Facial Detection (ML)
  * Bar (Showing the info)
  * Filter 
  * Comment 
  * Feed (You can post results and share to everyone)


## How to compile and run the code?
### Back End
```bash
cd Back_End
nohup bash run.sh & # Run the main program
nohup node index.js > status.log & # Run the crash detector
```

### Front End

Run:
```bash
npm install -g @ionic/cli
cd Front_End
ionic serve
```

Compile to Production 
```bash
npm install -g @ionic/cli
cd Front_End
ionic build # Compile
gh-pages -d build  # Deploy to GitHub Pages
```
## Class Organization
- Using MySQL the data is seperated into a class for each table which contain's users data as objects
  this is located in the Backend folder in the file models.py
- Using Fast api the api functions for the application are located in the main.py file of the backend folder
- Using a Ionic + React framework the frontend code for the home feed is located in /Front_End/src/pages/Home.tsx.

### Frontend
Components:
 - Card
  - Each post on the global feed is a Card and this component allows us to easily add new posts  
 - ExploreContainer
  - This is where we prepare data to be shown in the Card component. We fetch data from our API on this component and pass it onto the Card component
 - Popup
  - This component sends a popup to the user showing information passed into the component
 - Question Card
  - A Card showing a OChem question and answer choices
  
Pages:
 - Home
  - The Home page is the landing page that the users will first see when they go on the app. This is also where the global feed is to see user posts
 - Login
  - This is the login page where users can login or sign up a new account, with a forgot password option. 

Themes:
 - To prevent redundant code, we have a class where we have all our themes (i.e. colours) that we can easily access from other classes

### Backend
the documentation for the backend is located in HappieEE123/Project_310/FastAPI-docmentation UI.html


## Tech Stack
- Front End: Ionic + React
- Backend: Python Fast API, Node.js for crash detector, bash for logging.
- ML: TensorFlow was used to built the model, numpy and Pillow was used to process the data
- Database: MySQL.

## What has Changed since project 1
## a list of each feature you programmed for this assignment
- for each item on that list, explain briefly how you used that feature to improve your
system
- for each explanation, give a snippet of the output that demonstrates your feature
1. Login - using React Router, React, and React Dom Libraries to have a separate url for login page (6 points for libraries +1 point for feature)
- The login page is connected to the rest of the app and grants access to the feed upon login, and is connected to the signup page for new users. 
![Login](https://github.com/HappieEE123/Project_310/blob/2db917711289f4691fd00371237c6f28f411eff6/imgs/image%202.PNG) 
2. Signup - using React Router, React, and React Dom Libraries to have a separate url for signup page  (1 point for signup)
- the signup page has been created to collect and store users information inorder to register them and grant them access to the app as authorized users. 
![Signup](https://github.com/HappieEE123/Project_310/blob/2db917711289f4691fd00371237c6f28f411eff6/imgs/image%203.PNG) 
3. Like Counts - Axios to get and update # of likes to and from the server (2+1 points)
- Likes count feature is enabled, which is tracked through a counter and displayed on individual posts. 
![Likes count before](https://github.com/HappieEE123/Project_310/blob/2db917711289f4691fd00371237c6f28f411eff6/imgs/image.jpg) 
![Likes count after](https://github.com/HappieEE123/Project_310/blob/2db917711289f4691fd00371237c6f28f411eff6/imgs/image%202.jpg)

## Changed Since Last Group Assignment
- Added a question card asking users a ochem question to make them sad if they are happy
- added a feature allowing user to send the question to its number
- added some animation after upload the image

![image](https://user-images.githubusercontent.com/41298844/206081606-459cf1c8-ed26-4fe5-a09f-0d4111cbcb9d.png)
![image](https://user-images.githubusercontent.com/41298844/206081622-29f1dd24-5541-4309-a929-92f1aa846e38.png)
![image](https://user-images.githubusercontent.com/41298844/206081629-4fb462aa-d618-4df6-b230-fbee39041529.png)

4. GUI
GUI for main components is complete.
![GUI](https://github.com/HappieEE123/Project_310/blob/2db917711289f4691fd00371237c6f28f411eff6/imgs/image%204.PNG) 




