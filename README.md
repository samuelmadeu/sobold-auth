Ruby Auth0 API 

.env file needed for the AUTH0_CLIENT_SECRET and AUTH0_CLIENT_ID.


````bash
# .env file
AUTH0_CLIENT_SECRET=myCoolSecret
AUTH0_CLIENT_ID=myCoolClientId
````

Once you've set those 2 enviroment variables, run `bundle install`, then run `rackup -p 3001` and try calling [http://localhost:3001/ping](http://localhost:3001/ping)

You can then try to do a GET to [http://localhost:3001/secured/ping](http://localhost:3001/secured/ping) which will throw an error if you don't send the JWT in the header.

__Note:__ if you need to enable cross-origin resource sharing, check out the [sinatra-cors_origin](
https://github.com/britg/sinatra-cross_origin) gem.
