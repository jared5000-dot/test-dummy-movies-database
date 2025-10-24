# dummy-movies-database
A website mock up that allows users to CRED a movie or TV show. Both backend and front end. 
WHAT CAN THIS WEBSITE AND PROGRAM DO?
This is a web based tool for you to add movies and tv shows to share with your family and friends. You and edit any movie or show you add or delete it from the database entirly.

instructions on how to get started:
type this into the url
http://localhost:3000/create-media

1.
download node.js and visual studio code. 
express should already be installed for you in this code so dont worry about that.

2.
instructions on Mongo DB:
  a.
create Mongo DB account. 

  b.
After this it may ask for a multi factor authentication method. We dont care about this, i chose email , just find a way to get passed this step.
Afterwards it may ask for why you are using Mongo DB, you can answer these or hit skip personalization this is all optional.

  c.
if you are taken to a screen that says "deploy your clustor" congrats! you have made it to the correct screen skip to step d. 
If not hit the 9 dot grid in the top right corner. Then select Atlas. Then select Clusters on the left hand bar under DATABASE(may be a drop down arrow).
If you are still not at step d. then just click anything that says create cluster or create new cluster.

  d.
Select free. Name should be Cluster0 . Leave Tag blank. Then hit Create Deployment

  e. 
Now it will take you to a window that says Connect to Cluster0
The only thing on this page that is a must do is to remeber the password and username here and hit Create Database User , but Choose a connection method should work too. We just want to get to that circle 2 step.
Optional: You can change the password and username to whatever you like. This will be the username and password for you cluster.
If the button that says choose a connection method is still there in the bottom right corner then click it again.

  f.
For simplicity purposes hit "Drivers" (ussually the top most option)

  g.
driver option should have Node.js selected. Version 6.7 or later. Copy and paste the connection string they provide. IF it has <db_password> or <password> that means you need to replace those characters with the password in step e. Do the same for user name if not done already. If the user name and password from step e do not work, enter the password for your mongo DB instead.
Just put this Connection String somewhere safe we will need it later.

3.
.env
There is a file here called .env. Open it in VSC and you will see a non # line (line 2) that says DATABASE_CONNECTION_STRING =
on the other end of that '=' you want to paste your connection string. Example: DATABASE_CONNECTION_STRING = mongodb+srv://name:passwordddd@cluster0.libnbgg.mongodb.net/superheroes?retryWrites=true&w=majority&appName=Cluster0
Optional: before running the program in terminal you can make your mongoDB cluster view easier by adding the collection name of your choice. Come up with a name or use my name "superheroes" and put it inbetween the these 2 characters in your connection string. / and ?. See example 1 line above if confused where the collection name I used was superheroes.
now when you view your mongo DB collection it will be Clusters left hand side bar, browse collection.

4.
start server:
Now that we've done the pre steps we can begin running.
open this file in  vistual studio code or VSC.
We want to open a new terminal in VSC so go to the terminal option (top of screen) and hit new terminal window or control + shift + '
enter: 
npm run dev
if that does not work type node server.js and it MAY work, but npm run dev should always work.
NOTE: you may get a warning about not being able to open because the developer cannot be verified. You may have to hit cancel 2-3 times that is to be expected.

How do you open the website? after doing the above step open a browser of your choice and enter: http://localhost:3000/create-media in the URL bar
NOTE: by default unless you used the example database connection string and uncommented line 1 by deleting the '#' key, you will not see any posters of super hero movies up right now. You must add them all from scratch. If you are not already there head to the create new media page now and then go to step 5. 


5.

adding images to content: 
I understand adding images is a little different than you are probably used to. go to online image such as on google images and right click an image >> Copy Image Address.
an example of what you will be copying and pasting will look like this: https://cdn.europosters.eu/image/1300/133030.jpg 
Wherever it asks for a text field for an image address, paste that inside.


is Featured determines if the movie or tv show will be visible on the home menu.


stopping:
to stop server without closing the window use the keys: control + c in terminal
Closing the VSC window can also stop the server.
*/
