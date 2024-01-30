# NP HTML5, CSS3, and JavaScript 6e Tutorial 11, Case Problem 2

## Description
1.  Use your editor to open the mt_calc_txt.html and mt_calc_txt.js files from the html11 > case2 folder. Enter your name and the date in the comment section of each file, and save them as mt_ calc.html and mt_calc.js respectively.
2.  Go to the mt_calc.html file in your editor. In the head section, create a link to the mt_calc.css style sheet. Add a script element for the mt_calc.js file, loading the file asynchronously. Take some time to study the contents of the HTML file noting the element IDs and attributes and then save your changes to the file.
3.  Return to the mt_calc.js file in your editor. Directly below the initial comment section, insert a command that runs the init() function when the page is loaded by the browser.
4.  Create the init() function, which sets up the event handlers for the page. Within the init() func¬tion, add the following commands:
    a.  Declare the calcButtons variable containing the collection of page elements belonging to the calcButton class.
    b.  Loop through the calcButtons object collection and, for each button in that collection, run the buttonClick() function in response to the click event.
    c.  After the for loop, add a command that runs the calcKeys() function in response to the key- down event occurring within the element with the ID "calcWindow".
5.  Create the buttonClick() function. The purpose of this function is to change what appears in the calculator window when the user clicks the calculator buttons. Add the following commands to the function:
    a.  Declare the calcvalue variable equal to the value attribute of the calcWindow text area box.
    b.  Declare the calcDecimal variable equal to the value attribute of the decimals input box.
    c.  Each calculator button has a value attribute that defines what should be done with that button. Declare the buttonvalue attribute equal to the value attribute of the event object target.
    d.  Create a switch-case structure for the following possible values of the buttonValue variable:
    i.  For "del", delete the contents of the calculate window by changing calcValue to an empty text string.
    ii.  For "bksp", erase the last character in the calculator window by changing calcValue to the value returned by the eraseChar() function using calcValue as the parameter value.
    iii.  For "enter", calculate the value of the current expression by changing calcValue to: " = " + evalEq(calcValue, calcDecimal) + "\n" Note that \n is used to add a line return at the end of the answer.
    iv.  For "prev", copy the last equation in the calculator window by changing calcValue to the value returned by the lastEq() function using calcValue as the parameter value.
    v.  Otherwise, append the calculator button character to the calculator window by letting, calcValue equal calcValue plus buttonValue.
    e.  After the switch-case structure, set the value attribute of the calcWindow text area box to calcValue.
    f.  Run the command document.getElementByld("calcWindow").focus() to put the cursor focus within the calculator window.
6. Next, you will control the keyboard actions within the calculator window. Theresa wants you to program the actions that will happen when the user presses the Delete, Enter, and up arrow keys. Add the calcKeys() function containing the following commands:
   a.  As you did in the buttonClick() function, declare the calcvalue and calcDecimal variables.
   b.  Create a switch-case structure for different values of the key attribute of the event object as follows:
   i.  For "Delete", erase the contents of the calculator window by changing calcValue to an empty text string.
   ii.  For "Enter", add the following expression to calcValue: + evalEq(calcValue, calcDecimal)
   iii. For "ArrowUp", add the following expression to calcValue lastEq(calcWindow.value)
   iv. And then enter a command that prevents the browser from performing the default action in response to the user pressing the up-arrow key. c. After the switch-case structure, set the value attribute of the calcWindow text area box to calcValue.
7.  Document your work by commenting your program commands and then save your changes to the file
8.  Open the mt_calc.html file in your browser. Click the different calculator buttons and verify that you can enter a mathematical expression into the calculator and evaluate that expression by clicking the enter button. Verify that you can erase the last character by clicking the bksp button. Verify that you can copy the last expression by clicking the enter button followed by the prev button. Show that you can clear the contents of the calculator window by clicking the del button. Finally verify that you can change the number of decimal places in the answer by changing the value in the dec input box.
9.  Click within the calculator window and, using the keyboard, directly type a mathematical expression. Verify that pressing the Enter key evaluates the current expression and moves the cursor to a new line. Show that you can copy the previous expression by pressing the Enter key followed by the up-arrow key on your keyboard. Finally verify that pressing the Delete key clears the contents of the calculator window. Note: Keyboard commands might not work in the Safari browser since Safari does not support the key property at the time of this writing.


