# Snake Game
GDSC's Fall 23 Workshop Project to learn how to make a snake game in python.

## Description
<ul>
  <li>Part 1 of the summary title has detailed instructions to make the code.</li>
  <li>Part 2 of the summary title has instructions to push the project to your GitHub account.</li>
</ul>

Before you start, please install the resources below: <br>
<ul>
  <li>Visual Studio Code: https://code.visualstudio.com/download</li>
  <li>GitHub Extention: Python</li>
  <li>Git Bash: https://git-scm.com/downloads</li>
  <li>Check Codelab: https://usfgdsc.github.io/snake/#2 for more guidance</li>
</ul>

GDSC README Template: https://github.com/USFGDSC/ReadMeTemplate

## Final Project:

<p align="center">
  <img src="https://github.com/USFGDSC/snake/assets/98829238/872ea82f-df29-49d1-9e44-7ea20feb6cb9" width="350" height="300"/>
  <img src="https://github.com/USFGDSC/snake/assets/98829238/7362bda1-2afa-4558-8d51-ded82bc53142" width="350" height="300"/>
</p>

## Technologies used:
Python

## Summary of the DevShop:

## Part 1

<li>Follow DevShop Steps for the project!</li>
  If you are lost, navigate to the "finished" branch of the project repository or the Codelab link above to catch up  
  <br>
  <br>
<li>How to run the project in VS Code:</li>
<ul>
  <li>Step 1: Open the terminal, making sure is in the correct folder.</li>
  <li>Step 2: Type the command “Python File.py” where “File” is your file's name and press enter</li>
</ul>
<br>

---------MILESTONE 1---------

### STEP 1 ->  Setup screen ###

main.py:
    - add screen attribute and complete setup in game controller class

### STEP 2 -> Make Snake body ###

snake.py:
    - add visual setup and position attribute to Segment class init method
    - add head attribute to Snake class init method
    - add segments attribute to snake class init method (1 head +  2 segments)
    - add previous tail coordinate attribute to snake class init method 

main.py:
    - create instance of snake inside Gamecontroller class init methood

### STEP 3 -> moving Snake forward ###

snake.py:
    - Complete get_position and change_position Segment methods
    - Complete move forward Head method
    - Complete move forward Snake method

main.py:
    - Add attribute to hold game state
    - Add to game loop method that moves snake forward while game not Over
    - Add tracer(0) to screen and include sleep, update in game loop method

---------MILESTONE 2---------

### STEP 4 -> turning left and right ###

snake.py:
    - Add heading attribute to segment class
    - Complete turn left, right, up down methods in Head
    - Complete turn left and turn right methods in Snake

main.py:
    - Add screen listener to screen attribute in Game Controller
    - add onkeypress that turns snake left on 'Left' key press
    - add onkeypress that turns snake right on 'Right' key press

---------MILESTONE 3---------
        
### STEP 5 -> Create Food ###

food.py:
    - Add visual attributes in Food init method 
    - Complete move around method
    - Call move around method in init method

main.py:
    - Create an instance oof food class inside the Gamecontroller class init method

### STEP 6 -> detect snake food collissions ###

snake.py:
    - Complete get distance method in Head
    - Complete detect collission food method in Snake (recommend use distance <= 15)

main.py:
    - Add conditional statement to handle collision with food, if fullfilled move food move_around
    - Add handle collission wit food to the end of the game loop method 


### STEP 7 -> Eat food if collission ###

snake.py: 
    - complete eat food method that increases size of snake body
    - call eat food method inside detect collission food method only if conditional statement is True

---------MILESTONE 4---------

### STEP 8 -> check for collisionos with wall ###

snake.py: 
    - Complete echeck collission with wall method in Head class
    - Complete echeck collission with wall method in Snake class

main.py :
    - add conditional statement to game over method for collission with wall if so change game state attribute
    - call game over method at the end of the game loop 

