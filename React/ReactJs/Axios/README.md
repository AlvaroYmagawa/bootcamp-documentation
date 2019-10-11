# Axios
Package to deal with Apit rest

```bash
# Installation
yarn add axios
```

## Set a baseUrl
Create a api.js file inside a services folder in src then create a const api that will receive a baseurl.

```
# Example
import axios from 'axios';

const api = axios.create({
  baseURL: 'https://api.github.com',
});

export default api;
```

