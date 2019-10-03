# Styled Components
This package improve our style application, using js  inside our css.

```bash
# installation
yarn add styled-components
```

## Using function to manipulate css attributes

```bash
# Example
export const Title = styled.h1`
  font-size: 24px;
  color: ${props => (props.error ? 'red' : '#7159c1')}; /* Here we can control css propertys using js
  If the props error on the Title is true we change the color to red else the color is #7159c1
  */
  font-family: Arial, Helvetica, sans-serif;
`
```

## Chaining elements
You don't need to create a new styled components every time you need to create a new element, you can chaining then.
```bash
# Example
export const Title = styled.h1`
  font-size: 24px;
  font-family: Arial, Helvetica, sans-serif;

  chainningElement{
    background: blue;
  }
`
```

## References the own component
To reference the own component use '&' + some stage of css.
In this case the when the component is disabled he will have a opacity: 0.6 and his cursor will be blocked.
```
 &[disabled] { /* Css just works when disble is true */
    cursor: not-allowed;
    opacity: 0.6;
  }
```




## How to make a rotate animation 

### 1.
Import keyframes to work with animations.
```
import {keyframes} from 'styled components';
```

### 2.
Now create a const rotate to receive this.
```
const rotate = keyframes`
  from{
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
`;
```

### 3.
Now we need to import css to deal with props in css.
```
import {css} from 'styled components';
```

### 4.
Now create a function to make your svg animation works only when somethings is loading.
```
${props => props.loading && css`
    svg {
      animation: ${rotate} 2s linear infinite;
    }
  `};
```

## How to create a global style

### 1.
Create a folder styles and a file global.js

### 2.
Now import createGlobalstyle.
```
import { createGlobalStyle } from 'styled-components';
```

### 3. 
Import GlobalStyle in your App.js and add the component inside de return.
```
import GlobalStyle from './styles/global';
```

