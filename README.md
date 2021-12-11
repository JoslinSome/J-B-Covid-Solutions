# team17_swd

### Problem Statement
We at J&B Covid Solutions Have opted to find a way to make vaccination checking accessible and easy for everyone. Due to the immediate need of such  product we have dedicated many hours of our precious weekend to develop the best possible application. 
### Important
Our App uses a login system that considers 3 types of individuals,  Users, Organizations and Admins. Users and Organizations can be created by anyone using the app but, Admin accounts are directly created by us for security reasons. For your convenience, please use the credentials (without the quotes):
**Username: 'Swd' , Password: 'abcd'** in order to login as an admin.
Our app functions under the assumption that only we, will be able to make direct changes to the database **Please do not directly add or delete anything from the database**, use the UI for all necessary actions.

### Technology used
Our app runs using JavaFx as a GUI Framework paired with CSS styling. We use SQL databases for information storage and the Google distance Matrix Api for location pinpointing. We also use the SHA-512 algorithm for password hashing

### App Idea rundown

In order to be able to easily check people's vaccination status, we consider ourselves (J&B Covid Solutions) to be a top Health organization. 

When a user signs up, his vaccination status is set as False, he can view all signed up companies in a list along with all their policies. We also used the google Distance Matrix Api to determine the distance from the company to the user. Ideally when going into a store or restaurant, the user could check the organizations policies beforehand.  In order to prove their vaccination, the user would have to personally come into a J&B clinic where one of our employees with Admin access would set their vaccination status to true after verifying that they really are vaccinated. After this the users account would show the word "Vaccinated" on it and he could easily prove it to any organization just by showing the status on his phone. Since only an Admin can change vaccination values there is no risk of the user lying about their status.

**Log in/sign up  -scheme for identification of users (individuals, organizations, other 
possible account types)**

![Home Screen](https://github.com/JoslinSome/test1/blob/main/ezgif.com-gif-maker%20(3).gif?raw=true)

### User Documentation and requirement Fufillement

There are 3 user roles in this app. You can log in as either a User, an Organization or an Admin. 2 of these roles can be accessed by anyone just by creating an account at login
**Please note that we have a back button on the top left of most screens to undo previous actions**
![Sign up](https://github.com/JoslinSome/test1/blob/main/Screen_Shot_2021-12-06_at_2.44.33_AM_1_35.png?raw=true)

**-Organization interface for organizations to create their own public profile which includes their COVID 19 guidelines requirement**

On organization can create an account using the sign up button and following the required steps. After adding a logo image and  clicking sign up the page will automatically close and you will have to reopen the app with the login button.
Once logged in, an organization can add their mask regulation policies that will be directly viewable by the Users. We currently only have one organization set up which you can view with the login: **Username: 'Wendys1' Password: '1234'**
but feel free to add more by signing some up! For your convenience, we have added company logo's to the TestLogos folder

![Organization example](https://github.com/JoslinSome/test1/blob/main/Screen_Shot_2021-12-06_at_2.53.35_AM_35.png?raw=true)


**-User, Mobile interface for individuals to update and validate their vaccination records 
 Requirement:**

When a user logs in, he can see his current Vaccination status along with a list of all
the logged in Organizations you can search through this list for a particular Organization. Double tapping on an organization will take you to a page showing that organization's policies along with your distance from them. you can use the credentials **Username: 'Joslin12' Password: '1234'** to log in as a user or feel free to make your own account.

![User page](https://github.com/JoslinSome/test1/blob/main/Screen_Shot_2021-12-06_at_3.09.13_AM_35.png?raw=true)

**-Admin**
The administrator profile is created directly by a J&B executive and cannot be made by using the App. from the admin login you can view all current users and set their vaccination status to true, and Organazations. You can search through the tables at your leasure .Please use the credentials (without the quotes):
**Username: 'Swd' , Password: 'abcd'** in order to login as an admin.
![Admin](https://github.com/JoslinSome/test1/blob/main/ezgif.com-gif-maker%20(5).gif?raw=true)

**Security mesures:**

Our app uses SHA-12 hashing to store passwords securely into the database
![Table](https://github.com/JoslinSome/test1/blob/main/Screen_Shot_2021-12-06_at_3.50.44_AM_1_50.png?raw=true)

### Potential errors to fix 

Due to lack of time our app is not perfect! Notably, We struggled with image uploads and downloads to the database. When you add an image, that picture is sent to the database and immediately downloaded to the resources/image folder. Meaning if you were to add a an organization with an image name on one computer and you then ran the code on another without Committing the resources/image folder to git, the second user would be unable to access that organization in the database and the app would crash if they tried. 
We also added a field for User images but never had the time to add that image to the user screen.
Another bug we did not have time to fix is that our app assumes that no changes will be manually made to the database. If all the info from any table were suddenly deleted you would be unable to login or sign up anymore without manually inputting a row into the Table.
We also noticed that SQL has some difficulteis dealing with certain special charachters like '/"  
We blocked input of these characters for usernames and passwords but did not quite have time to figure out how to allow their use for Company regulation input


### Developer Documentation

Our program had many classes, the general uses were:

**API** This class controls the google API logic

**Database** This class contains all used database queries

**Hasher**. This class controlled the password hashing

**Driver**. This class runs the application

We also had various controller classes for each of the GUI pages

For more information please refer to the [Java docs](http://localhost:63343/team17_swd/docs/allclasses-index.html?_ijt=23i4fv80vpreovrjkbv66u2uci)

## UML Diagram
![UML Diagram](https://class-git.engineering.uiowa.edu/swd2021fall/team17_swd/-/raw/main/FinalProject/OrganizationScreenController.png)

## Source Code

[Click here for Source code](https://class-git.engineering.uiowa.edu/swd2021fall/team17_swd/-/tree/main/FinalProject/src)
