Before we start, we will have to prepare our Ubuntu  environment and get all libraries and programs updated and upgraded. The code we will ise are:

`sudo apt update && sudo apt upgrade`
This will do two things, update and then upgrade the Ubuntu repositories and associated programs.
You are likely to see the screen below:


Lets get the location of Node.js software from Ubuntu repositories.
To do this we will use the code:

`curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -`
