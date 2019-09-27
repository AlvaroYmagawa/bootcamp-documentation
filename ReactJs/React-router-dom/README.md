# React-router-dom
Is a package to deal with single page aplication (SPA) and control our frontend routes.

```
# Install
yarn add react-router-dom
```

## BrowserRouter
In react-router-dom we have routers for several types of application, so to run a application in browser we use the BrowserRoutes.

## Switch
Is responsable to change our routes.

## Route 
Route manage with our URL application 

```bash
#Example
export default function Routes() {
  return (
    <BrowserRouter>
      <Switch>
        <Route path="/" exact component={Main} /> // This url call the component Main 
        <Route path="/repository" component={Repository} />
      </Switch>
    </BrowserRouter>
  );
}
```

## Navigating between routes and encoding the url.

### 1. 
You need to import the Link class inside react-router-dom
```
import { Link } from 'react-router-dom'
```

### 2.
Now use the Link component inside your application for where you want to redirecionate to another page.
And set the url where you wanna go.
```
# Example
<Link to={`/repository/${encodeURIComponent(repository.name)}`}>Detalhes</Link>
* encodeURIComponent()  encode the param to deal with special characters like '/'or ' '
```

## Decoding the param

### 1.
First to get a param inside a url, you'll need to set a name for your param inside your routes.

```
# Example
<Route path="/repository/:repository" component={Repository} />
```

### 2.
Now to acess this param you need to desestruturate the 'match' in your Component that will receive your param.
And then decode the param with Js decodeURIComponent function.

```
# Example
export default function Repository({ match }) {
  return (
    <h1>Repository: {decodeURIComponent(match.params.repository)}</h1>
  );
}
```


