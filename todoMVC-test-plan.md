[Github](https://github.com/fkthereality/codarium/blob/ToDoMVC/todoMVC-test-plan.md)
### A priority ###
     ( ! ) high priority
     ( !! ) medium priority
     ( !!! ) low priority
     ( !!!! ) You can forget about this item

### Functional map ###
* **TodoMVC tab conditions**
    - ( ! ) Open
    - ( !! ) Reopen
    - ( !! ) Restart browser
* **( !!! ) Filters**
    - All
    - Active
    - Completed
* **Operations with todo in each of filters separately**
    - ( ! ) Create 
    - ( !! ) Edit 
      - ( !!! ) by use keys:  
      -  Up = go to start of string
      -  Down = go to end of string
      -  Left = go to 1 symbol left
      -  Right = go to 1 symbol right
      -  Escape = undo all changes
      -  Tab = confirm all changes
      -  Delete =  delete 1 symbol left
      -  Delete all string = delete a todo if confirm changes
      -  Control+Enter = confirm all changes
      -  Enter = confirm all changes

      
      - ( !!!! ) Click out of editing form 
    - ( ! ) Complete 
      - ( ! ) one (single) 
      - ( !!! ) Complete All

    - ( ! ) Delete 
      - ( ! ) by buttons: 
        - X 
        - Clear Completed
      - ( !!!! ) enter blank when edit todo

**Note: Clear completed button and left counter not required according to the terms of reference**
* **Items left counter in each of filters separately**
  
    - ( !!!! ) decrement
    - ( !!!! ) unchange
    - ( !!!! ) increment

* **Button Clear completed**
    - ( !!! ) is visible when  1 or more todos completed
    - ( !!!! ) is hidden when no completed todos
  
  
  
### Scenario: "Light version: TodoMVC, create, edit and delete todos in the todo list" ###

* Open https://todomvc4tasj.herokuapp.com/
* **Operations**

 * **( ! ) Create new todo** 
   * type "a." , Enter 
       + `accert "a."`
 * **( ! ) Edit todo** 
   * Double-click at the "a."
   * ( ! ) Type Delete once at the end of line  , Enter
   * type "b" , Enter
   * ( !! ) cancel edit "a" to "a to be canceled" 
     - accert "a" ,  "b"
     
* **( ! ) Complete todo** 
  * ( ! ) tap to the checkbox at the "a"
    - accert crossed out ~~"a"~~ and "b"
* **( ! ) Delete todo** 
  * ( ! ) click on the X button at the "a"
       + `accert one todo has deleted` 
  * tap to the checkbox at the left of input string
  * ( !! ) tap button Clear Complited 
      + `accert all complited todo has deleted`
