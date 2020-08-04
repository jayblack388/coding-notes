# Server VS Client

Javascript can be run in a number of different environments. The most regular places are server side (Node.js) or browser side (typically with a front end framework)

## Client

Up until this point, you've likely only/mostly seen client side javascript. This is javascript that exists and operates on the browser. Typically it's embedded in a script tag or imported from a javascript file that exists within a `public` or `static` folder. You can include other libraries/services through CDN's (do this) or directly sourced in your client app (don't do this it bloats your app). 

Up until now you've likely used something like jQuery's ajax functions to make requests to third party API's. When you don't have access to your own server this is ok practice, but as you gain an understanding of server side javascript and routing, it becomes important that you filter your client side requests to your own server, and from within the server, make requests to third party services. This will enable you to better protect resources like API Keys, as well as organize your code better. 

Imagine that you have a client app that is retrieving movie data directly from the OMDB api. If instead you wanted to switch to IMDB or Rotten Tomatoes (or query all 3 API's), you would have to rewrite your client side javascript to interpret each different response data. A better way to handle this is for your client side to request all movie data from your own server. Your server then reaches out to each different 3rd party API and transforms the data into a format that your client side can reliably use.

## Server

Javascript will run on the server as long as it's contained within a node package. The general idea is that we have a centralized node package with different "services" branching out of the package. Typically the functionality of the package will be extended by other packages listed in your own package's dependencies. 

For example, a really common extension is to add an `express` server. `express` is just a framework for generating servers. It can connect to various datasources, serve static or dynamic HTML, handle authentication, and even incorporate other servers as middleware.

Ideally each individual piece/service of the app (database/models, client/views, router/controller) can be abstracted/isolated so that their individual functionality is separate from other pieces of the app. That way if we choose to replace one of the services, it will only minimally affect the rest of the app.
