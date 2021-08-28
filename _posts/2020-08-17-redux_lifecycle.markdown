---
layout: post
title:      "Redux  Lifecycle"
date:       2020-08-17 17:43:51 -0400
permalink:  redux_lifecycle
---

Redux is a beautiful tool that we can use to keep our state from being too spread out between different components as our app becomes bigger.  Redux allows us to store all of the necessary data in our app as a plain Javascript object called state.  The state is stored in the Redux store.  

In the index.js file;
By wrapping our app in <Provider> it is like we are making a closed circuit, similar to an electrical circuit, for our store. 

```
<Provider store={myStore}>
   <App/>
</Provider> 

```

  

The cycle;

1. STORE:  It starts in the store, which contains the state.

2. STATE: The state defines what is being rendered to the page.

3.  UI/ USER INTERFACE: When a user is interacting with a page, usually by clicking or submitting a button, it will trigger an action dispatch to an action creator.  Importing and exporting with Connect allows us to do this.  

4.  ACTIONS: The action creator makes a fetch request to the API and dispatches a "type" to the reducer.

5. REDUCER: The reducer then updates the store and the cycle starts over again. 


![](https://imgur.com/NwVo8uU)

Have a Great Coding Day!
