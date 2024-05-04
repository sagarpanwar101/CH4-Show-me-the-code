## Theory assignment `CH4 Show Me The Code`

### 1 Is JSX mandatory for React?
JSX is not mandatory for react. Each JSX element is just syntactic sugar for calling React.createElement(component, props, ...children). So, anything you can do with JSX can also be done with just plain JavaScript.

### 2 Is ES6 mandatory for React ? 
ES6 is also not mandatory for React, but important for it. Cos core of react is ES6 and one can 
see many things comes from pure js and we can also use them on react as well. So having knowledge of ES6 helps to understand react better.

### 3 {TitleComponent} vs {<TitleComponent/>} vs {<TitleComponent></TitleComponent>} in JSX.
`{TitleComponent}`- This describes as react component or js variable. Anything `{}` under this
behaves as the javascript.
`{<TitleComponent/>}` This describes as jsx component, its nothing but a function calling in UI we can say roughly.
`{<TitleComponent></TitleComponent>}` This is same as above component calling but with bit of HTML syntax alike closing tag.

### 4 How can I write comments in JSX? 
`{/* */}` For multi line comments
`{//}` For Single line comments

### 5 What is <React.Fragment></React.Fragment> and <></>? 
Each Jsx component can have only one parent. This is because jsx component are converted to React.creatElement(parent,prop...children) before rendering in the DOM. There can be some situation where we cant group components inside div and needs to add them inside react fragement.

The shorter syntax for fragment is `<></>` these blank tags they does the same work but doesnt 
support keys or attributes.

### 6. What is virtual DOM ?
Virtual DOM is a programming concept where a copy/virtual representation of UI is kept in memory and syced with "real" DOM by a library called "React-DOM". This process is called `Reconcilation`.
In React, a virtual DOM is associated with React elements since they are the objects representing the UI. React, however, also uses internal objects called “fibers” to hold additional information about the component tree. They may also be considered a part of “virtual DOM” implementation in React.

### 7 What is Reconciliation in react ? 
React uses diffing algorithm to diff one tree (actually dom) from another which determines what needs to be updated and only re-renders the diff.

In React, we pass props to a component, when any of the prop changes, a reconciliation process is triggered internally by react which traverses the whole component hierarchy to mark any changes required in the given component at a time.

Reconciler vs Renderer => Reconciler does the work of computing which parts of the tree have changed. Renderer uses this info to actually update the rendered app.

### 8. What is React Fiber ? 
React Fiber is the new reconciliation engine in React 16. The goal of React Fiber is to increase its suitability for areas like animation, layout, and gestures. Its headline feature is incremental rendering: the ability to split rendering work into chunks and spread it out over multiple frames.

### 9. Why do we need key in React ? When do we need keys in React ? 
A key is a special string attribute you need to include when creating lists of elements. Keys help React identify which items have changed, are added, or are removed.Keys must be used when siblings are of different elements types.

### 10.  Can we use index as key in react ?
A key is the only thing React uses to identify DOM elements. It is not recommend to use indexes for keys if the order of items may change. This can negatively impact performance and may cause issues with component state.

But, nothing is better than anything. If we don't give a key, react by default assign id of that list item as it's key.

NO key << INDEX as key <<<<<< Unique id as key from data

### 11. What are props in React ? Ways to use props ?

Props (properties) passed in Component are similar to the arguments passed in a js function call and received by that function as parameters.

Every parent component can pass some information to its child components by giving them props. Props are similar to HTML attributes, but you can pass any JavaScript value through them, including objects, arrays, and functions.

Types of Props :

Familar Props - HTML attributes like className, src, width, height passed in HTML  tag

Passing Props to Component - props are the only argument to your component. React component functions accept a single argument, a props object.

|   `Real DOM`    |   `Virtual DOM` |
|-------------|-----------------|
| DOM manipulation is very expensive  | DOM manipulation is very easy  | 
| There is too much memory wastage  | No memory wastage  |
| It updates Slow | It updates fast |
| It can directly update HTML | It can’t update HTML directly  |
|  Creates a new DOM if the element updates. | Update the JSX if the element update |
| It allows us to directly target any specific node (HTML element) | It can produce about 200,000 Virtual DOM Nodes / Second. |
| It represents the UI of your application | It is only a virtual representation of the DOM |





