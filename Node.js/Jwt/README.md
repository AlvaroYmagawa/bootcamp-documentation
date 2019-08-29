# Json Web Token (JWT)
JSON Web Token is an Internet standard for creating JSON-based access tokens that assert a number of claims.

## Commands
```bash
# function to create a token
jwt.sign({id}, secret, {expireIn: 1d})

# function to compare tokens, then return the value inside(needs try and catch and import promisify from 'util')
const decoded = promisify(jwt.verify)(token, token2);

