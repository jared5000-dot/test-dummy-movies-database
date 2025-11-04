# mock up movies database
A full stack CRUD enabled mock up website that allows users to add movies or TV shows to the catalog.  

## Website features:
+ Full CRUD Operations: Create, Read, Edit, and Delete any movie or TV show in your personal database.
+ Web-Based Interface: Easy-to-use frontend accessible from any modern browser.
+ Customizable Collection: Add titles, descriptions, links, and poster images to build your catalog.
+ Featured Content: Mark items as "featured" to highlight them on the home page.
+ Saving: Saves all content added even after closing browser.


## Tech Stack:
+ frameworks : Express
+ template :  EJS = Express JS
+ language :  Javascript
+ database :  mongo DB





## Prerequisites:
Before you begin, ensure you have the following installed/downloaded on your machine: 
+ Node.js
+ VSC (Visual Studio Code) 
Express should already be installed for you in the code.


## Set up instructions and execution:

1.
### Mongo DB
  a. Create MongoDB account:
Create a free Mongo DB account. A free one will do. You can visit: https://www.mongodb.com . Hit the get "Started Button" to sign up.



 d. Create a Cluster:
  Get to the "deploy your cluster" screen and:
+ Select free.
+ Name should be Cluster0 (the default). 
+ Leave "Tag" blank. 
  
Then click Create Deployment.

  e. Create a Database:

Now it will take you to a window that says Connect to Cluster0
+ Create a username and password
+ Then click "Create Database User", but "Choose a connection method" should work too. 

potential issues: If the button that says choose a connection method is still there in the bottom right corner then click it again.

  f.Drivers:
Select "Drivers" as your connection method (ussually the top most option).

  g.Get Your Connection String:
+ Select Node.js option for Driver.
+ Select Version 6.7 or later. 
+ Copy the connection string they provide. If the connection string has  <db_password> replace it with your cluster password, likewise for the username. 
potential issues: If the user name and password from step e do not work, enter the password for your mongo DB instead.


2.
### Connect database to code
Download this zip file. Open it in VSC.
There is a file in there called .env. Open it and you will see a non '#' line (line 2) that says DATABASE_CONNECTION_STRING =
on the other end of that '=' you want to paste your connection string. Example: DATABASE_CONNECTION_STRING = mongodb+srv://name:passwordddd@cluster0.libnbgg.mongodb.net/superheroes?retryWrites=true&w=majority&appName=Cluster0

Optional: before running the program in terminal you can make your mongoDB cluster view easier by adding the collection name of your choice. Come up with a name or use my name "superheroes" and put it inbetween the these 2 characters in your connection string -> '/' and '?'. Example: mongodb+srv://myusername:mypassword@cluster0.xxxxx.mongodb.net/####?retryWrites=true&w=majority . Replace "####" with your collection name.  


3.
### Start server:
We want to open a new terminal in VSC, by going to the terminal option (top of screen) and hit new terminal window or: control + shift + ~

enter: 

npm run dev

NOTE: you may get a warning about not being able to open because the developer cannot be verified. You may have to hit cancel 2-3 times that is to be expected.

4.
### Access website on browser:
How do you open the website? after doing the above step open a browser of your choice and enter: http://localhost:3000/create-media in the URL bar.

NOTE: by default unless you used the example database connection string and uncommented line 1 by deleting the '#' key, you will not see any posters of super hero movies up right now. You must add them all from scratch. Before going to the next step. go see How to Use instructions.

5.
### Stopping Server:
To stop server without closing the window use the keys: 'control' + 'c' in terminal.
Closing the VSC window can also stop the server.



_____________________________________________________________________________________
## How to Use:
### Adding Media
Adding images to content: 

1. Navigate to the "Create Media" page.
2. Fill out the form with the title, description, etc.
3. Adding Images: To add a poster, find an image online (e.g., on Google Images), right-click it, and select "Copy Image Address". Paste this URL into the "Image URL" field in the form.
4. "Is Featured": Check this box if you want the item to appear on the home page.
5. Submit the form to add the item to your database.
6. Viewing your database: Now when you view your mongo DB collection it will be in "Clusters" on the left hand side bar, then click "Browse Collections".

### Featured content
+ is Featured check box determines if the movie or tv show will be visible on the home page.
+ You can view, edit, or delete any item from its respective page.


