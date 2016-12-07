# Battleship
Battleship created in MASM32.

## Installation

### Prerequisites

* Install Irvine libraries from [here](http://kipirvine.com/asm/examples/)
* Install masm32 executable and libraries from [here](http://www.masm32.com/download.htm)

### Steps

1. Download main.asm
2. Create a Visual Studio project. Adjust the build settings to be compatible with masm32.

If you have downloaded the 32-bit Visual Studio project from kipirvine, then you can reuse
it for future projects.
```
Located at C:\Irvine\Examples\Project_sample\
```

3. Replace the .asm file in the project with main.asm
4. Download and retireve each sound from the sounds\ folder

For the sounds to work properly, they must be placed in the below location.
```
C:\Irvine\
```
If you would like to change the location of the sounds, you have to change your reference to the
sound in the .asm file starting at line 87
```
Example: explosionSound BYTE "C:\Irvine\shipexploding.wav", 0
```
5. Build the project and run. There should be no errors.
