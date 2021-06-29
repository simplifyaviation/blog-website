# Blog-website

## Objective

- To become familiar with the different express notations

## To Start

Take a look at the dependencies in the `package.json` file. You will note that the package requires the following:

1. [Body Parser](https://www.npmjs.com/package/body-parser) - 
2. [EJS](https://ejs.co/#docs) -
3. [Express](https://expressjs.com/en/guide/routing.html) - 
4. [Lodash](https://lodash.com/) -

Take a look through all the files in the submission folder and become familiar with how the application will work.

Follow the steps below to install the dependencies and start the app.

1. Open a new terminal and change into the submission directory.

`cd submission`

2. Install the dependencies

`npm install`


## Part A

### Starting the server

Open `app.js` to find your starting place. In here we have imported express, bodyparser, lodash and ejs from the node modules.

Objective: Have an h1 tag with the word home displayed on your webpage.

Steps:

1. In the home.ejs file (located in views directory), write home in an h1 tag: `<h1>home</h1>`
2. In the app.js file create a callback function that renders home file.
3. Start your application `node app.js`

[](image)

### Hints

1. Create a route using `app.get` to determine what route you are specifying and a call back function that will render your webpage.

`app.get("", () => {})`

2. In the quotation marks we need to put the route, in this case, the home route. We can use "/"
3. Inside the parenthesis, input the parameters of request and response which is shortened to (req, res)
4. Inside the function use res.render() (we get the render() method from express.)
5. Determine what you want to render and place it inside the render brackets.

[](Video of how to do it)


## Part B

Objective: Display the homeStartingContent on the home page using EJS.

Steps:

1. Open your `home.ejs` file
2. You need to add a `<p>` tag that will contain the homeStarting content in it.
3. Input EJS tag inside of the p tag. You can use [EJS](https://ejs.co/#docs) to determine what tag to use.
4. Inside the EJS tag write startingContent.
5. Open the app.js file. Instead of just rendering the home.ejs page, we are going to enter another parameter, which is going to be a javascript object and is going to be a key value pair.
6. The key has to match with the variable name inside the home.ejs file.
7. The value is whatever you want to be displayed.

![exercise](docs/exercise.png)

Hints:

1. The EJS tag for HTML content is `<%= =>`
2. Inside home.ejs input the following code under your H1 tag `<p><%= startingContent %></p>`
3. Change the following code to accpet another parameter: `res.render("home")`
4. `res.render("home" , {key : value})

[](Video of how to do it)


## Part C

Objective: Display the header and footer partials on the home page.

Steps:

1. Open the home.ejs file

2. Use the following layout example to include the header and footer to your webpage.

```
<%- include('header'); -%>
<h1>Title</h1>
<p>My page</p>
<%- include('footer'); -%>
```

3. Refresh your page

[](image)

[video]

## Part D

Objective: Create routes for the about us, compose and contact pages.

Steps:

1. Create a route that renders the contact page (that includes the header and footer partials) that also renders the contact text.
2. Do the same thing for the about us and compose page.

[video]


## Part E

Objective: Add a post method to tell the server what to do when someone makes a post request to the /compose route.

Steps:

1. Open app.js
2. Create a post method that handles the data that is posted from the user when using the form in the compose.js file.
3. create a variable that contains an object with the following keys and values:

```
title: req.body.postTitle
content: req.body.postBody
```

4. push the post to the array posts.
5. redirect the user to the home page.

[gif]

[video]


## Part F

Objective: Show the blog posts on the home page.

Steps:

1. Open the file home.ejs
2. Create a loop that loops through the posts array. (hint- use a forEach loop)
3. In the loop input the title for each post in an h1 tag
4. In the loop input the content inside a p tag.
5. input a read more link that links to the post page.
6. Add the posts array to the object in `app.js` in the key:vaule format.

Answer:

home.ejs

```
<% posts.forEach((post) => { %>
<h1><%=post.title%></h1><p> 
<%=post.content%>
<a href="/posts/<%=post.title%>">Read More</a></p>
<% }) %>
```

app.js

```
app.get("/", (req, res) => { 
    res.render("home", { startingContent: homeStartingContent, posts: posts });
     });
```


## Part G

Objective: Create a route that directs to a page that contains each individual post.

Have a look through the express documentation - [express routing](https://expressjs.com/en/guide/routing.html)

Steps:

1. Use the following code example to create a path for each individual blog post.

```
app.get('/users/:userId/books/:bookId', (req, res) => { res.send(req.params) })
```

2. loop through the posts array and check to see if the requested title is equal to a title that is contained in the posts array.
3. render the post title and content.

Bonus: handle the case sensitiviy on the title when input into the url. (hint - use lodash)

Answer:


## Part H - Bonus

Objective: Reduce the amount of content text on the homepage to 100 characters (blog post content).
