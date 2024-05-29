# snake-game
snake game

GamePanel is a JPanel that contains the game logic and rendering. It has several instance variables, including the size of the game units, the number of body parts of the snake, the number of apples eaten, the position of the apple, the direction of the snake, and a boolean flag indicating whether the game is running or not. It also has a Timer object that triggers the game logic to be executed at regular intervals.

The GamePanel constructor initializes the instance variables, sets the preferred size of the panel, sets the background color to black, sets the panel to be focusable and adds a KeyAdapter to handle user input. It also starts the game by creating a new apple and starting the timer.

The startGame() method creates a new apple and starts the timer.

The paintComponent() method is overridden to draw the game components. It calls the draw() method to do the actual drawing.

The draw() method takes a Graphics object as a parameter and uses it to draw the game components. If the game is running, it draws the apple and the snake. If the game is not running, it calls the gameOver() method to display the game over screen.

The newApple() method generates a new random position for the apple.

The move() method updates the position of the snake's body parts based on its direction.

The checkApple() method checks if the snake has eaten the apple. If it has, it increases the number of body parts and the number of apples eaten, and generates a new apple.

The checkCollisions() method checks for collisions between the snake's body parts and the game boundaries. If a collision is detected, the game stops.

The gameOver() method displays the game over screen with the final score.

The actionPerformed() method is called at regular intervals by the Timer object. It calls the move(), checkApple(), and checkCollisions() methods to update the game state.

GameFrame is a JFrame that adds an instance of GamePanel to it. It sets the title, default close operation, resizability, visibility, and location of the frame.

The main() method creates an instance of GameFrame to start the game.
