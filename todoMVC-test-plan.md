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
      - undo all changes:    
          -  Escape 
      - confirm all changes:
          -  Tab
          -  Control+Enter
          -  Enter
          -  Click outside of editing form 

    - ( ! ) Complete 
      - ( ! ) one 
      - ( !!! ) All

    - ( !!! ) Activate  
      - one 
      - All

    - ( ! ) Delete 
       - X 
       - Clear Completed
       - Edit to blank


**Note: Clear completed button, items left counter and filters are not required according to the terms of reference**
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
  
  
### Scenario: 'TodoMVC - basic functionality' ###

* Open https://todomvc4tasj.herokuapp.com/

 * **Create new todo** 
   * create 'a', 'b'
     + `assert list: 'a', 'b'`
     
 * **Edit todo** 
   * edit 'a' to 'a edited'
   * cancel edit 'a edited' to 'a to be canceled' 
     + `assert list: 'a edited' ,  'b'`
     
* **Complete todo** 
  * complete 'a edited'
  * Clear Complited 
      + `assert list: 'b'`
      
* **Delete todo** 
  * delete 'b'
       + `assert list: empty` 
