# External-Resources
Hey, guys! Here's a list of useful tips and resources for unit 3

## Group Git Steps:
#### Team Leader
1. Create an empty GitHub repo
2. Locally, `mkdir project_folder_name` then `cd` && `git init` 
3. Locally, `git remote add <git url>`. 
4. Confirm this with `git remote -v`
5. Create file(s) and `git add -A` then `git commit -m 'relevant message'`
6. `git push origin master` push to repo master branch.
7. If you have a pull request pending, view the request and merge if and only if the code is perfect
8. `git checkout -b yourname-dev` to create dev branch and checkout to dev branch
9. Run `git remote add upstream <team leader git url>`
9. Create a new file and `git add -A` then `git commit -m 'relevant message'` 
10. `git push origin yourname-dev`
11. If you have a pull request pending, view the request and merge if and only if the code is perfect
12. `git checkout master` then `git merge dev`

#### Teammates
1. Fork and clone team leader's repo i.e. `git clone <your forked git repo url>`. This will be your `origin`
3. run `git remote add upstream <team leader git url>`
2. run `git checkout -b yourname-dev` to create a dev branch
4. Create a new file (e.g.- `name.html`) and `git add -A` then `git commit -m 'relevant message'` 
4. Run `git push origin yourname-dev`
5. Send a pull request to team leader
6. The team leader merges the code to master.
7. Run `git pull upstream master` to get current version from team leader locally. Your local branch should now be up to date with the upstream master.
8. `git merge master` will merge the latest version of the code to your dev branch.

## JSON
- A data exchange format.
- A way to represent data.
- A string with a specific format.

## AJAX
AJAX = Asynchronous JavaScript And XML.
AJAX transport data as plain text or JSON text.
AJAX allows developers to:
- Read data from a web server - after a web page has loaded
- Update a web page without reloading the page
- Send data to a web server - in the background

## Axios 
Axios is a very popular library and we can use it in the browser and with node. 
We use Axios for our AJAX requests

**[Axios Documentation](https://github.com/axios/axios)**

#### Installing
Using npm:
```bash
$ npm install axios
```

Using cdn:
```html
<script src="https://unpkg.com/axios/dist/axios.min.js"></script>
```

## AJAX Request
- method
    - GET
    - POST
    - DELETE
    - PATCH/PUT
- url
    - https://swapi.co/api/people/1
    - https://pokeapi.co/api/v2/pokemon/2
- data (optional)


### Response Object
- *data*: the payload returned from the server. By default, Axios expects JSON and will parse this back into a JavaScript object for you.
- *status*: the HTTP code returned from the server.
- *statusText*: the HTTP status message returned by the server.

### Error Object
- *message*: the error message text.
- *response*: the response object (if received) as described in the previous section.
- *request*: the actual XMLHttpRequest object (when running in a browser).

### Handling Responses
Since an AJAX call is asynchronous, we need to handle its response in a particular way.  
To work with asynchronous javascript, we are going to use promises and a promise chain.
The `.then` and `.catch` method want us to pass them functions to run. 
We often use anonymous, fat arrow functions `.then(() =>`  `.catch(()=>`
`axios` will pass our functions the `response` or `error` object so that we can access the data that the API returns to us.

```js
axios({
  url: 'https://dog.ceo/api/breed/boxer/images/random',
  method: 'get',
})
.then((response) => { //.then wants a function to run if the request is succesful
    // code for if the request succeeds
    console.log(response)
}) 
.catch((error)=>{ 
    // code for if the request fails
    console.log(error)
}) 
```

## Promises 
1. **[Promise - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)**
2. **[Async functions](https://developers.google.com/web/fundamentals/primers/async-functions)**
3. **[Promises](https://www.promisejs.org/)**
4. **[Common Promise Mistakes](https://pouchdb.com/2015/05/18/we-have-a-problem-with-promises.html)**
5. **[Promisees · Courtesy of ponyfoo.com](http://bevacqua.github.io/promisees/)**
6. **[wbinnssmith/awesome-promises: A curated list of useful resources for JavaScript Promises](https://github.com/wbinnssmith/awesome-promises)**
7. **[How to escape Promise Hell — Medium](https://medium.com/@pyrolistical/how-to-get-out-of-promise-hell-8c20e0ab0513#.4wtj9hlvw)**

## API:
1. **[Collective list of free APIs](https://github.com/public-apis/public-apis)**


## React Steps:
1. **Install create-react-app tool globally so we'll always have it available in our Terminal:** in the terminal write $`npm i -g create-react-app`
2. **Create React app:** in the terminal write $`create-react-app app_name`
3. **Run React app:**  in the terminal $`npm start`

## React Commands:
#### Create App
**Create React project:** in the terminal write 
```bash 
create-react-app app_name
```
**Start React project:** in the terminal write 
```bash 
npm start
```
