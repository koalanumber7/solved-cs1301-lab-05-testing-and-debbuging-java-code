Download Link: https://assignmentchef.com/product/solved-cs1301-lab-05-testing-and-debbuging-java-code
<br>
Errors can be categorized into:

<ul>

 <li>Syntax errors</li>

 <li>Logical errors</li>

 <li>Runtime errors</li>

</ul>

A syntax error occurs when your program does not comply with the syntactical rules of the Java language.  Usually, these errors are caused by misspelled words and missing punctuation, among others.  Syntax errors are relatively easy to find and correct as the compiler points out the line where the syntax error has occurred.  Runtime errors occur during the execution of a program when the program attempts to perform an invalid operation, like dividing by zero, causing the immediate termination of program’s execution.

Logical errors are errors in your program due to the design of a faulty algorithm to solve the problem at hand or in the implementation of such an algorithm.  When your application has a logical error, it might compile and run without the computer generating any error messages, but it will not work as expected.  Logical errors are generally more difficult to locate and fix than syntax errors.  The process of finding a logical or runtime error is called <strong><em>debugging</em></strong>.  An easy way to find a logical error is by tracing the value of the variables in a program while running using <strong>System.out.println(…);</strong> statements or by tracing the execution of the program step by step using a debugger.

In this lab you will learn how to monitor the value of the variables in a Java program and how to use the Eclipse debugger to locate its logical errors.

<strong>What to Submit </strong>

You should submit an error free copy of the program <strong>TemperatureConverter.java</strong>.

<h1>Instructions</h1>

Download the file <strong>TemperatureConverter.java</strong>, which contains several bugs, and the text document <strong>DebuggingWorksheet.txt</strong><strong>.   </strong>

<strong>Note: </strong>The worksheet has been provided for your convenience. Completing it might help you debug the program, but you do not need to submit it with your completed source file. <strong> </strong>

For the lab, you will test and debug the program to make it a correct, error free program.  <strong><u>Please resist</u></strong><strong> <u>the urge to try and look at the program to fix the errors.  Even if you can do that, it is not going to</u> <u>help you moving forward in this class.  Debugging skills will be critical as we move to more complex</u> <u>programming constructs</u>. </strong>

The program should allow the user to enter a temperature in Fahrenheit and display the equivalent temperature in a temperature scale of the user’s choice:  Kelvin, Rankine, Reaumur, or Celsius.  The program <em>should</em> do this. However, because of errors, it does not function properly in its current form.

The conversion from Fahrenheit to the other temperature scales is performed according to the following table:

<table width="0">

 <tbody>

  <tr>

   <td width="296"><strong>From Fahrenheit to </strong></td>

   <td width="295"><strong>Conversion Formula </strong></td>

  </tr>

  <tr>

   <td width="296">Kelvin Degrees</td>

   <td width="295">[°K] = ([°F] + 459.67) × 5/9</td>

  </tr>

  <tr>

   <td width="296">Rankine Degrees</td>

   <td width="295">[°R] = [°F] + 459.67</td>

  </tr>

  <tr>

   <td width="296">Reaumur Degrees</td>

   <td width="295">[°Re] = ([°F] – 32.0) × 4/9</td>

  </tr>

  <tr>

   <td width="296">Celsius Degrees</td>

   <td width="295">[°C] = ([°F] – 32.0) × 5/9</td>

  </tr>

 </tbody>

</table>







The program should do the following:




<ol>

 <li>Prompt the user for a valid temperature in degrees Fahrenheit.</li>

 <li>If the user enters a valid temperature in degrees Fahrenheit (i.e. <strong>temperature greater than or equal to -459.67</strong>), then the program asks the user the temperature scale to perform the conversion and displays such a conversion.</li>

</ol>




The program <strong>TemperatureConverter.java</strong> has several logical errors that you need to identify and correct using <strong>System.out.println</strong> and the <strong>Eclipse </strong>debugger.




<ol>

 <li>After you have downloaded the program <strong>java</strong> to your computer, create a new <strong>Java Project</strong> called <strong>TemperatureConverter</strong> in Eclipse, then create a new class called <strong>TemperatureConverter</strong> in the <strong>TemperatureConverter</strong> <strong>Java Project</strong>.</li>

</ol>




Using <strong>Notepad</strong>, open the file <strong>TemperatureConverter.java</strong> you have just downloaded on the desktop and copy all of its content into the class <strong>TemperatureConverter</strong> in your <strong>Eclipse </strong>project.

<ol start="2">

 <li>Add <strong>out.println</strong> statements as needed to help you understand and debug the program. After debugging, you should remove or comment out these <strong>println</strong> statements so they don’t show up in the correct version of your program.</li>

 <li>Compile and run the program.</li>

 <li>Execute the program entering the value <strong>56 </strong>at the prompt and enter 3 when prompted for the temperature scale.</li>

</ol>




o <strong>[Worksheet Item 1] What do you observe when you run the program?</strong>




<ol start="5">

 <li>One easy way to debug your program is to print to the console the values of the variables and other messages that will help you trace the execution of the program in order to find out the logical errors. However, this technique can be very time consuming if you are dealing with larger programs.  Instead, a more convenient way to locate logical errors in a program is by tracing the execution of the program and monitoring the values of the variables using a debugger.  For the rest of this lab exercise, you will learn the basics of the <strong>Eclipse </strong>debugger that will help you debug and fix logical errors in a Java program.</li>

</ol>










Afterwards, <strong>Eclipse </strong>will open several windows to help you to trace the execution of this project.




