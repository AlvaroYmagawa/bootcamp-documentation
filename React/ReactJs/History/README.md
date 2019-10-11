# History
It is a package to deal with navigations in React when you needs to wait for some process end to be executed 

like a api call.

## Installation
```
yarn add history
```

## Settings
- 1. In your <strong>services</strong> folder create a <strong>history.js</strong> file.
```
# Example
import { createBrowserHistory } from "history";

const history = createBrowserHistory();

export default history;

```

- 2. Now in your <strong>App.js</strong> file import <strong>history</strong> and change your <strong>BrowserRouter</strong> to <strong>Router</strong> and add a <strong>history</strong> props that receive <strong>history</strong>

```
# history import
import history from "./services/history";

# Example
function App() {
  return (
    <Provider store={store}>
      <Router history={history}>
        <Header />
        <Routes />
        <ToastContainer autoClose={3000} />
        <GlobalStyle />
      </Router>
    </Provider>
  );
}
```

- 3. And now in your component that you want to use history import him and use history <strong>push</strong> function and add the url to change your route.
```
# Example
history.push("/cart");
```
