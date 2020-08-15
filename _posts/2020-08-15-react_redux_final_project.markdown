---
layout: post
title:      "React/Redux Final Project"
date:       2020-08-15 10:24:53 -0400
permalink:  react_redux_final_project
---


When I started my React/Redux project, I was beyond excited!!!  For my project, I decided to build a invesetment tracker to keep track of the items that I purchase and how much money I spent on fixing up each item.  I also created a method to let me know what my breakeven point is for each individual item.  

To start out, I built a skelaton backend in Rails.  From there, I was on my way to building the frontend with create-react-app.  As I started on the frontend, I decided to take a step back and remind myself the difference between container components, functional components, props and state.   

Here is a look at some of the notes I jotted down;


**Container Components;**
* Are class components that render other components, which can be other container components and presentational components.
* Acts as the parent to the other components and is responsible for providing data and behavior to child components
* Primarily concerned with how things work.
* Usually has other functions inside them such as callback functions and a componentDidMount
* Rarely has any html tags
* Is often stateful
* Has access to global state


Example of a Container Component;
```

class ItemsContainer extends React.Component {

    componentDidMount() {
        this.props.fetchItems()
    }


    render() {
        return (
            <div>
                <NavBar/>
                <Switch>
             
                <Route exact path='/' component={Home}/>
                <Route path='/items/new' component={ItemInput}/>
                <Route path= '/items/:id' render={(routerProps) => <Item {...routerProps} items={this.props.items}/>}/>
                <Route path='/items' render={(routerProps) => <Items {...routerProps} items={this.props.items}/>}/>
                
                </Switch>
            </div>
        )
    }
}

const mapStateToProps = state => {
    return {
        items: state.items
    }
}

export default connect(mapStateToProps, {fetchItems})(ItemsContainer)

```


**Functional Components;**
* Takes in props from the parent and does not change the state, it's stateless.
* Mainly concerned with displaying the data.
* Set up as a regular function
* Cannot call render() inside a functional component, but it must have a return().
* Has very little logic, if any at all.

Example of a Functional Component;
```
const Items = (props) => {

    return (
     
        <div>           
                <Table responsive striped hover variant="dark" size="sm">
                
                <thead>
                  <tr >
                    <th>Item Name</th>
                    <th>Purchase Price</th>
                    <th>Date Purchased</th>
                    <th>Breakeven Point</th>
                  </tr>
                </thead>
                <tbody>
                {props.items.map(item => 
                  <tr>
                    <td key={item.id}><Link to={`/items/${item.id}`}>{item.item_name}</Link></td>
                    <td> ${item.purchase_price} </td>
                    <td> {item.date_purchased} </td>
                    <td>${item.breakeven_point}</td>
                   
                  </tr>
                 )}
                </tbody>
              </Table>
        </div>
    )

}

export default Items
```


**Props**
* Are read-only
* Can NOT be changed or modified.
* For a prop to change, it's parent component must send it new props
* Props give us the ability to pass values into our components and make our app more dynamic.
* The values can be different types of data such as strings and object
*  The objects can include arrays and functions.  


**State**
* CAN be changed or modified asynchronously
* Can also be modified by using this.setState
* gets initialState
* can only be passed as props
* Changes inside the component
* Can change during the components life.
* Allows us to maintain and update data within the component without requiring its parent to send updated data.



Since this was so beneficial to me, I thought I would share my notes with you. I hope they help!

Have a great coding day!!!!
