### Scenario: "TodoMVC, create, edit and delete todos in the todo list" ###

**Where** Given opened TodoMVC
* Open Chrome browser, newest edition
* Open https://todomvc4tasj.herokuapp.com/
  - todos page has opened
  
**Functionality**
* **Operations**

 * **Create new todo** ( 1 )
   * type "first todo" at input form
   * type space twice ( 4 ) *dot at the end of string*
   * type Enter
       + `accert todo has added`
     - accert you see 1 todo "first todo." and "1 item left" text at the bottom  *items left increment*
 * **Edit task** ( 1 )
   * Double-click to edit a todo
     - todo is editabling
   * Use Up , Down, Left, Right arrows on keyboard ( 4 )
     - Up and Down returns indicator to start and and of the line
     - Left and Right is moves the pointer one letter forward or backward through the text
   * Type Delete once at the end of line  ( 1 )
   * Type Control + Enter ( 4 )
       + `accert todo has edited`
     - accert you see 1 todo "first todo" and "1 item left" text at the bottom  *items left unchange*
   * Double-click at the text "first todo" to edit a todo
   * Click Tab ( 3 )
     - finish of editing a todo
   * Double-click to edit a todo
   * Click out of editing form ( 4 )
     - finish of editing a todo

   * Close tab  ( 2 )
   * Open https://todomvc4tasj.herokuapp.com/
       + `accert todo has saved after reopen page` 
     - accert you see 1 todo "first todo" and "1 item left" text at the bottom *items left unchange*
   * type "second todo" at input form
   * type Enter
     - accert you see 1 todo "first todo" and 1 todo "second todo" and "2 items left" text at the bottom *items left increment*
   * cancel edit "first todo" to "first todo to be canceled" ( 2 )
     - accert you see 1 todo "first todo" and 1 todo "second todo" and "2 items left" text at the bottom *items left unchange*
     
* **Complete task** ( 1 )
  * tap to the checkbox at the left of "first todo" string  ( 1 ) *toggle from active to completed*
    - accert you see 1 crossed out todo ~~"first todo"~~ and 1 todo "second todo" and "1 items left" text at the bottom *items left decrement*
  * tap to the checkbox at the left of input string  ( 2 ) *toggle All from active to completed*
    - accert you see 1 crossed out todo ~~"first todo"~~ and 1 crossed out todo ~~"second todo"~~ and "0 items left" text at the bottom *items left decrement*
  * tap to the checkbox at the left of "first todo" string  ( 1 ) *toggle from completed to active*
    - accert you see 1 todo "first todo" and 1 crossed out todo ~~"second todo"~~ and "1 item left" text at the bottom *items left increment*
  * tap to the checkbox at the left of input string  ( 2 ) *toggle All from completed to active*
    - accert you see 1 todo "first todo" and 1 todo "second todo" and "2 items left" text at the bottom *items left increment*
  * tap Completed  ( 3 )
       + `accert todo Filter Completed`
    - accert you see "2 items left" text at the bottom and didnt see the todos *items left unchange*
  * tap Active ( 3 )
       + `accert todo Filter Active` 
  * tap All ( 3 )
       + `accert todo Filter All`
    - accert you see 1 todo "first todo" and 1 todo "second todo" and "2 items left" text at the bottom *items left unchange*
* **Delete task** ( 1 )
  * hover the cursor over the line with the text "first todo"
    - a cross should appear on the right
  * click on the cross to the right of the line with the text "first todo" ( 1 )
       + `accert one todo has deleted` 
    - accert you see 1 todo "second todo" and "1 item left" text at the bottom *items left decrement*
  * type "third todo" at input form
  * type Enter
       + `accert todo has added`
     - accert you see 1 todo "third todo" and 1 todo "second todo" and "2 items left" text at the bottom *items left increment*
  * double-click on the text "first todo" to edit a todo
  * delete all symbols at the string *delete a todo by deleting its text in edit mode* ( 4 )
  * Click Tab or Click out of editing form or type Enter or type Control + Enter 
    - accert you see 1 todo "second todo" and "1 item left" text at the bottom *items left decrement*
  * tap to the checkbox at the left of input string
      + `accert all todo has complited`  
  * tap button Clear Complited ( 2 )
      + `accert all complited todo has deleted`
    - accert you see only input window and dont see any todo *items left decrement*
  
**A priority**
  1. high priority
  2. medium priority
  3. low priority
  4. You can forget about this item

 
