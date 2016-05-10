#Boilerplate API

Setup a boilerplate server-side API using Node, JavaScript, LoopBack (from the developers of Express and major contributor to the open source Node project), and a few other goodies.

##About LoopBack and StrongLoop

Boilerplate API uses LoopBack, an open source API framework built by San Mateo, California based company StrongLoop.  StrongLoop has been a very important contributor to the latest Node version and the Node community as a whole for quite some time.  StrongLoop are the current maintainers of the world's most popular and widely used Node framework for server-side development, Express.  Most developers use Express to serve pages, in lieu of Apache for example.

##What is LoopBack?

LoopBack makes it easy to connect to your backend data sources. It is built on top of Express, which means it's been tested, it works, it scales, it's intuitive (for us anyways).

It can also take a simple data model definition and easily generate a fully functional end-to-end REST API that can be called by any client.  Your boss will be taking you to lunch over this (maybe, no promises.  I don't know your boss).

LoopBack comes with a built-in client called the LoopBack API Explorer, which makes it easy for you to test the REST API endpoints you set up by simulating real world requests and responses.

##Requirements

Most importantly, you need to have Node installed on your machine, or whatever machine you choose to use as a web server.  It's free and it's easy to install to that's a no brainer. Get it here. npm comes with it, and you'll be needing that too.

https://nodejs.org/en/

You'll also need git, which I'm assuming you have if you use GitHub, but maybe you don't, and you just like reading README files for fun, and what not, so here's a URL for that:

https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

Let’s get started!

##Boilerplate API Installation Process

`$ git init`
`$ npm install --save strongloop`
`$ slc loopback`
`$ slc loopback:status`

..or something like that.  You'll be fine.

####Setup Your API Database

0. The LoopBack Connector for Boilerplate API has plugins that allow you to connect with most major datasources, and is pre-configured to use MongoDB.  Unless you require something else, feel free to use the defaults.

    - Oracle
    - MySQL
    - PostgreSQL
    - Redis
    - SQL Server
    - MongoDB

1. Install the Connector:

	`$ npm install --save loopback-connector-mongodb`


2. Add a DataSource:

	`$ slc loopback:datasource`

	Which will ask you to ...
	1. Enter the data-source name: <datasource-name>
	2. Select the connector for <datasource-name>: MongoDB (supported by StrongLoop)

3. Configure your DataSource:

	Here is a good default database setup configuration.  Enter your personal information where it asks for it.

	  "(your-datasource-name)": {
	    "name": "(your-datasource-name)",
	    "connector": "mongodb",
	    "host": "(your host, ex: localhost)",
	    "port": (an port that your api can use, ex: 27771),
	    "database": "(your-database-name)",
	    "username": "(your-username)",
	    "password": "(your-password)"
	  }

##Test Your REST with LoopBack API Explorer

It’s time to see what we’ve built so far! We’ll use the awesome built-in tool, LoopBack API Explorer, which can be used as a client for the service we just created. Let’s try testing REST API calls.

API Explorer allows you to select any of the exposed methods, and then see corresponding model schema in the bottom right corner. In the data text area, it is possible to write a custom HTTP request. Once the request is filled in, click the “Try it out” button, and the server’s response will be displayed below.

##Detailed Test Instructions:x

1. In a separate window, start MongoDB with:

    `$ mongod`

2. Run the application with:\

    `$ node .`

3. In your browser, go to: http://localhost:3000/explorer/

4. You'll see an administrative page for the StrongLoop API Explorer, which is intuitive enought for novices to figure out.

5. Select any of the exposed methods, and the corresponding model schema will be displayed in the bottom right corner.

6. In the data text area, it is possible to write a custom HTTP request.

7. Once the request is filled in, click the “Try it out” button

7. See the server’s response displayed in the box below

8. Edit your files within the skeleton of the application.

9.  A lot more comes after this, but I'm tired and It's rush hour, so ttyl.

#SBoilerplate API

Setup a boilerplate server-side API using Node, JavaScript, LoopBack (from the developers of Express and major contributor to the open source Node project), and a few other goodies.

##About LoopBack and StrongLoop

Boilerplate API uses LoopBack, an open source API framework built by San Mateo, California based company StrongLoop.  StrongLoop has been a very important contributor to the latest Node version and the Node community as a whole for quite some time.  StrongLoop are the current maintainers of the world's most popular and widely used Node framework for server-side development, Express.  Most developers use Express to serve pages, in lieu of Apache for example.

##What is LoopBack?

LoopBack makes it easy to connect to your backend data sources. It is built on top of Express, which means it's been tested, it works, it scales, it's intuitive (for us anyways).

It can also take a simple data model definition and easily generate a fully functional end-to-end REST API that can be called by any client.  Your boss will be taking you to lunch over this (maybe, no promises.  I don't know your boss).

LoopBack comes with a built-in client called the LoopBack API Explorer, which makes it easy for you to test the REST API endpoints you set up by simulating real world requests and responses.

##Requirements

Most importantly, you need to have Node installed on your machine, or whatever machine you choose to use as a web server.  It's free and it's easy to install to that's a no brainer. Get it here. npm comes with it, and you'll be needing that too.

https://nodejs.org/en/

You'll also need git, which I'm assuming you have if you use GitHub, but maybe you don't, and you just like reading README files for fun, and what not, so here's a URL for that:

https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

Let’s get started!

##Boilerplate API Installation Process

`$ git init`
`$ npm install --save strongloop`
`$ slc loopback`
`$ slc loopback:status`

..or something like that.  You'll be fine.

####Setup Your API Database

0. The LoopBack Connector for Boilerplate API has plugins that allow you to connect with most major datasources, and is pre-configured to use MongoDB.  Unless you require something else, feel free to use the defaults.

    - Oracle
    - MySQL
    - PostgreSQL
    - Redis
    - SQL Server
    - MongoDB

1. Install the Connector:

    `$ npm install --save loopback-connector-mongodb`


2. Add a DataSource:

    `$ slc loopback:datasource`

    Which will ask you to ...
    1. Enter the data-source name: <datasource-name>
    2. Select the connector for <datasource-name>: MongoDB (supported by StrongLoop)

3. Configure your DataSource:

    Use this configuration...

      "datasource-name": {
        "name": "(your-datasource-name)",   // the name you gave your datasource
        "connector": "mongodb",             // change this if not using mongodb
        "host": "localhost",                // your host
        "port": 27771,                      // whatever port number you want to use
        "database": "(your-database-name)", // the name of your database in mongodb
        "username": "(your-username)",      // a mongodb username with admin-like permissions
        "password": "(your-password)"       // a mongodb password with admin-like permissions
      }

##Test Your REST with LoopBack API Explorer

It’s time to see what we’ve built so far! We’ll use the awesome built-in tool, LoopBack API Explorer, which can be used as a client for the service we just created. Let’s try testing REST API calls.

API Explorer allows you to select any of the exposed methods, and then see corresponding model schema in the bottom right corner. In the data text area, it is possible to write a custom HTTP request. Once the request is filled in, click the “Try it out” button, and the server’s response will be displayed below.

##Detailed Test Instructions:x

1. In a separate window, start MongoDB:

    `$ mongod`

2. Run the application:

    `$ node .`

3. Go to: http://localhost:3000/explorer/

4. You'll see an administrative page for the StrongLoop API Explorer, which is intuitive enought for novices to figure out.

5. Select any of the exposed methods, and the corresponding model schema will be displayed in the bottom right corner.

6. In the data text area, it is possible to write a custom HTTP request.

7. Once the request is filled in, click the “Try it out” button

7. See the server’s response displayed in the box below

8. Edit your files within the skeleton of the application. You'll notice some new directories for your project.

    - /server: Node application scripts and configuration files.
    - /client: Contains .js, .html, .css, and all other static files
    - /common: Used by both server and client. Model files go in common.

9. Configure the Model (a good example shown)

`{
  "User": {
    "dataSource": "datasource-name"
  },
  "AccessToken": {
    "dataSource": "datasource-name",
    "public": false
  },
  "ACL": {
    "dataSource": "datasource-name",
    "public": false
  },
  "RoleMapping": {
    "dataSource": "datasource-name",
    "public": false
  },
  "Role": {
    "dataSource": "datasource-name",
    "public": false
  },
  "Gift": {
    "dataSource": "datasource-name",
    "public": true
  },
  "Donor": {
    "dataSource": "datasource-name",
    "public": true
  },
  "Receiver": {
    "dataSource": "datasource-name",
    "public": true
  }
}

Open `server/model-config.json` and change the datasource for all entities we want to persist in the DB to "(datasource-name)".

10.  Search Google for LoopBack and become a sponge for informaton about using the product, for about an hour.  It may not take you that long or it may take you longer.  Just go learn more.  You need to know your stuff.

##Note for Newbies

Please, remember, the configurations above do not contain literal names, usernames, passwords, etc.

If it's in parenthesis, that means you need to supply that information.   Don't actually use the parenthesis, and don't call your datasource datasource-name.

Just being sure.  You don't know how many times I get that.
`
