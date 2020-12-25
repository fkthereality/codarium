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

* **Operations with todo in each of filters separately**
    - ( ! ) Create 
    - ( !! ) Edit 
      -  Escape = undo all changes
      -  Tab = confirm all changes
      -  Delete =  delete 1 symbol left
      -  Delete all string (enter blank when edit todo) = delete a todo if confirm changes
      -  Control+Enter = confirm all changes
      -  Enter = confirm all changes
      - ( !!!! ) Click out of editing form 

    - ( ! ) Complete 
      - ( ! ) one 
      - ( !!! ) All

    -( !!! ) Activate  
      - one 
      - All

    - ( ! ) Delete 
       - X 
       - Clear Completed
      

**Note: Clear completed button and left counter and filters not required according to the terms of reference**
* **( !!!! ) Items left counter in each of filters separately**
  
    - decrement
    - unchange
    - increment

* **( !!!! ) Button Clear completed**
    - is visible when  1 or more todos completed
    - is hidden when no completed todos
* **( !!! ) Filters**
    - All
    - Active
    - Completed  
  
  
### Scenario: "Light version: TodoMVC, create, edit and delete todos in the todo list" ###

* Open https://todomvc4tasj.herokuapp.com/
* **Operations**

 * **( ! ) Create new todo** 
   * Create "a" 
       + `accert "a"`
 * **( ! ) Edit todo** 
   * edit "a" to "a edited"
   * Create "b"
   * ( !! ) cancel edit ""a edited"" to "a to be canceled" 
     - accert "a edited" ,  "b"
     
* **( ! ) Complete todo** 
  * ( ! ) tap to the checkbox at the "a edited"
  * ( !! ) tap button Clear Complited 
      + `accert "b"`
* **( ! ) Delete todo** 
  * ( ! ) click on the X button at the "a edited"
       + `accert todo has deleted` 

  
