
# G:LOOT iOS assignment
## Instructions
Build a iOS application that communicates with the server provided in this repository. You may use any library/framework/technique/boilerplate that you like and deem suitable for this assignment. If you use any library or framework that is not part of Apples standard frameworks, make sure to attach instructions on how to build your app.

The application you will build is a very simple player management tool. The user should be presented with a list of players received from the server, and have the option to add new players and view/update/delete existing ones. Think [CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete)

Expose the functionality of the API in a way that it is easily resusable in another project, i.e. seperate the code exposing the API from the application code. You don't have to create a framework or library from it, but that would be a plus.

## How to run the server
The server is a minimal HTTP-server exposing a REST-type API written using nodeJS and Express. You may alter the server code in any way you wish.

You will need to have nodeJS installed on your computer to run the server.

 1. Clone this repository.
 2. Open a terminal and run `npm i && npm run start` from the project root.
 3. The server is now running on `localhost:3000`. You can test the server by going to `http://localhost:3000/players` in your browser.

The API is described in `index.js` within the project root.

We recommend that you run the server on your local machine and test your app using the simulator. To get around Apples "App Transport Security" while testing make sure to add the following to the Info.plist.

```xml
<key>NSAppTransportSecurity</key>
<dict>
    <key>NSExceptionDomains</key>
    <dict>
        <key>127.0.0.1</key>
        <dict>
            <key>NSExceptionAllowsInsecureHTTPLoads</key>
            <true/>
        </dict>
        <key>localhost</key>
        <dict>
            <key>NSExceptionAllowsInsecureHTTPLoads</key>
            <true/>
        </dict>
    </dict>
</dict>
```

## Evaluation
These are some of the things we appreciate:

 - Easy, clean and readable code, no unnecessary complexity.
 - Testable code (separation of concern, referential transparency).
 - Exposing the API in a reusable way.
 - Handling of asynchronous fetching of data from an API.
 - Do not reinvent the wheel :)
 
## Submission notes:
 -  If you are using a boilerplate, please submit the boilerplate code and your own code in different git commits, so that we may differentiate the two.
 - Uploading the assignment to github and sending us the link is our preferred method of submission. However you may send the project as a zip file instead if github is not an option for you.
