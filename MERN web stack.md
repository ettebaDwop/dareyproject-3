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

 ` mkdir Todo && cd Todo`
        
Running the command 
    
 ` npm init` 
    
gives the result below.

![Screenshot (175)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/fc441bbd-ba66-4f76-8b3a-f4099462604b)

### Installing expressjs
Install Express and create a file, index.js.

``` 
npm install express
touch index.js
```
Install the dotenv module

` npm install dotenv`

Open the index.js file

` vim index.js`

node index.js

![Screenshot (242)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/3920188e-21fd-41e4-b22a-2b83587bc2a3)

The next step is to open up port 5000 on the AWS EC2 instance

![Screenshot (244)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/23ebd2f0-8cb2-4fd1-8822-f4c17bb61527)

 On the browser this is what the result shou;s look like
 
![Screenshot (179)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/b9ecefdb-bb01-4b30-b959-d163c2a1afa1)



#### The routes directory

To provide the functionality required for our To-Do application, we need to implement three actions:

- Create a new task: This action will involve sending a POST request to a specific endpoint to add a new task to the list.

- Display a list of all tasks: This action will require a GET request to retrieve and display all the existing tasks.

- Delete a completed task: To remove a completed task from the list, we will use a DELETE request sent to the appropriate endpoint.

For each of these actions, we will create routes that define the necessary endpoints for our To-Do application. These routes will handle the incoming HTTP requests and execute the corresponding actions. Let's begin by creating a folder called "routes" to organize our route files

`mkdir routes && cd routes`

 Create a file api.js and open the file with the command:
 
 `touch api.js && vim api.js`
 
Paste the following code in the api.js file

```
const express = require ('express');
const router = express.Router();

router.get('/todos', (req, res, next) => {

});

router.post('/todos', (req, res, next) => {

});

router.delete('/todos/:id', (req, res, next) => {

})

module.exports = router;
```

### Models

Now we will incorporate MongoDB, a NoSQL database, into our application. To achieve this, we need to establish a model.

A model lies at the core of JavaScript-based applications, driving their interactivity and functionality.

In addition, we will utilize models to define the database schema. This step is crucial as it allows us to specify the fields stored in each MongoDB document. 

Essentially, the schema serves as a blueprint for constructing the database structure, including optional data fields that may not require storage in the database. These fields are referred to as virtual properties.

To create both a schema and a model, we will install Mongoose, a Node.js package designed to simplify working with MongoDB.

` npm install mongoose`

Create a new directory, "models", change into the models directory and create a new file , "todo.js" and paste the code as seen below:

` sudo mkdir models && cd models && touch todo.js`

![Screenshot (246)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/c7b17fb2-4aa7-4b81-ac3f-d630555d1b2d)

 Also, update the routes api.js file to look like this:
 
 ![Screenshot (248)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/526e875f-c579-4588-a021-a0ffc2c0c91b)


### Mongodb database
This step involves the creation of a MongoDB Database from mLab

![Screenshot (250)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/2e69f796-10ba-4dbc-9892-b2d94111ee9f)

```
To access environmental variables we create a .env file

touch .env
vi .env
```
To access the database run:

`DB = 'mongodb+srv://<username>:<password>@<network-address>/<dbname>?retryWrites=true&w=majority'`

![Screenshot (252)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/63db82a4-4653-46d4-bd6b-eb90abd7bddb)

To connect to the database run:

`node index.js`

![Screenshot (257)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/a0be7a3e-99c0-4092-b592-74e565bba0c0)

### Testing Backend Code without Frontend using RESTful API
To test the backend we will use Postman
![Screenshot (185)](https://github.com/ettebaDwop/dareyproject-3/assets/7973831/b6b73734-46b0-47ab-ae33-4dfe64b28816)


