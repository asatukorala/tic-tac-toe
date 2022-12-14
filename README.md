# Tic Tac Toe

# :computer: [Click here](https://asatukorala.github.io/tic-tac-toe/) to see my live project!

# :information_source: About 
- An online Tic-Tac-Toe game. Click the URL above to play the game. 
- An excerpt from the code:
![Code](https://i.imgur.com/b3mmGk2.jpg)

# :pencil: Tic-Tac-Toe Game Planning

## High Level Design
There would be a heading called "Tic Tac Toe". Below the main heading, have a heading to display the player who is playing. The game would consist of a three by three grid with nine squares. The user input would be based on clicks on the squares. After each click, the player's mark would be displayed on the square and a check would be done to see if the player has completed three marks in a line. In this case, display that the player has won. If not, prompt the next player to play.   

Have a heading on the lower left side of the screen for name of player 1 and a heading on the lower right side of the screen for the name of player 2. Underneath the grid, have a heading for the game status (Player 1 won, Player 2 won, Tie) which will only be displayed at the end of the game. 

## Technical Notes
- The CSS grid layout would be suitable to use for the board. I saw a Google Image search result of a nine-piece board when searching CSS grid.
- Variables required: player1Name, player2Name, whoseTurn, there may be other variables required.
- The default would be a blank board. Through the DOM, I can make the items appear at the appropriate squares. 
- At the top of the page, create an h1 heading and h2 heading in the HTML.
- Below it, have the main section called Board. Use the CSS grid layout for it.
- Below the board, have headings and paragraph tags for the players and game status.
- The CSS would be in a separate file.
- In the JavaScript, set player1Name and player2Name variables to "Player 1" and "Player 2". Later as an extension we can prompt the players to provide names. 
- Have multiple functions all dealing with the same thing: the user clicks.
- Have a function called playing which would make the "X" and "O" appear on the board in the position where the player selects. Use addEventListener with a click function. 
- Have a function to check the result using a for loop to calculate if there is three of the same type in a line resulting in a winner. This function would be called after displaying the mark on the square. 

# :rocket: Cool tech
This was implemented in HTML content with CSS layout and JavaScript methods.

# :anguished: Bugs to fix :
I thought I had reached MVP stage Wednesday night, but I unfortunately discovered two major bugs on Thursday which I spent time fixing. 

The first of these bugs is that it was possible to click over an existing piece of the board which results in one player overwriting another player's moves thus being functionally incorrect. I fixed it by removing the event listener if the text content on the board has an "X" or a "O". 

The second of these bugs is that if a game is won by playing all pieces of the board, the message "The result is a draw" was displayed. The reason this occurred is because I put a counter and the counter condition was set to print this message once it reached nine, the amount of pieces on the board. As a result of this, I put additional if statements checking for "X" and "O" under my counter check.

Removing the event listener affected the reset button, so I kept the event listener and instead created a variable called occupied to check if the text content on the board has an "X" or a "O". If the square is occupied, then you fall out of this function. Hence the function processes only unoccupied squares. 

# :persevere: Lessons learnt
Test more throughly to find the issues earlier. 

# :white_check_mark: Future features
- The ability for the players to enter their names.
- Images instead of letters for Xs and Os.
- More CSS content to make it look nicer. 
- Changed the fonts.
- Animate the "Tic-Tac-Toe" heading.
- Ensure the design is totally responsive. 
