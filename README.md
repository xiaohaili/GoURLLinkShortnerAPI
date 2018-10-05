# Generate a Short URL

Forked from https://github.com/minaandrawos/GoURLLinkShortnerAPI, adding an index.html that is forked from https://github.com/Lusitaniae/Golang-Url-Shortener. Background image from https://bing.com.

Full tutorial could be found at http://www.minaandrawos.com/2015/09/05/link-shortener-golang-web-service-tutorial-mongodb/

The purpose of the API is to shorten url links via a REST HTTP request. 
Once the code is built and running, to create a short url to a long url mapping, send a POST request to http://localhost:5100/Create, the POST request should include the shortUrl and the longUrl as follows:
{'shorturl':'cosmosfading','longurl':'https://cosmosmagazine.com/space/universe-slowly-fading-away'}

You could then consume a shorturl by issuing a GET request to http://localhost:5100/shorturl

The program makes use of the Gorilla web toolkit mux library (http://www.gorillatoolkit.org/pkg/mux) for routing as well as the mgo library (https://labix.org/mgo) to interface with mongo database

The code utilizes the socket pool that comes with the mgo library for efficient concurrent communication with Mongodb. It also makes use of the nice http routing and handling syntax that comes with Gorilla mux.
