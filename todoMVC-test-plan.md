**Where** 
* Open Chrome browser, newest edition
* Open https://todomvc4tasj.herokuapp.com/
  - todos page has opened
  
**Functionality**
* **Operations**

 * **Create new todo** ( 1 )
   * type "фывафывафы" at input form
   * type space twice
   * type Enter
      + `todo has added`
     - you see 1 todo "фывафывафы."
 * **Edit task** ( 1 )
   * Double-click to edit a todo
     - todo is editabling
   * Use Up , Down, Left, Right arrows on keyboard ( 4 )
     - Up and Down returns indicator to start and and of the line
     - Left and Right is moves the pointer one letter forward or backward through the text
   * Type Delete at the end of line  ( 1 )
   * Type Control + Enter ( 4 )
      + `todo has edited`
     - you see 1 todo "фывафывафы"
   * Double-click to edit a todo
   * Click Tab
     - finish of editing a todo
   * Double-click to edit a todo
   * Click out of editing form
     - finish of editing a todo

   * Close tab  ( 2 )
   * Open https://todomvc4tasj.herokuapp.com/
      + `todo has saved after reopen page` 
     - you see 1 todo "фывафывафы" and "1 item left" text at the bottom
   * type "2t" at input form
   * type Enter
     - you see 1 todo "фывафывафы" and 1 todo "2t" and "2 items left" text at the bottom
* **Complete task** ( 1 )
  * tap to the checkbox at the left of "фывафывафы" string  ( 1 ) *toggle from active to completed*
    - you see 1 crossed out todo ~~"фывафывафы"~~ and 1 todo "2t" and "1 items left" text at the bottom
  * tap to the checkbox at the left of input string  ( 2 ) *toggle from active to completed*
    - you see 1 crossed out todo ~~"фывафывафы"~~ and 1 crossed out todo ~~"2t"~~ and "0 items left" text at the bottom
  * tap to the checkbox at the left of "фывафывафы" string  ( 1 ) *toggle from completed to active*
    - you see 1 todo "фывафывафы" and 1 crossed out todo ~~"2t"~~ and "1 item left" text at the bottom
  * tap to the checkbox at the left of input string  ( 2 ) *toggle from completed to active*
    - you see 1 todo "фывафывафы" and 1 todo "2t" and "2 items left" text at the bottom
  * tap Completed  ( 3 )
      + `todo Filter Completed`
    - you see "2 items left" text at the bottom and didnt see the todos
  * tap Active ( 3 )
      + `todo Filter Active` 
  * tap All ( 3 )
      + `todo Filter All`
    - you see 1 todo "фывафывафы" and 1 todo "2t" and "2 items left" text at the bottom
* **Delete task** ( 1 )
  * hover the cursor over the line with the text "фывафывафы"
    - a cross should appear on the right
  * click on the cross to the right of the line with the text "фывафывафы"
      + `one todo has deleted` 
    - you see 1 todo "2t" and "1 item left" text at the bottom
  * tap to the checkbox at the left of input string
      + `all todo has complited` 
  * tap button Clear Complited
      + `all complited todo has deleted`
    - you see only input window and dont see any todo
  
**A priority**
  1. high priority
  2. medium priority
  3. low priority
  4. You can forget about this item

 
