import React from 'react';

**Module 5**
 - Working with Props and State State and its significance
 - Set and read states
 - Passing data to a component through props 
 - Validation of props with propTypes
 - Using default props to supply default values to props
 - Rendering lists Using the React key prop Using the map function for iteration on arrays to generate elements

 **Working with Props and State State and its significance**
 1. **Props**
    ```javascript 
        import PropTypes from 'prop-types';
        const Heading = (props) => {
            return (
                <h1>{props.title}</h1>
            );
        };

        Heading.propTypes = {
            title: PropTypes.string.isRequired,
        };

        Heading.defaultProps = {
            title: 'Default Title',
        };
        export default Heading;
    ```
 2. **State**
    ```javascript
    import { useState } from 'react';
    const ButtonClickCount = () => {
        const [count, setCount] = useState(0);

        const handleClick = () => {
            setCount(count + 1);
        };

        return (
            <div>
                <button onClick={handleClick}>
                    Click me
                </button>
                <p>You clicked {count} times</p>
            </div>
        );
    }
    export default ButtonClickCount;

2. **Rendering lists Using the React key prop Using the map function for iteration on arrays to generate elements**
```javascript
	const List = () => {
	const headings = ['Heading 1', 'Heading 2', 'Heading 3', 'Heading 4', 'Heading 5'];
	return (
		<div>
				{headings.map((heading, index) => (<h1 key={`${index}+'app'`}>{heading}</h1>))}
		</div>
		);
	}
	export default List;
```