# mock up movies database
A full stack CRUD enabled mock up website that allows users to add movies or TV shows to the catalog. Both backend and front end. 

## Webstie features:
+ Full CRUD Operations: Create, Read, Edit, and Delete any movie or TV show in your personal database.
+ Web-Based Interface: Easy-to-use frontend accessible from any modern browser.
+ Customizable Collection: Add titles, descriptions, links, and poster images to build your catalog.
+ Featured Content: Mark items as "featured" to highlight them on the home page.
+ Saving: Saves all content added even after closing browser.


## Tech Stack:
+ frameworks: Express
+ template :  EJS = Express JS
+ language :  Javascript
+ database :  mongo DB



instructions on how to get started:
type this into the url
http://localhost:3000/create-media

## Prerequisites set up:
1. 
### Node.js and VSC 
Before you begin, ensure you have the following installed on your machine:
download Node.js and Visual Studio Code or VSC. 
express should already be installed for you in this code so dont worry about that.

2.
### Mongo DB
Create a Mongo DB account. A free one will be all you need instructions on how to proceed the free way are as follows below.
instructions on Mongo DB:
  a. Create MongoDB account:
Create a free Mongo DB account. You can visit: https://www.mongodb.com . Hit the get "Started Button".

  b.Skipping personalization questions:
After this it may ask for a multi factor authentication method. We dont care about this, i chose email , just find a way to get passed this step.
Optional: You can skip any optional personalization questions.

  c. Stuck?:
if you are taken to a screen that says "deploy your clustor" congrats! you have made it to the correct screen skip to step d. 
If not hit the 9 dot grid in the top right corner. Then select Atlas. Then select Clusters on the left hand bar under DATABASE(may be a drop down arrow).
If you are still not at step d. then just click anything that says create cluster or create new cluster.

  d. Create a Cluster:
Select free. 
Name should be Cluster0 (the default). 
Leave "Tag" blank. 
Then click Create Deployment.

  e. Create a Database:
Now it will take you to a window that says Connect to Cluster0
Create a username and password
Remeber the password and username here and hit "Create Database User", but "Choose a connection method" should work too. We just want to get to that circle 2 step.
Optional: You can change the password and username to whatever you like. This will be the username and password for your cluster.
potential issues: If the button that says choose a connection method is still there in the bottom right corner then click it again.

  f.Drivers:
Select "Drivers" as your connection method (ussually the top most option).

  g.Get Your Connection String:
driver option should have Node.js selected. Version 6.7 or later. 
Choose Node.js and version 6.7 or later.
Copy and paste the connection string they provide. IF it has <db_password> or <password> that means you need to replace those characters with the password in step e. Do the same for user name if not done already. 
potential issues: If the user name and password from step e do not work, enter the password for your mongo DB instead.
Just put this Connection String somewhere safe we will need it later.

3.
### .env
Download this zip file.
There is a file here called .env. Open it in VSC and you will see a non # line (line 2) that says DATABASE_CONNECTION_STRING =
on the other end of that '=' you want to paste your connection string. Example: DATABASE_CONNECTION_STRING = mongodb+srv://name:passwordddd@cluster0.libnbgg.mongodb.net/superheroes?retryWrites=true&w=majority&appName=Cluster0
Optional: before running the program in terminal you can make your mongoDB cluster view easier by adding the collection name of your choice. Come up with a name or use my name "superheroes" and put it inbetween the these 2 characters in your connection string -> '/' and '?'. Example: mongodb+srv://myusername:mypassword@cluster0.xxxxx.mongodb.net/####?retryWrites=true&w=majority . Replace "####" with your collection name.  
Viewing your database: Now when you view your mongo DB collection it will be Clusters left hand side bar, browse collection.

4.
### start server:
Now that we've done the pre steps we can begin running.
open this file in  vistual studio code or VSC.
We want to open a new terminal in VSC so go to the terminal option (top of screen) and hit new terminal window or: control + shift + '
enter: 
npm run dev
if that does not work type node server.js and it MAY work, but npm run dev should always work.
NOTE: you may get a warning about not being able to open because the developer cannot be verified. You may have to hit cancel 2-3 times that is to be expected.

5.
### access website on browser:
How do you open the website? after doing the above step open a browser of your choice and enter: http://localhost:3000/create-media in the URL bar
NOTE: by default unless you used the example database connection string and uncommented line 1 by deleting the '#' key, you will not see any posters of super hero movies up right now. You must add them all from scratch. Before going to step 6. go see How to Use instructions.

5.
### Stopping Server:
To stop server without closing the window use the keys: 'control' + 'c' in terminal
Closing the VSC window can also stop the server.

## How to Use:
### Adding Media
adding images to content: 
I understand adding images is a little different than you are probably used to. 
To add a poster, find an image online (e.g., on Google Images), right-click it, and select "Copy Image Address". Paste this URL into the "Image URL" field in the form..
An example of what you will be copying and pasting will look like this: https://cdn.europosters.eu/image/1300/133030.jpg 

### Featured content
"Is Featured": Check this box if you want the item to appear on the home page.
is Featured determines if the movie or tv show will be visible on the home menu.


