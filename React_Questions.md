
## Q: What is React?

ReactJS is an open-source front-end JavaScript library that is used for building reusable user interfaces, for single-page applications.
made by facebook and fortune500 companies are used it.

---

## Q: What are the major features of React?

- Uses JSX syntax, Its allows developers to write HTML in their JS code.
- It uses Virtual DOM instead of Real DOM considering that Real DOM manipulations are expensive.
- Follows Unidirectional or one-way data flow or data binding.
- It has component based architecture

`(extra question: does react supports SSR? => YES it does , read more about it by your own)`

---

## Q: What is JSX?

* JSX stands for JavaScript XML (html + js)
* jsx not understand by browser, browser only understand js 
* jsx convert to js by using bebel 
* babel is a javascript compiler

---

## Q: Explain Bundler?

* Bundling is the process of following imported files and merging them into a single file is called “bundle”. 
* saari files ko eki structure mein kr rke ek file bnane ka kaam --> bundler
* Eg .  webpacks, vite , percel  ===> to manage files --> sari files ko bundle krta hai
* babel comes with bundler

---


## Q: Explain Components?

There are 2 types of Components

* Class-based Component :  --> used for dynamic changes --> stateful
* functional Component : --> used for static changes --> stateless

---


## Q: Which to use a Class Component or a Function Component?

After the addition of Hooks, it is always recommended to use Function components over Class components in React
<br>
As you can make dynamic changes with the help of hooks with Function components and the lifecycle method as also covered in useEffect

---

## Q: Which to use a functional Component over class Component?

* functional component have high readability as compare to class component
* It has less boiler-plate code
* No this keyword binding
* Reuseability
* High performance
  
---

## Q: What are Pure Components?

Pure components are the components which render the same output for the same state and props. In function components, you can achieve these pure components through memoized React.memo()

---

## Q: What is state in React?

States are just like variables in a component which can change themselves throughout the journey using hooks `(useState)`

---

## Q: What are props in React?

it is just an argument which is used to transfering the data from one component  to another component

---

## Q: What is the difference between state and props?

`states` -> They are <ins>mutable</ins> (can be changed)
`props` -> They are <ins>immutable</ins> (cant be changed)

---

## Q: What is "key" prop and what is the benefit of using it in arrays of elements?

A key is a special attribute you should include when mapping over arrays to render data. `Key prop helps React identify which items have changed, are added, or are removed.`

⚠️ <ins>Keys should be unique among its siblings</ins>

---

## Q: What is Virtual DOM?

The Virtual DOM is an in-memory representation of Real DOM (similar to DOM but sort of imaginary). The representation of a UI is kept in memory and synced with the `real DOM`.
<br>
It's a step that happens between the render function being called and the displaying of elements on the screen. This entire process is known as <b>`Reconciliation`</b>.

### **NUTSHELL**

⚠️ Reconciliation in React refers to the process of comparing the virtual representation of a component’s UI (Virtual DOM) with the actual DOM and determining if and how the real DOM should be updated to match the virtual representation.



---

**`Reconciliation`** : It is a algorithm uses by react to differentiate between two tress {} to determine which part to be changed
	two tress --> 1 . Browser dom wala treee 
		            2.  ek virtual dom wala tree jo create root se bnta hai


**`React Fibre`** : It is the implementation of core algorithm which is basically happening behind the scene of virtual DOM.

**`Hydration`**: The concept when the layout has arrived and the JS is yet to be injected in the layout for eg if you have a button and clicking on the button will lead to some functionality then sometimes what happens is that the button is non-clickable for the moment till JS arrives the layout.

---

## Q: What are controlled components?

A component that controls the input elements within the forms, i.e, every state change will have an handler function. That means, the displayed data is always in sync with the state of the component.

---

## Q: What are Higher-Order Components?

A higher-order component (HOC) is a function that takes a component and returns a new component.

---

## Q: What are fragments?

It's a common pattern or practice in React for a component to return multiple elements. Fragments let you group a list of children without adding extra nodes to the DOM.

---


## Q: What are the limitations of React?

- React is just a view library, not a full framework.

- Integrating React into a traditional MVC framework requires some additional configuration.

- The code complexity increases with inline templating and JSX.

- Too many smaller components leading to over engineering or boilerplate.

- Poor SEO

- unidirection problem create krega (loop hole)

- no self routing

---

## Q: What is the difference between React and ReactDOM?

**`React`** -> Used for creating the elements
<br>
**`ReactDOM`** -> Used for displaying the elements

---
---

## Hooks

### useStates 

* It is used to manage the state. Its accept one value and return array of two things [state  , fxn ]. It observe it if states are change then it rerender that component
* fxn is used to update the state.


### useEffect 
* It is used to run side effects (like data fetching, api calling)
* It accept a callback fxn and a dependency array .  useEffect(callback fxn , dependency array)
* callback function never be asynchornus
* if dependency array diya hi nhi toh kuch bhi change hoga toh component rerender hoga ,  agar dependency array toh diya hai but khali hai toh component Runs only on the first render. baki runs any time any dependency value changes
* it returns a cleanup fxn  {timer wala code yaad kro }

### useRef

* It is useful for accessing or focusing elements.
* It Doesn't trigger re-renders.

### memo
* agar kisi fxnn ya component ko memo se wrap kr diya toh wo component tabhi rerender hoga jbb uske props mein changes honge

### useMemo
* It is use to memoize the value 
* It Only recalculates if dependencies change.

### useCallback
* Memoizes functions to prevent unnecessary re-renders.




### Extras 

* empty <></>  is also called fragment
* return hmesha ek hi parent  kyu ki  single parents taki "reconsilation" faster ho
* component ka name always be capital letter
* component app.jsx mein import kr ke call krna hota hai
* component call is self closing tags
* <App/> --> self closing tag && or we can say component calling
* * when we use or call a component inside a component is called `component composition`

### Extras

* boolean value display nhi hoti
	let a= true;
	return (
		<p>{a}</p>
		<p>(JSON.stringify(a))</p>

* null struingyfy mein show hoga
* undefined khi bhi show nhi hoga
* obj direct  nhi display hota
* * obj.a display
* *  stringyfy obj  chlta hai
* *  obj.keys
* *  obj.values
* *  obj.entries
---

* lazy loading
* propdrilling
* context api
