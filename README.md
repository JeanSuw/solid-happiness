# Solid-Happiness
E-commerce Back End
## [Description](#table-of-content)

## table-of-content
* [Description](#description)
* [Installation](#installation)
* [Usage](#usage)
* [Walkthroughs](#walkthroughs)
* [Credits](#credits)

## Installation(#table-of-content)
This application will not be deployed. The walkthrough is provided in usage section

Package Requirement
```bash
npm i mysql2
npm i sequelize
npm i dotenv
```
## [Usage](#table-of-content)
Before starting the application, you must add schema.
Inside mysql, these are the commands you must type
```bash
mysql -u root -p
source db/schema.sql
quit
```
After you get out of mysql, you must run the seed before starting application
```bash
npm run seed
npm start
```

Insomnia is crucial for this project

Here are the quick copy and paste to insomnia request inputs
```bash
http://localhost:3001/api/Tags
http://localhost:3001/api/Categories
http://localhost:3001/api/Products
```

### GET all
SWITCH to GET
To GET all the items from Products, Categories, or tags.

### GET One with id
SWITCH to GET
To GET one item from Products, Categories, or tags

### PUT / Update
Switch to PUT
In Body dropdown menu, select JSON
Inside JSON add this input. You can rewrite anything in "INSERT_NAME_HERE"

```bash
// For products
{
    "product_name":"INSERT_NAME_HERE"
}
// For categories
{
    "category_name":"INSERT_NAME_HERE"
}
// For Tag
{
    "tag_name":"INSERT_NAME_HERE"
}
```
Once you are done, send the request and then go back to get all or get one product by the id that you updated.

### DEL / Delete
Switch to DEL

Copy one of these link to the DEL request and then add an id number that are avaliable in the database. I recommend to revisit GET All for the routes that you want your id in.

```bash
http://localhost:3001/api/Tags/"INSERT_ID_HERE"
http://localhost:3001/api/Categories/"INSERT_ID_HERE"
http://localhost:3001/api/Products/"INSERT_ID_HERE"
```

Once you are done, send the request and then go back to get all items (Tags, Categories, or Products) to see the changes you made.

### POST / Create new
Switch to POST
If you want to create a new product, switch to POST and switch to JSON. 
```bash
http://localhost:3001/api/Products
http://localhost:3001/api/Categories
http://localhost:3001/api/Tags

// For products
{
	"product_name": "Insert_Name",
	"price": numbers,
	"stock": number,
	"category": {
			"category_name": "Insert_Name"
	},
	"tag": null
}
// For categories
{
    "category_name":"INSERT_NAME_HERE"
}
// For Tag
{
    "tag_name":"INSERT_NAME_HERE"
}
```
## [Walkthroughs](#table-of-content)
* [Walkthrough for How to start application, request GET all and GET one by id](./tutorials/Part1.webm)
* [Walkthrough for How to Delete things by id](./tutorials/DeleteRequests.webm)
* [Walkthrough for How to Put/Update by id](./tutorials/UpdateRequest.webm)
* [Walkthrough for How to Post/Create new items](./tutorials/PostRequest.webm)


## [Credits](#table-of-content)
Without these guidances, my application would not exist

* [findByPk: Using findByPk and WHERE condition in sequelize](https://stackoverflow.com/questions/59111392/using-findbypk-and-where-condition-in-sequelize)
* [findByPk](https://www.tabnine.com/code/javascript/functions/sequelize/Model/findByPk)
* [Sequelize Model Querying Basic](https://sequelize.org/docs/v6/core-concepts/model-querying-basics/)
* [Sequelize Model Querying Finders](https://sequelize.org/docs/v6/core-concepts/model-querying-finders/)
* [Sequelize Associations](https://sequelize.org/docs/v6/core-concepts/assocs/)

Packages
* [Mysql2](https://www.npmjs.com/package/mysql2)
* [Sequelize](https://www.npmjs.com/package/sequelize)
* [Dotenv](https://www.npmjs.com/package/dotenv)

Bootcamp course 13-ORM
* 13-Ins_Validation
* 21-Ins_One-to-One
* 23-Ins_One-to-Many