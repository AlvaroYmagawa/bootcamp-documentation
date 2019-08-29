## Commands


//Function to create a token
jwt.sign({id}, secret, {expireIn: 1d})


//Function to compare tokens, then return the value inside(needs try and catch)
const decoded = promisify(jwt.verify)(token, token2);

