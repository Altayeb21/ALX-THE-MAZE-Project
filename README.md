Maze Project

Maze is a semi 3D game where you try to escape the maze while facing and killing enemies, I did this project alone which was a big benefit for me because I learned so much from it and I enjoyed coding every bit of it. being a simple game I focused on graphics to get the ultimate experience from it.

Since I was a child I admired video games, from snake on nokia phones to atari games to today's ps5 modern games, I was facinated by all of these games and I wanted to know how these great things were made, and with alx i had the opportunity to read about SDL library in C and Ray Casting algorithm to make my own game, and the experience was nothing less than amusement.

project blog post: https://www.linkedin.com/posts/abobaker-eltom-3a1a90147_activity-7196348105389178881-eytZ?utm_source=share&utm_medium=member_desktop .

My linkedin Profile: 
https://www.linkedin.com/me?trk=p_mwlite_feed-secondary_nav
wep1.


Installation: use gcc compiler with SDL flags to compile all .c files to make the executable.

gcc *.c -o <executable_name> sdl2-config --cflags --libs -lSDL2 -lSDL2_image

Usage: execute a the file providing the map file name as an argument:

./<executable_name> <map_file_name> a map file called map is provided or you can create your own mapfile. the syntax for a map file is:

first line: player's x, y coordinates terminated by a semicolon. for example: 53, 86;
second line: enemies x, y coordinates seperated with semicolons. for example: 43, 59; 23, 243; 65, 23;
third line: first value represent the map's width, the second value represent the map's height. for example: 20, 20;
fourth to the last line: represents the map. use 1 to represent a wall and 0 for no wall. a line represents a row which has width columns. for example if the dimensions of the map is 6, 5 the map would look something like this:

1, 1, 1, 1, 1, 1;

1, 0, 0, 0, 0, 1;

1, 0, 0, 0, 0, 1;

1, 0, 0, 0, 0, 1;

1, 1, 1, 1, 1, 1;

**NOTE: it is very important that the dimensions provided are consistant with the rows and columns of the map, otherwize the game might crash.

Contribution: Altayeb mohamed : altayebmohamed2013@gmail.com .
Technologies used to develop the game: 1- Ray Casting: So the idea of Ray Casting is to make a 3D world out of a 2D world, a 2D world which consists of a grid containing cells and each cell either contains a wall or it doesn't. so according to the player's position and the direction it's facing, rays are casted, and when a ray hits the wall it records the distance from the player, and this distance is then used to render the the wall on the screen, for example if the distance is small the wall would appear bigger and for greater the distance the smaller the wall would appear. for example: the following picture shows a 2D world

image

and the final 3D world would look something like this:

image

As simple as ray casting algorithm might seem, it took more than a week to implement it, I would wake up every day, bring a white paper and a pen and do the math manually, but when i turn it into code it doesn't work, at first I refused to watch a youtube tutorial about ray casting but after a lot of failure i decided to watch one, and i still couldn't get it 🤣 the problem was that i was able to detect only horizontal walls and after i solved that i wasn't able to detect both vertical and horizontal walls at the same time. after a lot of papers, math and youtube tutorials i was finally able to solve both problems, for the first one i figured that the math for the vertical walls is lightly different from the math for the horizontal ones, and on the second problem i figured that the main loop that detects both walls should not break after it detects one of them because sometimes they do not go simultaneously and the vertical wall might be closer on the next iteration than the horizontal wall on this one and vice versa.

2- SDL library: for creating the window and rendering everything on it, I used SDL (Simple DirectMedia Layer) library in C, its simpleness and ease of use made it a great choice to work with.

I learned so much from this project, for instance when i first heard about ray casting i couldn't imagine how would i cast a ray using only code, but when i delved deeper i understood it is just math, this changed my perspective on how i was viewing things, that in programming we only care about the characteristics of the thing not the thing in essence. working with SDL was really fun, i learned how things are rendered on the screen and the basics of game making. I used to think that game developing is too complicated for me and i should stick to web developing but after this project i might think seriously about considering game developing as a path i would go into. As a passionate and determined individual, I thrive on challenges that push me to grow and learn. My journey with developing the maze game using ray casting was both exhilarating and enlightening. Through overcoming various obstacles and refining my coding skills, I discovered a deep sense of satisfaction in bringing ideas to life. Beyond programming, I am an avid learner who enjoys exploring new technologies and embracing opportunities for personal and professional development. I am excited to continue my journey of creativity, innovation, and self-discovery in the world of game development and beyond
