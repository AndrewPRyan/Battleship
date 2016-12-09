# Battleship
Battleship created in MASM32.
Lines: 4086
#### Contributions

* Andrew: Created maps and UI. Integrated score system and UI adjustments including ship health and directions. Implemented mouse clicks for both left and right click. Created player ship placement and the algorithm behind the player turn. Created all UI screens such as splash screen, explosion screens, and victory/defeat screen. Implemented sonud.

* Brandie: Created the entirety of the computer. This includes random and automated ship placement and attacking the player map. Created complex algorithms to ensure that the computer is smart enough to beat the player. Helped on perfecting UI elements and statistics. Created introduction screen at the beginning of the game.

#### Known Bugs: 

* Ships can sometimes be placed outside of map bounds
* Very rarily, an enemy ship may be deployed one cell outside of the map bounds
* Under certain circumstances, the UI might look innacurate due to displaying of integer values

## Getting Started

The project must be set up and all dependencies must be installed. This project will only run in Visual Studio or any IDE that supports masm32. It can only be run on Windows.

### Background

This game was created by a group of two individuals for an undergraduate assembly language course. The course focused on masm32, hence why it is coded in this language. 

### Installation

#### Prerequisites

* Install Irvine libraries from [here](http://kipirvine.com/asm/examples/)
* Install masm32 executable and libraries from [here](http://www.masm32.com/download.htm)

#### Steps

1. Download main.asm.
2. Create a Visual Studio project. Adjust the build settings to be compatible with masm32.
3. Replace the .asm file in the project with main.asm.
4. Download and retireve each sound from the sounds\ folder.
5. Build the project and run. There should be no errors.

##### Tips and Additional Setup

If you have downloaded the 32-bit Visual Studio project from kipirvine, then you can reuse
it for future projects.
```
Located at C:\Irvine\Examples\Project_sample\
```

For the sounds to work properly, they must be placed in the below location.
```
C:\Irvine\
```
**IMPORTANT** : All sounds used must be in .wav format. This is the only format that
works properly in the given implementation.

If you would like to change the location of the sounds, you have to change your reference to the
sound in the .asm file starting at line 87
```
Example: explosionSound BYTE "C:\Irvine\shipexploding.wav", 0
```

## How To Play

### Basics

Battleship is a naval stradegy game. Your goal is to defeat the opposing naval fleet. The fleet consists of five different ships of different sizes (as specified after each ship).
 
 * Carrier : 5
 * Battleship : 4
 * Submarine : 3
 * Destroyer: 3
 * Sweeper : 2
 
Once you arrange your ships, the game is started. The game system is turn based, meaning that each player alternates their moves one by one. Once all ally or enemy ships are destroyed then the game is over amd the winning fleet is declared.

**One Player** : One user-controlled player, another bot-controlled player

### Ship Placement

#### Player Placement

The player will begin the game placing their ships. This is done on the leftmost map in the user interface. Each ship will be placed in a specific order (as defined in the list above under **Basics**).

To place a ship, the player must click on a coordinate on their map. Different clicks represent different orientations for placement.
```
            Left Click: Vertical Placement                       Right Click: Horizontal Placement
```
The ships are not allowed to breach the bounds of the map or overlap with each other. The game will prevent this from happening and will display an error message asking to place again in a valid location.

**IMPORTANT** : To fully experience ship placement, you must have a mouse/trackpad/trackball that allows for left and right mouse clicks. There is no alternative to this feature.

Once the ships are placed, the game proceeds to the computer placement.

#### Computer Placement

The computer bot places its ships after the user is completed placing theirs. This is done automatically and the user is updated once this process is completed.

Once the computer has placed its ships, the turn rotation begins.

### Statistics and Scoring System

There is no set scoring system in Battleship. Rather, there are scores to keep track of the current state of the fleet. The game will display the total health (which is calculated by the amount of health left in each ship), and the amount of ships remaining (which will change color the closer the amount gets to 0). These statistics are displayed below each map for both the player and the computer. 

### Turn Rotation

For each turn, the player selects coordinate on the computer map they wish to attack. Once a coordinate is clicked, the user interface displays if the player has either hit or miss an enemy ship. This is done by changing the appearance of the coordinate selected.

 * Red X for Hit
 * White O for Miss
 
Under Directions, the game outputs if the attack was a hit or miss. This is another way to be notified of the last move.
**WARNING** : If the same coordinate is selected more than once, it will count it as a turn. Be wise, this counts as your turn.

Each time a ship is destroyed by the player or computer, the game displays an explosion screen to make sure the player knows the current state of the game. On either map, the X for hit will not change color or display if that ship is sunk. It is up to the player to know which ships are sunk and which ones are in the process of being sunk.

After the player has completed their turn, the computer turn is automatically performed. Under Directions, the game notifies when the computer is attacking the player. The player must wait until the computers turn results are displayed in order to attack again. The computer attack will be displayed on the player map with the same UI changes as the player attack.

There are delays in place for each turn to ensure enough time to plan your next attack. There is no time limit for planning an attack, so the player can take as long as they want to attack the computer.

### Goal

Once the player has destroyed all of the computers ships, then they will be welcomed with a victory screen. If the player fails to destroy all computer ships before the computer destroys theirs, then they will be greeted with a defeat screen.

The game has ended. To play the game again, you must rerun the program as there is no feature to restart from the same instance of the game.

## Acknowledgments

### Authors

All contributers to the project

**Special thanks to all contributers who helped create this project and thanks to the instructor who made all of this possible**

Created Fall 2016
