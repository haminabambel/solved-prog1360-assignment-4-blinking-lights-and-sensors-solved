Download Link: https://assignmentchef.com/product/solved-prog1360-assignment-4-blinking-lights-and-sensors-solved
<br>
This assignment builds on the labs and assignments so far.

The Demonstration section of this document outlines the items you are required to show.

Tasks

You will implement a new simple game that uses the lights and accelerometer on the board.

Given the command below (where xx is your initials)

xxTilt delay target game_time

your board will turn on the light(s) according to the X and Y accelerometer values retrieved via the I2C interface. See the appropriate lab for details of retrieving these values.

When the target light has been kept on for the target time, you win, and the board flashes all lights twice (as you did in the last assignment).

If you do not manage to turn on the lights in the allotted game time (specified in seconds) you lose, and the single target light will be turned on.

Example:

jsGame 500 5 30

This would run the game with a target of light 5 being on for 500ms to win. The game will run for 30 seconds in this case before it would end with a loss

Note that you will have to find a way to time your game – in this case, busy_delay is not going to be useful for you.

<h3>Requirements</h3>

<ul>

 <li>No logic is to be implemented in your C hook code unless it is related to eliminating the busy delay.</li>

 <li>You may use library functions from the stm32 code to parse input.</li>

 <li>You will have to use the I2C functions to retrieve accelerometer values.</li>

 <li>It is very important that you structure your code cleanly for this assignment.</li>

 <li>You must name all functions and adapt any menu help instructions appropriately.</li>

 <li>You will have to determine how to count time (approximation is OK).</li>

 <li>On starting the game, ensure that all lights are first turned off.</li>

</ul>

<h2>Demonstration</h2>

Please note that you must be prepared before offering to demonstrate your code. You must demonstrate the code that you have submitted to the eConestoga dropbox.

For this assignment, you will demonstrate the following items. You may use a lab PC or your own. If needed, you may use a classmate’s VM, but you MUST run your own code and only your own code. You must demonstrate in your regularly scheduled lab period. If you demonstrate modified code, you will receive a late penalty according to how long it has been since the dropbox deadline.

<ol>

 <li>Your xx_hook.c and xx_asm.s code as taken directly from the drop box compiles.</li>

 <li>Your code deploys with sudo make program.</li>

 <li>Your code runs with no parameters provided (sensible defaults).</li>

 <li>Your code runs as specified.</li>

 <li>You can demonstrate both cases – that it is possible to both win and lose.</li>

</ol>

<h2>Code</h2>

Your code will be evaluated as follows. Each will be evaluated on a 0 to 5 basis, where 0 is unacceptable or not present, and 5 is excellent.

<h3>Functionality</h3>

Your program behaves as specified.

<h3>Proper use of Registers, the stack, and link register</h3>

Only necessary items (no more, no less) are pushed onto the stack. Your function calls use the link register appropriately.

<h3>Code Readability and Structure</h3>

Your code is properly indented, does not wrap or have long lines, and can be logically understood.

You use subroutines and memory appropriately.

<h3>Code comments</h3>

As this is assembly language, you must extensively comment any code that is unclear (i.e. nearly every line).

<h2>Document Requirements</h2>

This assignment requires a single flowchart of the flow of your code. This flowchart should use standard flowchart shapes for steps and decisions, and should correspond with your logic.

Please print the table below, with your name clearly displayed, for marking purposes.

<table>

 <tbody>

  <tr>

   <td width="312">Item</td>

   <td width="312">Grade</td>

  </tr>

  <tr>

   <td width="312">Demonstration </td>

   <td width="312">/ 5</td>

  </tr>

  <tr>

   <td width="312">Code</td>

   <td width="312"></td>

  </tr>

  <tr>

   <td width="312">Functionality</td>

   <td width="312">/ 5</td>

  </tr>

  <tr>

   <td width="312">Proper use of registers, etc.</td>

   <td width="312">/ 5</td>

  </tr>

  <tr>

   <td width="312">Readability</td>

   <td width="312">/ 5</td>

  </tr>

  <tr>

   <td width="312">Comments</td>

   <td width="312">/ 5</td>

  </tr>

  <tr>

   <td width="312">Code Subtotal </td>

   <td width="312">/ 20</td>

  </tr>

  <tr>

   <td width="312">Total </td>

   <td width="312">/ 25</td>

  </tr>

  <tr>

   <td width="312">Applicable Cap:</td>

   <td width="312"></td>

  </tr>

 </tbody>

</table>

<h3>Caps</h3>

If you do not complete all functionality, the following caps will be applied:

<table>

 <tbody>

  <tr>

   <td width="312">Function</td>

   <td width="312">Maximum Grade</td>

  </tr>

  <tr>

   <td width="312">Hard coded delays</td>

   <td width="312">60%</td>

  </tr>

  <tr>

   <td width="312">Win / Loss missing</td>

   <td width="312">80%</td>

  </tr>

  <tr>

   <td width="312">Game works but is unplayable</td>

   <td width="312">90%</td>

  </tr>

  <tr>

   <td width="312">All functions implemented</td>

   <td width="312">100%</td>

  </tr>

 </tbody>

</table>