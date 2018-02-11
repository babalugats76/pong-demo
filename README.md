# Construct 2 - Pong Demo

## Adding a Basic Scoring System

Follow these steps to add a basic scoring system to the barebones Pong game.  Remember, the goal of Pong is to get to **11 points** before the opponent. Start with the `PongDemo.capx` Construct 2 project and modify according to the instructions. Reference `PongDemoScoring.capx` for what your project should look like when completed.

1. With the `Game` layer active and unlocked, insert two new object types of the **Text** plugin type, e.g., `TextPlayerScore`, `TextComputerScore` which will **display the score** to the user
2. Update the **properties** of the `TextPlayerScore` and `TextComputerScore` object instances:

Property | Value
--- | ---
Position | **100,100** &amp; **500,100**
Size |  **200, 100**
Text | **0**
Font | **Arial(36)**
Color | **255,255,255** (White)
Horizontal alignment | **Center**
Vertical alignment* | **Center**

3. With the `Game` layer active and unlocked, insert two new object types of the **Sprite** plugin type, e.g., `ComputerBaseline`, `PlayerBaseline`, creating each as an **invisible sprites**
4. Position the `ComputerBaseline` and `PlayerBaseline` carefully, stretching to be **long and skinny**; avoiding sidelines
5. With the `Pong Event Sheet` open, add the following **variables** (Right-click -> *Add global variable*)

Name | Type | Initial value  | Description | Constant (Y/N)
--- | --- | --- | --- | ---
PlayerScore   | Number | 0 | Current score of Player  | N
ComputerScore | Number | 0 | Current score of Computer| N
GOAL  | Number | 11 | Score needed to win | Y

6. Add an action to **On start of layout**, setting `PlayerScore` and `ComputerScore` to **0**; for each: 
    * *Add Action* -> *System* -> *Set value* (Under *Global &amp; local variables*) 

7. Add an event (trigger) for `ComputerBaseline` and `PlayerBaseline` which **checks for collisions** with the `Ball` object type. If `Ball` collides with `ComputerBaseline`, increment `PlayerScore` by **1**; if `Ball` collides with `PlayerBaseline`, increment `ComputerScore` by **1**. You will also need to update the contents of the corresponding *Text* object type, i.e., `TextComputerScore` or `TextPlayerScore` with the newly-updated value of the global variable:
    * *Add event*
        * `PlayerBaseline`or `ComputerBaseline`
        * *On collision with another object*
            * Object: `Ball`
        * *Add action* -> *System* -> *Add to* (Under *Global &amp; local variables*) 
            * Variable: `PlayerScore` or `ComputerScore`
            * Value: **1**
        * *Add action* -> `TextPlayerScore` or `TextComputerScore` -> *Set text*
            * Text: `PlayerScore` or `ComputerScore`
8. Add an event that checks for the **end of the game**. If the game is over, **restart the layout**:
    * *Add event*
        * *Compare two values* (Under *General*)
            * First value: `PlayerScore`
            * Comparison: = (Equal to)
            * Second value: `GOAL`
    * Right-click -> *Make 'Or' block*
    * Right-click -> *Add* -> *Add another condition*
        * *Compare two values* (Under *General*)
            * First value: `ComputerScore`
            * Comparison: = (Equal to)
            * Second value: `GOAL`
    * *Add action* -> *System* -> *Restart layout* (Under *General*)
    
    
    