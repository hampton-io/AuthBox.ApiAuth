[![tested with jest](https://img.shields.io/badge/tested_with-jest-99424f.svg)](https://github.com/facebook/jest)

# AuthBox.ApiAuth

Package to provide auth strategy for API projects

Reference as a package through GitHub

### To use

### Config

Your config requires a section called 'auth' which should look like the following for JWT

```
{
    auth: {
        type: 'secret',
        secret: 'jwt-signing-secret'
    }
}
```

And for AzureActiveDirectory
```
{
    auth: {
        type: 'AAD',
        identityMetadata : 'Url for AAD metadata',
        clientID : 'AAD application id'
    }
}
```
### Usage
```
const auth = require('authbox.apiauth')
.
.
app.use(auth(app, config));
```
