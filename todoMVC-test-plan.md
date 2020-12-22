**Where** 
* Open Chrome browser, newest edition
* Open https://todomvc4tasj.herokuapp.com/
  - todos page has opened
  
**Functionality**
* **Operations**

 * **Create new todo** ( 1 )
   * type "first todo" at input form
   * type space twice ( 4 ) *dot at the end of string*
   * type Enter
       + `todo has added`
     - you see 1 todo "first todo."
 * **Edit task** ( 1 )
   * Double-click to edit a todo
     - todo is editabling
   * Use Up , Down, Left, Right arrows on keyboard ( 4 )
     - Up and Down returns indicator to start and and of the line
     - Left and Right is moves the pointer one letter forward or backward through the text
   * Type Delete once at the end of line  ( 1 )
   * Type Control + Enter ( 4 )
       + `todo has edited`
     - you see 1 todo "first todo"
   * Double-click at the text "first todo" to edit a todo
   * Click Tab ( 3 )
     - finish of editing a todo
   * Double-click to edit a todo
   * Click out of editing form ( 4 )
     - finish of editing a todo

   * Close tab  ( 2 )
   * Open https://todomvc4tasj.herokuapp.com/
       + `todo has saved after reopen page` 
     - you see 1 todo "first todo" and "1 item left" text at the bottom
   * type "second todo" at input form
   * type Enter
     - you see 1 todo "first todo" and 1 todo "second todo" and "2 items left" text at the bottom
* **Complete task** ( 1 )
  * tap to the checkbox at the left of "first todo" string  ( 1 ) *toggle from active to completed*
    - you see 1 crossed out todo ~~"first todo"~~ and 1 todo "second todo" and "1 items left" text at the bottom
  * tap to the checkbox at the left of input string  ( 2 ) *toggle All from active to completed*
    - you see 1 crossed out todo ~~"first todo"~~ and 1 crossed out todo ~~"second todo"~~ and "0 items left" text at the bottom
  * tap to the checkbox at the left of "first todo" string  ( 1 ) *toggle from completed to active*
    - you see 1 todo "first todo" and 1 crossed out todo ~~"second todo"~~ and "1 item left" text at the bottom
  * tap to the checkbox at the left of input string  ( 2 ) *toggle All from completed to active*
    - you see 1 todo "first todo" and 1 todo "second todo" and "2 items left" text at the bottom
  * tap Completed  ( 3 )
       + `todo Filter Completed`
    - you see "2 items left" text at the bottom and didnt see the todos
  * tap Active ( 3 )
       + `todo Filter Active` 
  * tap All ( 3 )
       + `todo Filter All`
    - you see 1 todo "first todo" and 1 todo "second todo" and "2 items left" text at the bottom
* **Delete task** ( 1 )
  * hover the cursor over the line with the text "first todo"
    - a cross should appear on the right
  * click on the cross to the right of the line with the text "first todo" ( 1 )
       + `one todo has deleted` 
    - you see 1 todo "second todo" and "1 item left" text at the bottom
  * type "third todo" at input form
  * type Enter
       + `todo has added`
     - you see 1 todo "third todo" and 1 todo "second todo" and "2 items left" text at the bottom
  * double-click on the text "first todo" to edit a todo
  * delete all symbols at the string *delete a todo by deleting its text in edit mode* ( 4 )
  * Click Tab or Click out of editing form or type Enter or type Control + Enter 
    - you see 1 todo "second todo" and "1 item left" text at the bottom
  * tap to the checkbox at the left of input string
      + `all todo has complited`  
  * tap button Clear Complited ( 2 )
      + `all complited todo has deleted`
    - you see only input window and dont see any todo
  
**A priority**
  1. high priority
  2. medium priority
  3. low priority
  4. You can forget about this item

 
