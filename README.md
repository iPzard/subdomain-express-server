# Subdomain Express server
Subdomain Express server for multi-app projects.

# Setup
Clone the project and run `npm install`. Add your sites to the domain folder then update `./config/domains.js` to match your project structure. The `server.js` file utilizes vhost to allow for multiple subdomains, reconfigure these to match your domains. Regex is used instead of hardcoding the domain to allow for developing and testing on `localhost`.

# Servers
If your app or apps have their own server, you can export it instead of listening to a port in the server file. Set its template property to `"app"` in `domain.js`. The `setEngine()` function will expect your server file to be named `server.js` at the root of your projects folder in `domains`. For example, if your app was named `foo`, your `server.js` file should be found as follows `./domains/foo/server.js`.

# Tests
Tests have been configured to test if the domains configured in `./config/domains.js` match the domain directory structure of your project. To run tests, use `npm test` or `npm run test`. 

# Launch
To launch the server, use `npm start` and navigate to `your subdomain here`.localhost:8080 in your browser.