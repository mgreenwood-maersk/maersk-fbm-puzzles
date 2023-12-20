# ASCII A-Maze-ment

Write a program that reads in a simple 2-D maze in a format like these examples:

```
     _______________________FbM
     |     |        |        |
     |__   |_____   |  ______|
     |        |        |     |
     |  ___   |_____   |     |
     |  |  |           |  |  |
     |  |  |  ___      |  |  |
     |  |        |  |  |  |  |
     |  |_____   |__|__|__|  |
     |  |                    |
Start|__|____________________|

      ______________FbM
     |              |
     |________   ___|
     |        |     |
     |  ___   |     |
     |  |        |  |
     |  |__   ___|  |
     |  |     |     |
Start|__|_____|_____|

      _________________FbM
     |                 |
     |__   ______   ___|
     |     |        |  |
     |_____|  ______|  |
     |              |  |
     |__   ___   ___|  |
     |     |  |  |     |
     |_____|  |  |  ___|
     |  |  |           |
     |  |  |__         |
     |           |  |  |
Start|___________|__|__|

```
Download the mazes above as ASCII text. [sample-mazes.txt](sample-mazes.txt)

The input is guaranteed to be a well-formed maze and to have a unique solution path from the bottom left 
grid cell to the top right grid cell. 
Your program should re-output the maze with the solution path filled in, e.g.:

```
      _______________________FbM
     |     |        |XX XX XX|
     |__   |_____   |  ______|
     |XX XX XX|      XX|     |
     |  ___   |_____   |     |
     |XX|  |XX XX XX XX|  |  |
     |  |  |  ___      |  |  |
     |XX|        |  |  |  |  |
     |  |_____   |__|__|__|  |
     |XX|                    |
Start|__|____________________|

      ______________FbM
     |         XX XX|
     |________   ___|
     |XX XX XX|XX   |
     |  ___   |     |
     |XX|   XX XX|  |
     |  |__   ___|  |
     |XX|     |     |
Start|__|_____|_____|

      _________________FbM
     |            XX XX|
     |__   ______   ___|
     |     |XX XX XX|  |
     |_____|  ______|  |
     |      XX XX   |  |
     |__   ___   ___|  |
     |     |  |XX|     |
     |_____|  |  |  ___|
     |  |  |   XX      |
     |  |  |__         |
     |XX XX XX XX|  |  |
Start|___________|__|__|
```
