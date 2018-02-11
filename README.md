# Construct 2 - Pong Demo

## Adding a Basic Scoring System

Follow these steps to implement a basic scoring system to the barebones Pong game.  Remember, the goal of Pong is to get to 11 points before the opponent. 

1. With the `Game` layer active and unlocked, insert two new object types of the Text plugin type, e.g., `TextPlayerScore`, `TextComputerScore` which will display the score to the user
2. Update the properties of `TextPlayerScore` and `TextComputerScore` object instances
    * `Position`: (100,100) &amp; (500,100), respectively 
    * `Size`: 100, 100
    * `Text`: 0
    * `Font`: Arial(36)
    * `Color`: 255,255,255 (White)
    * `Horizontal alignment`: Center
    * `Vertical alignment`: Center
3. With the `Game` layer active and unlocked, insert two new object types of the Sprite plugin type, e.g., `ComputerBaseline`, `PlayerBaseline`, creating each as an *invisible sprites* 