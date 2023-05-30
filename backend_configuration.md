# Step 1
Before we start, we will have to prepare our Ubuntu  environment and get all libraries and programs updated and upgraded. The command we will run are:

       `sudo apt update && sudo apt upgrade`

This will do two things, update and then upgrade the Ubuntu repositories and associated programs.
You are likely to see the screen below:

![Screenshot (170)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/00b4f215-30f7-414f-8bd9-917e7fe74ea5)

Lets get the location of Node.js software from Ubuntu repositories.
To do this we will use the code:
          `Install node.js`  to install Node.js software

         `curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -`
         
 to verify installation od Node.js we will run the command
     `node -v` 
 this command would display the version of node.js if installed.
         

