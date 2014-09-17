blog.devteaminc.co
==================

This is the theme repository for the devteaminc blog and the devteaminc theme.


**Prerequisites**

- Node 
- NPM
- wget (from homebrew - `brew install wget`)

**Installation**

Clone the existing theme:

```
cd ~/sites
git clone https://github.com/devteaminc/blog.devteaminc.co.git
```

Grab the latest version of Ghost:

`wget http://ghost.org/zip/ghost-latest.zip`

Unzip directory, copy all content except from the README.MD from this directory into `~/sites/blog.devteaminc.co.git` (where prompted select the option to "keep newer")

Install Ghost:

```
cd ~/sites/blog.devteaminc.co
npm install --production
mv config.example.js config.js
```
Set the URL of your development/local site:

```
development: {
    // The url to use when providing links to the site, E.g. in RSS and email.
    url: 'http://localhost:2368',

    database: {
        client: 'sqlite3',
        connection: {
            filename: path.join(__dirname, '/content/data/ghost-dev.db')
        },
        debug: false
    },
    server: {
        // Host to be passed to node's `net.Server#listen()`
        host: '127.0.0.1',
        // Port to be passed to node's `net.Server#listen()`, for iisnode set this to `process.env.PORT`
        port: '2368'
    }
}
```

*you can at this stage setup your production ghost details but this file will only ever remain local - up to you!*


Start Ghost (by default npm start will start in development mode):

```
cd ~/sites/blog.devteaminc.co
npm start

```

Navigate to your local URL [http://localhost:2368/](http://localhost:2368/)  (by default), if this is working correctly then setup Ghost [http://localhost:2368/ghost](http://localhost:2368/ghost) and enable your template to test locally. 

Once you are happy this is working as you like, push your updates to Github - this will deploy the updates to the site.

`git push origin master`

 

