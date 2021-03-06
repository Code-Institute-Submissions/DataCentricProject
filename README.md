# Data Centric Development Milestone Project

The project is focused on the use of databases and the use of python and flask to put it all together.

My cooking book concept is a space where users can check, create or edit their own recipes, with a simple, yet balanced
design. The user experience is clean and the navigation through pages creates a space where you can come and go as you please,
never limiting the user.

This project generated various challenges when using the different syntax for the Mongo terminal and pymongo. The 
conceptualization of the project was simple but creating the logic in python based in mongo and applied to flask was
the biggest challenge. Trying to create a web site which responds to the user in the most basic manner and keep 
the standards for an acceptable web site took time but was rewarding.

This project delivers by using the mongo database, which is flexible and intuitive. 

** All information and pictures are fictional, non related and just for testing **

## Application guidelines
  - [x] MongoDB to hold a database based on cooking recipes
  - [x] User is presented to a web page inviting to see create or edit recipes
  - [x] User can create, edit and delete recipes created by him/her
  - [x] User has a simple verification method to access his/her own recipes
  - [x] The page flow is intuitive and lets the user navigate to any place at any moment
  - [x] The web development has sections which allow for the distribution of information
  - [x] A graph updates and shows users the amount of authors and recipes in the site

## Project guidelines
  - [x] Logic written in python. other technologies used
  - [x] Semantic HTML
  - [x] The website must be data-driven (MongoDB)
  - [x] Use Flask, a micro-framework, to run your application
  - [x] Instructions to deploy (see deployment)
  - [x] Share details of how you created your database schema in your README.
  - [x] Make sure the site is responsive
  - [x] User stories, wireframes
  - [x] CSS and Bootstrap frameworks used
  - [x] README.md file made
  - [x] GitHub version control used during development https://github.com/CEsarABC/DataCentricProject
  - [x] Final version of the code deployed in Heroku



## Technologies used

- HTML
- CSS
- Bootstrap 4.0
- Python 3.6
    - PyMongo
- JavaScript
- Charts.js
- Flask
- Cloud9
- mLab MongoDB
- Adobe Illustrator
- Abobe Photoshop


## Basic project tree

  - cooking-recipes
      - static
        - css
        - images
        - js
      - templates
      - Wireframes https://github.com/CEsarABC/DataCentricProject/tree/master/wireframes


  - app.py **(main application)**
 

## UX
- This development presents the content to the users and let them chose what path they want to take.
- The information is simple and in a clean manner
- The introduction invites the users to interact and find what they are looking for.
- Images are compresed and light so the user doesn't experience delays 


## Features
- User can navegate in any section of the site 
- User can see all recipes in the database
- User can search by author name, cuisine or search by filtering an allergen
- User is able to add recipes, important fields are required in the form
- User validation for editing or deleting recipes
- User is able to retrieve all his/her recipes for edition or deletion
- User can see how many recipes all users have
- Forms are not case sensitive to avoid problems trying to access any data

### Left to Implement
Bringing this project to life took some time and some ideas where left on the side just because of the time left to finish my course.
- [ ] A better and more complete search section
- [ ] Giving the user option to upload their own pictures
- [ ] Adding more grahps to display more information on the database
- [ ] More visually appealing design 
- [ ] Pagination for extensive results
- [ ] Limit to the amount of results in the graph
- [ ] Code auto format for ingredients and method sections

## Database Schema
I decided that mongoDB was the best database I could use in my project. I needed flexibility
and my data was not extensive enought for me to create a relational database to extract information.
My collections were then divided between the document, which was going to hold all the information about
the recipe, and the options such as cuisine type. Choices in cuisine was supported by having its own document with 
data avaliable for the user, when creating or editing recipes.

The Database structure:
- recipes database
  - collection of recipes
  - collection of cuisines
  
The schema used for the main document:
- `'author': name   `                 (used for verification)   
- `'dob': dob    `                    (used for verification)
- `'recipe_name': nrecipe  `          (new document)
- `'description': description `       (information)
- `'cuisine': cuisine `               (information)
- `'serves': serves `                 (information)
- `'time': ctime   `                  (information)
- `'ingredients': ingredients `       (information)
- `'method': method `                 (information)
- `'views': 0`                        (views count and record)
- `"images_small": "/dishes0.jpg"`    (image link for card)
- `"images_large": "/dishesL0.jpg"`   (image link for recipe page)
- `'allergens': arrayValues  `        (array created with the selected allergens)



## Testing

- Mostly manual testing, all modules in the python application where developed
individually and the assembled into the full application
- Modules tested:
- [x] reading from database
- [x] queries from database
- [x] use of flask to bring data to html documents
- [x] inserting and modifing from database
- [x] use of python to extract data from database
- [x] use of python to create basic javascript documents 
- [x] passing data from database to charts 

- Tests have been made for media queries in different formats from pc to mobile
- Heroku deployement tested



## Deployment
- Project fully deployed to Heroku  https://cooking-book-cb.herokuapp.com/
  - The project was deployed following the guidelines from the code Institute materials
  - New project was created in Heroku
  - requirements.txt was created by the use of `pip3 freeze`
  - Procfile was created
  - Heroku remote was set in order to push application
  - Configuration variables were changed as indicated to have `'IP' = (0.0.0.0) and 'PORT' = (5000)`
  - To access the recipes for edition you can use and test your own recipes or just use:
    - ==author: Cesar DOB: 24/02/87==
    - ==author: Oscar DOB: 24/02/88==
  - In search by cuisine `italian`, `british` and `japanese` have some recipes


- pip3 used to install pymongo

- Requirements.txt
    - Click==7.0
    - Flask==1.0.2
    - Flask-PyMongo==2.2.0
    - Jinja2==2.10
    - MarkupSafe==1.1.0
    - Werkzeug==0.14.1
    - itsdangerous==1.1.0
    - pymongo==3.7.2


**Running locally - in the terminal**
- To run this application in cloud9 `$ python3 app.py`


## Credits

- This module was complemented through a couple of courses from **Udemy**
  - MongoDB - The Complete Developer's Guide
  - Python and Flask bootcamp
- https://docs.mongodb.com/
- Small blocks of code taken from boostrap 4.0 web page 
- Recipe texts taken from https://www.jamieoliver.com
- Recipe texts taken from https://realfood.tesco.com/recipes/

## Media
- Fonts taken from google fonts
- Images taken from https://unsplash.com/search/photos/food
- Charts from https://www.chartjs.org/
- Images taken from https://www.freepik.com/free-photos-vectors/food

## Acknowledgments
Thank you to the code institute for the support. This last project has been challenging and took me some time to develop. 
I have learned a lot and I hope to keep learning to become the professional I want to be.
Thank you to the slack channels for the support and the code academy tutors which always had answers to help me move forward.



