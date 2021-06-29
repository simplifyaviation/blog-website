# Blog-website

## Objective

- To become familiar with the different express notations

## To Start

Take a look at the dependencies in the `package.json` file. You will note that the package requires the following:

1. Body Parser -
2. EJS -
3. Express -
4. Lodash -

Take a look through all the files in the submission folder and become familiar with how the application will work.

Follow the steps below to install the dependencies and start the app.

1. Open a new terminal and change into the submission directory.

`cd submission`

2. Install the dependencies

`npm install`

---

## Part A

### Starting the server

Open `app.js` to find your starting place. In here we have imported express, bodyparser and ejs from the node modules.

Objective: Have an h1 tag with the word home displayed on your webpage.

Steps:

1. In the home.ejs file (located in views), input the h1 tag with home written inbetween `<h1>home</h1>
2. In the app.js file create a callback function that renders home file.
3. Start your application `nodemon app.js`

[](image)

Hints:

1. Create a route using `app.get` to determine what route you are specifying and a call back function that will render your webpage.
2. `app.get("", () => {})
3. In the quotation marks we need to put the route, in this case is the home route. We can use "/"
4. Inside the parenthases, we input our parameters of request and response which is shortened to (req, res)
5. Inside the function we use res.render() (we get the render() method from express.)
6. Determine what you want to render and place it inside the render brackets.

[](Video of how to do it)

---

## Part B

Objective: Display the homeStartingContent on the home page using EJS.

Steps:

1. Open your `home.ejs` file
2. You need to add a `<p>` tag that will contain the homeStarting content in it.
3. Input EJS tag inside of the p tag. You can use https://ejs.co/#docs to determine what tag to use.
4. Inside the EJS tag write startingContent.
5. open the app.js file. Instead of just rendering the home.ejs page, we are going to enter another parameter, which is going to be a javascript object which is going to be a key value pair.
6. The key has to match the with the variable name inside the home.ejs file.
7. The value is whatever you want to be displayed.

[](image)

Hints:

1. The EJS tag for HTML content is <%= =>
2. Inside home.ejs input the following code under your H1 tag `<p><%= startingContent %></p>`
3. Change the following code to accpet another parameter: `res.render("home")`
4. `res.render("home" , {key : value})

[](Video of how to do it)

## Part C

## Part D
