# Battleship
Battleship created in MASM32.

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
Left Click: Vertical Placement   Right Click: Horizontal Placement
```
The ships are not allowed to breach the bounds of the map or overlap with each other. The game will prevent this from happening and will display an error message asking to place again in a valid location.

Once the ships are placed, the game proceeds to the computer placement.

#### Computer Placement

The computer bot places its ships after the user is completed placing theirs. This is done automatically and the user is updated once this process is completed.

Once the computer has placed its ships, the turn rotation begins.

### Turn Rotation
