# Redux

Redux is an open source JavaScript library for managing application state. It is most commonly used with libraries like React or Angular to create user interfaces.

## Intallation

```
# install redux and his integration wth react js
yarn add redux react-redux

```

## Settings

1. Create a store folder inside src, here is where you will storage all redux files

2. create a index.js file and create a reducer inside the store:

```
import { createStore } from 'redux';

const store = createStore();

export default store;
```

3. Now import store into your App.js

```
import store from './store';
```

4. And import Provider from react-redux into your App.js

```
import { Provider } from 'react-redux';
```

5. Now in your App.js return you will use the Provider components to involve all your others components and then you will add a props into your Provider components call store that will receive your store import.

```
#Example
<Provider store={store}>
      <BrowserRouter>
        <Header />
        <Routes />
        <GlobalStyle />
      </BrowserRouter>
    </Provider>

```

6. Note that will generate a error, this error is because you do not have any reducer inside your storage.

## How to create a reducer

1. Create a folder call modules and then create some reducer folder

store/
module/
example

2. Now inside the example folder create a reducer.js file and create a reducer

```
# Example
export default function example() {
  return [];
}
```

3. Now to create organize yours reducers better create a rootReducer.js file in store folder

```
# Example
import { combineReducers } from 'redux';

import cart from './cart/reducer';

export default combineReducers({
  cart,

})
```

4. And now in your storage/index.js import your rootReducer and add inside the store()

```
# Example
import { createStore } from 'redux';
import rootReducer from './modules/rootReducer';

const store = createStore(rootReducer);

export default store;
```

## How to connect your reducers into your application

1. You need to import connect from react-redux in some class that you want to manipulate the reducer.
```
import {connect} from 'react-redux'
```

2. Now in the class you imported connect from, you will need to change the default export and place, you should put it at the end of the file.
```
export default connect()(File Name);
```
3. Now create a function to manipulate this reducer.
```
handleAddProduct = product => {
    const { dispatch } = this.props;// dispatch is a redux function that you trigger your reducer switch function

    dispatch({ 
      type: 'ADD_TO_CART',
      product,
    })
  };
```

4. Now in your reducer that will be inside the src/ storage/ module/ example/ reducer.js
you will create a function like that to manipulate your state.
```
export default function cart(state = [], action) {
  switch (action.type) {
    case 'ADD_TO_CART':
      return [...state, action.product];
    default:
      return state;
  }
}
```

5. And now you can get this reducer in any component that have the 'connect' like that
```
export default connect(state => ({
  cart: state.cart,
}))(Header);
```

6. To get the state.cart you need to desestruturate him in your component like a props.

## Create reusable actions
1. First create a action.js file inside your src/store/modules/example

2. Now export the functions that you wanna use.
	```
	# example
	export function addToCart(product) {
  	  return {
    	    type: 'ADD_TO_CART',
    	    product,
  	  };
	}
	```

3. Now import your actions.js file in some Component that you wanna use the action and import bindActionsCreator from redux to deal with actions.
	```
	# import action.js
	import * as ExampleActions from '../../store/modules/example/actions.js'
	# import bindActionsCreators
	import { bindActionCreators } from 'redux';
	```

4. In the end of your component create a const that will receive the actions.
	```
	const mapDispatchToProps = dispatch =>
	  bindActionCreators(CartActions, dispatch);
	```

5. Now add this const inside your connect function, and after that you can desestruturate yours actions in this.state of this component.
	```
	export default connect(null, mapDispatchToProps)(Example);
	```



