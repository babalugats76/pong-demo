# Construct 2 - Pong Demo

## Adding a Basic Scoring System

Follow these steps to add a basic scoring system to the barebones Pong game.  Remember, the goal of Pong is to get to **11 points** before the opponent. 

1. With the `Game` layer active and unlocked, insert two new object types of the Text plugin type, e.g., `TextPlayerScore`, `TextComputerScore` which will **display the score** to the user
2. Update the properties of `TextPlayerScore` and `TextComputerScore` object instances
    * `Position`: (100,100) &amp; (500,100), respectively 
    * `Size`: 100, 100
    * `Text`: 0
    * `Font`: Arial(36)
    * `Color`: 255,255,255 (White)
    * `Horizontal alignment`: Center
    * `Vertical alignment`: Center
3. With the `Game` layer active and unlocked, insert two new object types of the Sprite plugin type, e.g., `ComputerBaseline`, `PlayerBaseline`, creating each as an **invisible sprites**
4. Position the `ComputerBaseline` and `PlayerBaseline` carefully, stretching to be long and skinny and avoiding the sidelines
5. With the `Pong Event Sheet` add the following three variables (Right-click -> *Add global variable*)

Name | Type | Initial value  | Description | Constant (Y/N)
--- | --- | --- | --- | ---
PlayerScore   | Number | 0 | Current score of Player  | N
ComputerScore | Number | 0 | Current score of Computer| N
GOAL  | Number | 11 | Score needed to win | Y
