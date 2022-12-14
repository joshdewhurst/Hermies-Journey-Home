# Hermie-s-Journey-Home

## Play Yourself 
[Hermie's Journey Home](https://joshdewhurst.github.io/Hermies-Journey-Home/)

# Game Discription:
### This will be a game centered around a poor hermit crab who has misplaced his shell. Without protection he will die everytime he runs into a rock, sand castle, or enemy. The objective is to survive the journey long enough to find your shell and get back to safety.
___
# Game Play Basics
### This game is very easy to play. There are only four commands.
- "A" = go left
- "D" = go right
- "W" = go up
- "S" = go down
### You are trying to avoid obstacles on the beach until you either, lose your life as a defenseless crab, or beach the timer and win!
___
## This game will use HTML, CSS, Javascript, DOM Elements and Canvas. 
___
# MVP Goals:
- Create a game with movement controls, life counter, and timed events
- Create different damage points based on seperate objets/enemies
- If you die, the screen says game over and you are forced to restart
- Have enemies move at different speeds based on their type
- End point is on a timer and will appear after 3-5 minutes, game will end once the player reaches this end point
___
# WireFrame:
![Hermit Crab Game Board](https://i.postimg.cc/RZw35sm4/Screen-Shot-2022-08-22-at-9-22-37-AM.png)
___
# Stretch Goals:
- Create different levels with different speeds/times
- Create drawings myself and have them show up on the screen as art 
- Create a leaderboard that tracks health level after each level and remembers that value and records it in a leaderboard 
___
# Road Blocks Before Starting:
- I make a lot of syntax errors and keeping track of that will be hard for me. 
- Making my code easy and readable and not conveluted.
- Creating timed events for each enemy object and when they will appear and move across the screen. 
___
# Road Blocks After Finising
- I need to compress my code and make it more readable and not as repetitive. I could have done the Classes differently.
- I had an issue with two timer-like functions, one that tracks the game frame and one that changes a running clock in the game. I wish I would have compressed these.
- I don't know how to make an image redraw so it is only the image and not the blank white background. i.e. outlining the image. This is one of the things I spent a long time trying to do. And when rendering an image, making it not leave traces when prompted to move.
- The way I had my game play function set up, it was calling itself recursively over and over and over, and I think that caused me to encounter errors when I tried to create a health/score constant that could be deducted
___
# My Process
### Going into this game design, I was so focused on making it LOOK a certain way. I wanted my images to move a certain way, function a certain way, and have more complex elements without necessarily having a good foundation of the basics. 
### Below are bullet points of my Planning Process when I wrote out my idea
- Create Classes for Pieces
    - Player (Hermie); pink square
    - Crab; red circle
    - SandCastle; yellow circle
    - Shell; blue circle
- Game Play
    1. Make player move on key commands
    1. Make enemies move across screen on various speeds
    1. Create a collision function
    1. Create a lose game function
    1. Create intervals to spawn enemies/ change clock/ end game.
    1. Create a start button/ clear button to restart game.
___
# Code I was proud of
## Creating my clear button to appear once my game frame reached a certain time and the player "Survived" and won was something I a actually really proud of.

```javascript
gameFrame++;
    if (gameFrame >5500) {
        gameOver = false
        document.getElementById('title').innerText = "Winner!!!"
        // making a replay button
        let btn = document.createElement("button");
        btn.innerHTML = "Play Again!";
        document.body.appendChild(btn);
        btn.addEventListener('click', () => {
            location.reload()
        })
    }
```
### I know it is not the prettiest way, but when I decided to have clear refresh the page, I know that my game would start over. I was struggling with my game play loop running recursively, so havng this idea made me happy that I was able to find a work around. 
___
# Post Game Reflection
### Reflecting on this project, I realized that I am not good at taking things slowly, and starting where I am at and NOT where I want to finish. A huge amount of my time creating this animation loop, I spent trying to render images to move freely without traces, and I could have spent that time building my logic, redesigning my CSS, or working towards some of my stretch goals with what I knew how to do; draw shapes. 
### I also realized that I need to ask for help when I need it, instead of spending hours by myself trying to get a line of code to work. If I were to do this project again I would follow the below steps:
- brainstorm game
- write out on paper, what needs to happen, and general logic
- start with what I know before building out
- if I get stuck for longer than 45 minutes, ask for help
- build out once the basics are there
#### I am excited to go in over the next couple weeks and get my game to run how I liked by building it out slowly one element at a time, instead of trying to do every element all at once. The following are things I will add for sure now that I feel more confident with my basics
- Making crabs move like crabs.
- Making an end goal that you have to touch to end the game.
- Having game pieces be images instead of just shapes.
- Creating a health meter that will deduct health when touching an enemy, and also having the enemy disappear on contact.
___
# Credits
 - Franks Laboratory on Youtube. 
 [Youtube](https://www.youtube.com/c/Frankslaboratory/videos)
 - David Reid on Youtube. 
 [Youtube](https://www.youtube.com/watch?v=FwLMz7jMRac)
 - CodeExplainedRepo/FlappyBird-JavaScript on Github
 [GitHub](https://github.com/CodeExplainedRepo/FlappyBird-JavaScript)
