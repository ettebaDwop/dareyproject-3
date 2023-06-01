# The MERN Web Stack Implementation

The MERN stack is a popular web development stack that consists of MongoDB, Express.js, React.js, and Node.js. This project documents a step-by-step instructions on implementing the MERN stack on Amazon AWS using an Ubuntu Server. The MERN stack allows you to build scalable and efficient web applications. This project will attempt to create a Simple to-do application on MERN  web stack.

The implementation will involve the follwowing steps:

#### Step 1
- Backend configuration
- Installing expressjs
- Models
- Mongodb database
#### Step 2
- Frontend creation
- Frontend creation (continued)




# Step 1
### Backend Configuration
* Create a new EC2 instance on the Amazon AWS Console
* Prepare our Ubuntu  environment and get all libraries and programs updated and upgraded.
The command we will run are:

       `sudo apt update && sudo apt upgrade`

This will do two things, update and then upgrade the Ubuntu repositories and associated programs.
You are likely to see the screen below:

![Screenshot (170)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/00b4f215-30f7-414f-8bd9-917e7fe74ea5)

Lets get the location of Node.js software from Ubuntu repositories.
To do this we will use the code:

     `curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -`

To install both  Node.js and the packet manager for node.js, npm, run:

    ` sudo apt-get install -y nodejs`
     
 to verify installation od Node.js we will run the command:
 
     `node -v && npm -v` 
This command would display the version of node.js if installed.

#### Application Code Setup
Create a new directory, "Todo" and change into the directory using the following commands:

        `mkdir Todo && cd Todo`
        
    Running the command 
    
        `npm init` 
    
    gives the result below.

![Screenshot (175)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/fc441bbd-ba66-4f76-8b3a-f4099462604b)
