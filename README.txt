Names: Sydney Taylor, Kenton Carrier
Url: http://www.cs.uky.edu/~spta224/CS316/P2/Supercalifragilisticexpialidocious.html
Description: This program creates a simple matching game using JavaScript. The program 
asks for the names of the two players and an even number between 4 and 10 to produce 
the gameboard. The program generates a NxN boardgame where N is the number entered 
by the user and displays the players names. The players take turns choosing two game 
pieces. The game pieces are combinations of a color as the background and a number from 
1-4 as the text. When a player makes a match, the game disables those tiles and adds a 
point to that player's score. That player would then choose again. If the player does 
not make a match, they flip the tiles back over and it becomes the other player's turn.
Players can concede the game at any time and at the end of the game, the program will 
display which player won.   

We used Bulma for styling purposes (https://bulma.io/) through their provided CDN
CDN link used for Bulma styling framework:
https://cdnjs.cloudflare.com/ajax/libs/bulma/0.7.5/css/bulma.min.css

Q1) Why in the writeup did I say it doesn't really mean anything that this project needs
to run on the www.cs.uky.edu server?

    There is no CGI in this project. As per the slides, HTML + JavaScript is dynamic content 
provided by the browser, not the server.

Q2) Give a reason why I told you to pick a random name for your file. Think, why THIS time
when I am usually very strict about what you name files?

    To make it so other people can't find the page without us giving them the exact URL. 
There is no CGI and the JavaScript is embedded in the HTML, meaning if someone found the page 
they could easily view the source code and see the entire project. If other students found 
the page, they could copy our source code, which is the exact reason we received screenshots 
of the sample game rather than the URL from the professor.

Q3) What datastructure (simple or complex) did you choose to use to store the game pieces
and their location? Why did you choose that datastructure?

    We used a one dimensional array, because if you know what the size of the array (gameboard) 
is, you can access any position in the array by providing the row and column number. In our 
opinion, this makes it more efficient and easier to work with than other options (such as a 
two dimensional array).

Q4) Does your program accept mouse clicks on areas that are not (or should not be) active?
If so, what does your program do in those events? If not, what did you do to prevent those
mouseclicks from triggering code? Be specific!

    Our program does not accept mouse clicks on areas that should not be active. We did this 
by removing the OnClick event from tiles that should not be active and added it back when it 
should be active. We also removed the end turn and reset game button from the document whenever 
it shouldn't be active and added it back whenever it should be active.