<ol start="7">

 <li>Scroll through the Java source code and set break points where it is indicated by a comment (look for “<strong>Set a breakpoint here</strong>”). To set a breakpoint, click on the left margin (in blue-grey) on the line where you want to place the breakpoint.  You will see a small dot in the margin to the left of the line.</li>

 <li>After you have set the indicated breakpoints in the program, click on the tab <strong>Breakpoints</strong>.</li>

</ol>




<ul>

 <li><strong>[Worksheet Item 2] Where (what line numbers) have you set the breakpoints? </strong></li>

</ul>




<ol start="9">

 <li>Run the program in <strong>Debug </strong>mode by clicking the little bug in the toolbar , or <strong>Run</strong>/<strong>Debug </strong>in the menu bar. Click <strong>OK </strong>on the window <strong><u>Save and Launch</u></strong>.</li>

</ol>













<ol start="10">

 <li>Click on the <strong>Variables </strong>window tab,, it should be located in the top right window.</li>

</ol>




<ul>

 <li><strong>[Worksheet Item 3] What is the value of the named constant </strong><strong>MIN_FAHRENHEIT</strong><strong> and the variable </strong><strong>tempScaleStr</strong><strong> displayed in the Variables window? </strong></li>

</ul>

<ol start="11">

 <li>The debugger will stop on the first breakpoint you set. Observe that the debugger highlights the line of code that will execute next.</li>

</ol>




Now, click on the <strong>Step Over </strong>icon, , in the toolbar to execute the statement

<strong>fahrenheit = keyboard.nextDouble(); </strong>

Click on the <strong>Console </strong>window, then enter <strong>56 </strong>and hit enter.   Afterwards, do the following:

<ol>

 <li>a) Click on the <strong>Step Over </strong>icon, , several times to see what happens and answer the following questions in the Debugging worksheet:</li>

</ol>




<ul>

 <li><strong>[Worksheet Item 4a] Does the first </strong><strong>if</strong><strong> statement display the error message correctly? </strong>o <strong>[Worksheet Item 4b] What is the problem?  </strong></li>

 <li><strong>[Worksheet Item 4c] How would you fix the program so it terminates when the user enters a Fahrenheit temperature less than the possible minimum temperature? </strong></li>

</ul>

<strong> </strong>

<ol>

 <li>b) Terminate the current execution of the program by clicking on the</li>

</ol>




<strong>Terminate </strong>icon, , in the toolbar or to the right of the <strong>Console </strong>Window.

<strong> </strong>

<ol start="12">

 <li><strong><u>Modify the first if statement so it works correctly. </u></strong><strong> </strong></li>

 <li>Run the program in <strong>Debug </strong>mode again by clicking the little bug in the toolbar, or <strong>Run/Debug</strong> in the menu bar. When you reach the <strong>first and second breakpoints</strong>, use</li>

</ol>

<strong>Step Over </strong>icon, , to be sure that the first if statement works properly.  If you have modified this if statement correctly you will notice that the next statement to be executed is the prompt that asks the user to enter a temperature scale:




<ol start="15">

 <li>Now, click on <strong>Step Over, </strong><strong>, </strong>in the toolbar.</li>

</ol>




o <strong>[Worksheet Item 5a] Is the condition of the second </strong><strong>if</strong><strong> statement correct?  </strong>o <strong>[Worksheet Item 5b] How will you change it?  </strong>

<ol start="16">

 <li>Terminate the current execution of the program (click on the <strong>Terminate </strong>icon, , in the toolbar or to the right of the <strong>Console </strong>window). Then, do the following:

  <ol>

   <li>Remove the first breakpoint you set by clicking on the dot in the margin on the left.</li>

   <li>Remove the breakpoint you set on the first if statement.</li>

   <li>Modify the condition of the second if statement properly.</li>

   <li>Run the program again in Debug mode (click on the little bug in the toolbar), or click</li>

  </ol></li>

</ol>

<strong>Run</strong>/<strong>Debug </strong>in the menu bar.  Then click on <strong>Step Over, </strong><strong>,</strong> or the <strong>Resume </strong>button, , in the toolbar to trace the execution of your program until it reaches the statement:

<strong>convertedDegrees = fahrenheit – 32* 4/9 ; </strong>




<ol start="17">

 <li>We are going to monitor the value of the following two expressions:

  <ul>

   <li><strong>fahrenheit – 32 </strong></li>

   <li><strong>fahrenheit – 32* 4/9 </strong></li>

  </ul></li>

</ol>

To do so, select the expression, then right click and click on <strong>Watch. </strong>A window called <strong>Expressions </strong>will open up.

o <strong> [Worksheet Item 6] What is the value of the expression just selected in the Watch window?  </strong>




<ol start="18">

 <li>Click on the <strong>Resume </strong>button, , in the toolbar.</li>

</ol>

o <strong>[Worksheet Item 7a] Does the program compute the correct temperature in Reaumur degrees? </strong>

<strong>(Check if multiplying the 1st expression by 4/9 gives you the value of the 2nd expression.  </strong>o <strong>[Worksheet Item 7b] Does the program assign the correct value </strong><strong>fortempScaleStr</strong><strong>?  </strong>o <strong>[Worksheet Item 7c] How can you modify the program to compute the value properly? </strong>

<ol start="19">

 <li>Fix the body of the if statement that computes the Reaumur temperature properly.</li>

 <li>There are other logical errors, use the debugger to fix them. Then, compile, run, and test the program until you are sure the program is error free and works correctly to convert any valid temperature in Fahrenheit to an equivalent temperature when the scale chosen by the user is valid.</li>

</ol>

<h1>Additional Requirements</h1>

These are things that make the graders lives easier, and ultimately, you will see in the real world as well. Remember the teaching staff does not want to touch your code after they gave you requirements; they want to see the perfect results they asked for! Here is a checklist of things you can<strong> lose points</strong> for:





