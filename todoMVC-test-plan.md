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
        - Clear Complited
      - ( !!!! ) enter blank when edit todo
      
* **Items left counter in each of filters separately**
    - ( !!!! ) decrement
    - ( !!!! ) unchange
    - ( !!!! ) increment
* **Button Clear completed**
    - ( !!! ) is visible as 1+ completed
    - ( !!!! ) is hidden as no completed
  
  
  
### Scenario: "Light version: TodoMVC, create, edit and delete todos in the todo list" ###

* Open https://todomvc4tasj.herokuapp.com/
* **Operations**

 * **( ! ) Create new todo** 
   * type "a." , Enter 
       + `accert "a."`
 * **( ! ) Edit todo** 
   * Double-click at the "a"
   * ( ! ) Type Delete once at the end of line  , Enter
   * type "b" , Enter
   * ( !! ) cancel edit "a" to "a to be canceled" 
     - accert "a" ,  "b"
     
* **( ! ) Complete todo** 
  * ( ! ) tap to the checkbox at the "a"
    - accert Xed out ~~"a"~~ and "b"
* **( ! ) Delete todo** 
  * ( ! ) click on the X button at the "a"
       + `accert one todo has deleted` 
  * tap to the checkbox at the left of input string
  * ( !! ) tap button Clear Complited 
      + `accert all complited todo has deleted`
  
  
### Scenario for monkeys: " FULL version TodoMVC, create, edit and delete todos in the todo list + filters and features"  ###

**Where** Given opened TodoMVC
* Open Chrome browser, newest edition
* Open https://todomvc4tasj.herokuapp.com/
  - todos page has opened
  
**Functionality**
* **Operations**

 * **( ! ) Create new todo** 
   * type "a" at input form
   * ( !!!! ) type space twice  *dot at the end of string*
   * type Enter
       + `accert todo has added`
     - accert you see ! todo "a." and "1 item left" text at the bottom  *items left increment*
 * **( ! ) Edit todo** 
   * Double-click to edit a todo
     - todo is editabling
   * ( !!!! ) Use Up , Down, Left, Right arrows on keyboard 
     - Up and Down returns indicator to start and and of the line
     - Left and Right is moves the pointer one letter forward or backward through the text
   * ( ! ) Type Delete once at the end of line  
   * ( !!!! ) Type Control + Enter 
       + `accert todo has edited`
     - accert you see ! todo "a" and "1 item left" text at the bottom  *items left unchange*
   * Double-click at the text "a" to edit a todo
   * ( !!! ) Click Tab 
     - finish of editing a todo
   * Double-click to edit a todo
   * ( !!!! ) Click out of editing form 
     - finish of editing a todo

   * ( !! ) Close tab  
   * Open https://todomvc4tasj.herokuapp.com/
       + `accert todo has saved after reopen page` 
     - accert you see ! todo "a" and "1 item left" text at the bottom *items left unchange*
   * type "b" at input form
   * type Enter
     - accert you see ! todo "a" and ! todo "b" and "2 items left" text at the bottom *items left increment*
   * ( !! ) cancel edit "a" to "a to be canceled" 
     - accert you see ! todo "a" and ! todo "b" and "2 items left" text at the bottom *items left unchange*
     
* **( ! ) Complete todo** 
  * ( ! ) tap to the checkbox at the left of "a" string   *toggle from active to completed*
    - accert you see ! Xed out todo ~~"a"~~ and ! todo "b" and "1 items left" text at the bottom *items left decrement*
  * ( !! ) tap to the checkbox at the left of input string   *toggle All from active to completed*
    - accert you see ! Xed out todo ~~"a"~~ and ! Xed out todo ~~"b"~~ and "0 items left" text at the bottom *items left decrement*
  * ( !! ) tap to the checkbox at the left of "a" string   *toggle from completed to active*
    - accert you see ! todo "a" and ! Xed out todo ~~"b"~~ and "1 item left" text at the bottom *items left increment*
  * ( !! ) tap to the checkbox at the left of input string   *toggle All from completed to active*
    - accert you see ! todo "a" and ! todo "b" and "2 items left" text at the bottom *items left increment*
  * ( !!! ) tap Completed  
       + `accert todo Filter Completed`
    - accert you see "2 items left" text at the bottom and didnt see the todos *items left unchange*
  * ( !!! ) tap Active 
       + `accert todo Filter Active` 
  * ( !!! ) tap All 
       + `accert todo Filter All`
    - accert you see ! todo "a" and ! todo "b" and "2 items left" text at the bottom *items left unchange*
* **( ! ) Delete todo** 
  * hover the cursor over the line with the text "a"
    - a X should appear on the right
  * ( ! ) click on the X to the right of the line with the text "a" 
       + `accert one todo has deleted` 
    - accert you see ! todo "b" and "1 item left" text at the bottom *items left decrement*
  * type "c" at input form
  * type Enter
       + `accert todo has added`
     - accert you see ! todo "c" and ! todo "b" and "2 items left" text at the bottom *items left increment*
  * double-click on the text "a" to edit a todo
  * ( !!!! ) delete all symbols at the string *delete a todo by deleting its text in edit mode* 
  * Click Tab or Click out of editing form or type Enter or type Control + Enter 
    - accert you see ! todo "b" and "1 item left" text at the bottom *items left decrement*
  * tap to the checkbox at the left of input string
      + `accert all todo has complited`  
  * ( !! ) tap button Clear Complited 
      + `accert all complited todo has deleted`
    - accert you see only input window and dont see any todo *items left decrement*
  
