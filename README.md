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

Battleship is a naval stradegy game. Your goal is to defeat the opposing naval fleet. The fleet consists of five different ships.
 
 * Carrier
 * Battleship
 * Submarine
 * Destroyer
 * Sweeper
 
Once you arrange your ships, the game is started. The game system is turn based, meaning that each player alternates their moves one by one. Once all ally or enemy ships are destroyed then the game is over amd the winning fleet is declared.

**One Player** : One user-controlled player, another bot-controlled player

### Ship Placement



### Turn Rotation
