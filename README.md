# newsscraper
This is an application that will scrape news from a news source and display the articles on the site.  This will uses Node.js, MongoDB, Mongoose, Cheerio, Express, and Express-handlebars.

You may go to [https://fullers-newsscraper.herokuapp.com](https://fullers-newsscraper.herokuapp.com) to view a demo of the application.

## Technologies used
The following technologies, tools, and npm packages were used:
* Node.js
* Javascript/Jquery
* NPM Packages
	* express
	* body-parser  
	* express-handlebars
	* handlebars
	* mongodb
	* mongoose
	* morgan
	* bluebird
* MVC Desgin
* Object Relational Mapping (ORM)
* MongoDB and MongoLAB (heroku add-on)

 ## Files and Folder Structure

* **server.js** - File used to start the node.js web server. Setup routes and MongoDB Connection
* **package.json** - File used to install the npm packages.
* **.gitignore** - File used to ignore the node_modules folder used by NPM.
* **models** - Folder to house the model files.
	* Article.js - File created for MongoDB, this model creates the document for MongoDB called articles.
	* Note.js - File created for MongoDB, this model creates the document for MongoDB called notes.
* **public** - Folder to store any files the browser needs to access.
	* **css** - Sub folder to store css files.
			* style.css - File used to create the CSS needed for the application.
	* **img** - Sub folder to store image files.
			* newsscraper.png - image used for this README.md
* **views** - Folder used for express-handlebars
	* **layouts** - stores the main.handlbars view
		* **main.handlebars** - View that creates the template for the application
	* **index.handlebars** - View that creates the body of the main.handlebars view

## Requirements

For MongoDB Connection.  Please note the `mongodb://` needs to be included first in your URI.

```javascript

//Database configuration with mongoose
var dbURI = 'Your local Mongo URI';
if (process.env.NODE_ENV === 'production') {
    dbURI= "Your heroku Mongo URI";
}
mongoose.connect(dbURI);
var db = mongoose.connection;

```

## Getting Started

* Use git clone to copy this git hub 

* Open the command line and navigate to the folder when you cloned the files
	* Run npm install to install dependencies.
	* Use run server.js to start the application.
* use localhost:3000 in your browser to access this application. 

### Anime News Scraper! - Home Page 

![Alt Text](/public/img/newsscraper.png?raw=true "Anime News Scraper! Home Page")

The application will automatically scrape the news from [https://www.animenewsnetwork.com/](https://www.animenewsnetwork.com/). You can click on an article and you may save and delete notes about the article.

## Author

* **Shaun** - * Javascript, Node.js, Express, Express-Handlebars, Handlebars (HTML Templates), Mongoose, MongoDB*

## License
   
   None 
