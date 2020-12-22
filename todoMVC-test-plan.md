### Functional map ###
* **( 1 ) TodoMVC tab conditions**
    - ( 1 ) Open
    - ( 2 ) Reopen 
* **( 3 ) Filters**
    - ( 3 ) All
    - ( 3 ) Active
    - ( 3 ) Completed
* **( 1 ) Operations with todo in each of filters separately**
    - ( 1 ) Create 
    - ( 2 ) Edit 
      - ( 3 ) by use keys:  Up, Down, Left, Right, Escape, Delete, Control+Enter, Enter, Tab
      - ( 4 ) Click out of editing form 
    - ( 1 ) Complete 
      - ( 1 ) checkbox V 
      - ( 3 ) checkbox Complete All
    - ( 1 ) Delete 
      - ( 1 ) by buttons Cross, Clear Complited
      - ( 4 ) enter "" when edit todo
* **( 3 ) Items left counter in each of filters separately**
    - ( 4 ) decrement
    - ( 4 ) unchange
    - ( 4 ) increment
* **( 3 ) Button Clear completed**
    - ( 3 ) is visible as 1+ completed
    - ( 4 ) is hidden as no completed
  
  
  
### Scenario: "Light version: TodoMVC, create, edit and delete todos in the todo list" ###

* Open https://todomvc4tasj.herokuapp.com/
* **Operations**

 * **( 1 ) Create new todo** 
   * type "a." , Enter 
       + `accert "a."`
 * **( 1 ) Edit todo** 
   * Double-click at the "a"
   * ( 1 ) Type Delete once at the end of line  , Enter
   * type "b" , Enter
   * ( 2 ) cancel edit "a" to "a to be canceled" 
     - accert "a" ,  "b"
     
* **( 1 ) Complete todo** 
  * ( 1 ) tap to the checkbox at the "a"
    - accert crossed out ~~"a"~~ and "b"
* **( 1 ) Delete todo** 
  * ( 1 ) click on the cross button at the "a"
       + `accert one todo has deleted` 
  * tap to the checkbox at the left of input string
  * ( 2 ) tap button Clear Complited 
      + `accert all complited todo has deleted`
  
  
### Scenario for monkeys: " FULL version TodoMVC, create, edit and delete todos in the todo list + filters and features"  ###

**Where** Given opened TodoMVC
* Open Chrome browser, newest edition
* Open https://todomvc4tasj.herokuapp.com/
  - todos page has opened
  
**Functionality**
* **Operations**

 * **( 1 ) Create new todo** 
   * type "a" at input form
   * ( 4 ) type space twice  *dot at the end of string*
   * type Enter
       + `accert todo has added`
     - accert you see 1 todo "a." and "1 item left" text at the bottom  *items left increment*
 * **( 1 ) Edit todo** 
   * Double-click to edit a todo
     - todo is editabling
   * ( 4 ) Use Up , Down, Left, Right arrows on keyboard 
     - Up and Down returns indicator to start and and of the line
     - Left and Right is moves the pointer one letter forward or backward through the text
   * ( 1 ) Type Delete once at the end of line  
   * ( 4 ) Type Control + Enter 
       + `accert todo has edited`
     - accert you see 1 todo "a" and "1 item left" text at the bottom  *items left unchange*
   * Double-click at the text "a" to edit a todo
   * ( 3 ) Click Tab 
     - finish of editing a todo
   * Double-click to edit a todo
   * ( 4 ) Click out of editing form 
     - finish of editing a todo

   * ( 2 ) Close tab  
   * Open https://todomvc4tasj.herokuapp.com/
       + `accert todo has saved after reopen page` 
     - accert you see 1 todo "a" and "1 item left" text at the bottom *items left unchange*
   * type "b" at input form
   * type Enter
     - accert you see 1 todo "a" and 1 todo "b" and "2 items left" text at the bottom *items left increment*
   * ( 2 ) cancel edit "a" to "a to be canceled" 
     - accert you see 1 todo "a" and 1 todo "b" and "2 items left" text at the bottom *items left unchange*
     
* **( 1 ) Complete todo** 
  * ( 1 ) tap to the checkbox at the left of "a" string   *toggle from active to completed*
    - accert you see 1 crossed out todo ~~"a"~~ and 1 todo "b" and "1 items left" text at the bottom *items left decrement*
  * ( 2 ) tap to the checkbox at the left of input string   *toggle All from active to completed*
    - accert you see 1 crossed out todo ~~"a"~~ and 1 crossed out todo ~~"b"~~ and "0 items left" text at the bottom *items left decrement*
  * ( 2 ) tap to the checkbox at the left of "a" string   *toggle from completed to active*
    - accert you see 1 todo "a" and 1 crossed out todo ~~"b"~~ and "1 item left" text at the bottom *items left increment*
  * ( 2 ) tap to the checkbox at the left of input string   *toggle All from completed to active*
    - accert you see 1 todo "a" and 1 todo "b" and "2 items left" text at the bottom *items left increment*
  * ( 3 ) tap Completed  
       + `accert todo Filter Completed`
    - accert you see "2 items left" text at the bottom and didnt see the todos *items left unchange*
  * ( 3 ) tap Active 
       + `accert todo Filter Active` 
  * ( 3 ) tap All 
       + `accert todo Filter All`
    - accert you see 1 todo "a" and 1 todo "b" and "2 items left" text at the bottom *items left unchange*
* **( 1 ) Delete todo** 
  * hover the cursor over the line with the text "a"
    - a cross should appear on the right
  * ( 1 ) click on the cross to the right of the line with the text "a" 
       + `accert one todo has deleted` 
    - accert you see 1 todo "b" and "1 item left" text at the bottom *items left decrement*
  * type "c" at input form
  * type Enter
       + `accert todo has added`
     - accert you see 1 todo "c" and 1 todo "b" and "2 items left" text at the bottom *items left increment*
  * double-click on the text "a" to edit a todo
  * ( 4 ) delete all symbols at the string *delete a todo by deleting its text in edit mode* 
  * Click Tab or Click out of editing form or type Enter or type Control + Enter 
    - accert you see 1 todo "b" and "1 item left" text at the bottom *items left decrement*
  * tap to the checkbox at the left of input string
      + `accert all todo has complited`  
  * ( 2 ) tap button Clear Complited 
      + `accert all complited todo has deleted`
    - accert you see only input window and dont see any todo *items left decrement*
  
