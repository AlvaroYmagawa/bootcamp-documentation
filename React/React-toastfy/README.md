# React Toastify

Lib to manipulate warings, dialogs and messages for the final user.

## Installation

```
yarn add react-toastify
```

## Settings

- 1. In your <strong>App.js</strong> import <strong>ToastContainer</strong> component and add in your <strong>App return()</strong> function.

```
import { ToastContainer } from "react-toastify";
```

- 2.  Then into your <strong>global.js</strong> style import react-toastify/dist/ReactToastify.css path.

```
 import "react-toastify/dist/ReactToastify.css";
```

- 3. And now you have to import <strong>toast</strong> in the component that throw the message.

```
import { toast } from "react-toastify";
```

- 4. Use the toast <strong>error</strong> function to call the error.
     toast.error("Quantidade solicitada fora de estoque");
