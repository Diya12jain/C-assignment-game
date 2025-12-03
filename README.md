Basic Knowledge of Snake Game : A simple console-based Snake game implemented in C.
Control the snake to eat the fruit and grow longer while avoiding collisions with yourself.
The game ends when the snake collides with its own tail.
** Controls in the game**
| Key | Action          |
Enter below keys for moving snake:
| `w` for Move Up        |
| `a` for Move Left      |
| `s` for Move Down      |
| `d` for Move Right     |
| `x` for Exit the Game  |
The game is divided into several sections:
Global Variables , Setup Function , Draw Function , Input Function , Logic Function , Main Function.
** In Setup Function initialize all game variables at the start. 
srand(time(0)); → Seeds the random number generator for fruit placement.
gameOver = 0; → Sets the game state to not over.
dir = 0; → Sets the initial snake direction to none (stationary).
x = WIDTH / 2; y = HEIGHT / 2; → Places snake head in the center of the field.
fruitX = rand() % WIDTH; fruitY = rand() % HEIGHT; → Places fruit at a random location.
score = 0; → Initializes player score to zero. **
** In Draw Function display the current game state on the console. **
-> Clears the screen using system("cls"); to redraw each frame.
-> Prints # for left and right walls.
-> Prints O for the snake head.
-> Prints F for the fruit.
-> Prints o for each tail segment by checking tailX and tailY.
-> Prints a blank space if nothing is present. **
** In Input Function handle user input to control the snake. 
Uses _kbhit() to check if a key is pressed.
Uses _getch() to read the key without pressing enter.
Exit the game (gameOver = 1). **
** In Logic Function stores previous head position in tailX[0], tailY[0] and moves each tail segment to the position of the segment in front of it. **
** Also moves snake head based on direction:
dir = 1 → x-- (left)
dir = 2 → x++ (right)
dir = 3 → y-- (up)
dir = 4 → y++ (down)
** In Main Function calls Setup() once to initialize the game.
Draw() → Display the game.
Input() → Handle user input.
Logic() → Update the game state.
Sleep(100); → Pause for 100 milliseconds to control snake speed.
Prints "Game Over!" when the loop ends.
system("pause"); → Waits for the user to press a key before closing. **