### STEP 9 -> Collisions with self 

snake.py:
    -  Complete detect collission with self method in Snake class

main.py; 
    - add detect collission with self to the conditionoal statement in game over method 


---------MILESTONE 5--------- --> optional milestone

### STEP 10 -> Create Scoreboard  ###

scoreboard.py;
    - add basic visual setup and score attribute to Scoreboard class
    - complete write_score method (which should clear itself before writing score)
    - call write score method in init method 

main.py;
    - cerate an instance of scoreboaord inside the Gamecontroller class init method


### STEP 11 -> Increment socre when eating food ###

scoreboaord.py:
    - Complete increment score method in Scoreboard class (shold increase score and rewrite it )

main.py:
    - Add increment score in case of collission with food inside the hadnel collission food method of GameController class


---------MILESTONE 6---------

### STEP 12 -> GAME OVER screen ###

scoreboard.py:
    - Complete write_game_over method 

main.py;
    - if conditional statement in game over is true call the scoreboard's write game over method 

### STEP 13 -> Reset functionality ###

snake.py:
    - Complete the reset method in the snake class

scoreboard.py:
    - Complete reset method in scorebaord class

main.py:
    - Complete reset method in Game Controller class
    - Add a keypress listener to game over mehtod (if game has ended) that calls reset method when activated


## Part 2

<ol>
  <li>VS Code installed</li>
  <br>
  <li>GitHub Account created/logged in</li>
  Having trouble? Go to: https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account
  <br>
  <br>
  <li>Git Bash Installed and configurated:</li>
  <ul>
    Open Git Bash in your computer and type:
    <li>git config --global user.name "Your name"</li>
    <li>git config --global user.email youremail@example.org</li>
    <b>Attention: ***Git email must be the same GitHub email*** </b>
  </ul>
  <br>
  <li>Create a new repository on GitHub</li>
  <ul>
    <li>Step 1: Select the dropdown menu, click on "Your repositories." This will take you to a page that lists your existing repositories (if any).</li>
    <li>Step 2: On the "Your repositories" page, click the green "New" button. This button is located on the right side of the page, just above your repository list.</li>
    <li>Step 3: Fill in Repository details, make sure to choose to add a README file. Once you've filled in the required details, click the green "Create repository" button at the bottom of the page.</li>
  </ul>
  <br>
  <li>Initializing the repository using Git:</li>
  <ul>
    <li>Step 1: Navigate to the repository you which to clone</li>
    <li>Step 2: Click the "Code" Button on the repository's main page and copy the HTTPS Url</li>
    <li>Step 3: Open the directory(folder) you want the cloned repository to be in and then, navigate to a new terminal within it</li>
    <li>Step 4: In the terminal run the followings command  "git clone 'Insert your HTTPS URL here' " and press Enter</li>
  </ul>
  <br>
  <li>How to commit a repository:</li>
  <ul>
    <li>Step1: Navigate to Source control on VScode</li>
    <li>Step 2: Ensure you have the modified file code you want to commit</li>
    <li>Step 3: Select the '+' next to the file name for the modified file which you are tying to commit</li>
    <li>Step 4: Write a message in the Entry box to indicate what change/feature has been added</li>
    <li>Step 5: Click the checkmark icon (or "Commit" button) next to the commit message box. This will commit your staged changes.</li>
    <li>Step 6: Click the "..." (more options button)  button in the Source Control panel, and select "Push" to push your changes to the remote repository.</li>
  </ul>
  <br>
  <img src="https://github.com/USFGDSC/BoardReadMeTemplate/assets/98829238/15351354-0d53-4530-b2c6-2e0e950a5f40" height=300px />   
  <br>
  <br>
  <li>Go to your updated repository and edit your README. You can use GDSC README Template: https://github.com/USFGDSC/ReadMeTemplate </li>
  This is really important to mantain an organized repository and facilitate the access to anyone that wants to look your project!
</ol>
<br>
