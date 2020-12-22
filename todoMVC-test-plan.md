### A priority ###
     ( 1 ) high priority
     ( 2 ) medium priority
     ( 3 ) low priority
     ( 4 ) You can forget about this item
  
### Functional map ###
* **TodoMVC tab conditions**
    - Open
    - Reopen 
* **Filters**
    - All
    - Active
    - Completed
* **Operations with todo in each of filters separately**
    - Create 
    - Edit 
      - by use keys:  Up, Down, Left, Right, Escape, Delete, Control+Enter, Enter, Tab
      - Click out of editing form 
    - Complete 
      - checkbox at the todo 
      - checkbox Complete All near input
    - Delete 
      - by buttons Cross, Clear Complited
      - enter "" when edit
* **Items left counter in each of filters separately**
    - decrement
    - unchange
    - increment
* **Button Clear completed**
    - is visible as 1+ completed
    - is hidden as no completed
  
  
  
### Scenario: "Light version: TodoMVC, create, edit and delete todos in the todo list" ###

* Open https://todomvc4tasj.herokuapp.com/
* **Operations**

 * **( 1 ) Create new todo** 
   * type "first todo." , Enter 
       + `accert "first todo."`
 * **( 1 ) Edit todo** 
   * Double-click at the "first todo"
   * ( 1 ) Type Delete once at the end of line  , Enter
   * type "second todo" , Enter
   * ( 2 ) cancel edit "first todo" to "first todo to be canceled" 
     - accert "first todo" ,  "second todo"
     
* **( 1 ) Complete todo** 
  * ( 1 ) tap to the checkbox at the "first todo"
    - accert 1 crossed out todo ~~"first todo"~~ and 1 todo "second todo"
* **( 1 ) Delete todo** 
  * ( 1 ) click on the cross button at the "first todo"
       + `accert one todo has deleted` 
  * tap to the checkbox at the left of input string
  * ( 2 ) tap button Clear Complited 
      + `accert all complited todo has deleted`
  
  
### Scenario: " FULL version TodoMVC, create, edit and delete todos in the todo list + filters and features" ###

**Where** Given opened TodoMVC
* Open Chrome browser, newest edition
* Open https://todomvc4tasj.herokuapp.com/
  - todos page has opened
  
**Functionality**
* **Operations**

 * **( 1 ) Create new todo** 
   * type "first todo" at input form
   * ( 4 ) type space twice  *dot at the end of string*
   * type Enter
       + `accert todo has added`
     - accert you see 1 todo "first todo." and "1 item left" text at the bottom  *items left increment*
 * **( 1 ) Edit todo** 
   * Double-click to edit a todo
     - todo is editabling
   * ( 4 ) Use Up , Down, Left, Right arrows on keyboard 
     - Up and Down returns indicator to start and and of the line
     - Left and Right is moves the pointer one letter forward or backward through the text
   * ( 1 ) Type Delete once at the end of line  
   * ( 4 ) Type Control + Enter 
       + `accert todo has edited`
     - accert you see 1 todo "first todo" and "1 item left" text at the bottom  *items left unchange*
   * Double-click at the text "first todo" to edit a todo
   * ( 3 ) Click Tab 
     - finish of editing a todo
   * Double-click to edit a todo
   * ( 4 ) Click out of editing form 
     - finish of editing a todo

   * ( 2 ) Close tab  
   * Open https://todomvc4tasj.herokuapp.com/
       + `accert todo has saved after reopen page` 
     - accert you see 1 todo "first todo" and "1 item left" text at the bottom *items left unchange*
   * type "second todo" at input form
   * type Enter
     - accert you see 1 todo "first todo" and 1 todo "second todo" and "2 items left" text at the bottom *items left increment*
   * ( 2 ) cancel edit "first todo" to "first todo to be canceled" 
     - accert you see 1 todo "first todo" and 1 todo "second todo" and "2 items left" text at the bottom *items left unchange*
     
* **( 1 ) Complete todo** 
  * ( 1 ) tap to the checkbox at the left of "first todo" string   *toggle from active to completed*
    - accert you see 1 crossed out todo ~~"first todo"~~ and 1 todo "second todo" and "1 items left" text at the bottom *items left decrement*
  * ( 2 ) tap to the checkbox at the left of input string   *toggle All from active to completed*
    - accert you see 1 crossed out todo ~~"first todo"~~ and 1 crossed out todo ~~"second todo"~~ and "0 items left" text at the bottom *items left decrement*
  * ( 2 ) tap to the checkbox at the left of "first todo" string   *toggle from completed to active*
    - accert you see 1 todo "first todo" and 1 crossed out todo ~~"second todo"~~ and "1 item left" text at the bottom *items left increment*
  * ( 2 ) tap to the checkbox at the left of input string   *toggle All from completed to active*
    - accert you see 1 todo "first todo" and 1 todo "second todo" and "2 items left" text at the bottom *items left increment*
  * ( 3 ) tap Completed  
       + `accert todo Filter Completed`
    - accert you see "2 items left" text at the bottom and didnt see the todos *items left unchange*
  * ( 3 ) tap Active 
       + `accert todo Filter Active` 
  * ( 3 ) tap All 
       + `accert todo Filter All`
    - accert you see 1 todo "first todo" and 1 todo "second todo" and "2 items left" text at the bottom *items left unchange*
* **( 1 ) Delete todo** 
  * hover the cursor over the line with the text "first todo"
    - a cross should appear on the right
  * ( 1 ) click on the cross to the right of the line with the text "first todo" 
       + `accert one todo has deleted` 
    - accert you see 1 todo "second todo" and "1 item left" text at the bottom *items left decrement*
  * type "third todo" at input form
  * type Enter
       + `accert todo has added`
     - accert you see 1 todo "third todo" and 1 todo "second todo" and "2 items left" text at the bottom *items left increment*
  * double-click on the text "first todo" to edit a todo
  * ( 4 ) delete all symbols at the string *delete a todo by deleting its text in edit mode* 
  * Click Tab or Click out of editing form or type Enter or type Control + Enter 
    - accert you see 1 todo "second todo" and "1 item left" text at the bottom *items left decrement*
  * tap to the checkbox at the left of input string
      + `accert all todo has complited`  
  * ( 2 ) tap button Clear Complited 
      + `accert all complited todo has deleted`
    - accert you see only input window and dont see any todo *items left decrement*
  
