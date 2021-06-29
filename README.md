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

[](image)

Hints:

1. Create a route using `app.get` to determine what route you are specifying and a call back function that will render your webpage.
2. `app.get("", () => {})
3. In the quotation marks we need to put the route, in this case is the home route. We can use "/"
4. Inside the parenthases, we input our parameters of request and response which is shortened to (req, res)
5. Inside the function we use res.render() (we get the render() method from express.)
6. Determine what you want to render and place it inside the render brackets.

---

## Part B

## Part C

## Part D
