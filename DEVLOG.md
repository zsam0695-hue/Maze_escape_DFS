Entry #1 04/17/26 
- Issues/Error messages or symptoms: I wasn't sure how to start the DFS function or what order the checks should go in.
- Attempts made: I looked at the project README and looked at the function parameters to understand what variables were already given.
- Final resolution: I organized the DFS in the correct order so it first rejects invalid cells, then marks valid cells visited, checks for the exit, and explores neighbors.

Entry #2 04/19/26
- Issues/Error messages or symptoms: My DFS would keep revisiting cells, which could cause infinite recursion or repeated searches.
- Attempts made: I checked whether I had a visited condition and realized I needed to mark the current cell as visited before exploring neighbors.
- Final resolution: I added `visited[r][c] = true;` before the neighbor loop and returned false immediately for already visited cells.

Entry #3 04/19/26
- Issues/Error messages or symptoms: I didn't know how to use `dr` and `dc` to be able to move through the maze. 
- Attempts made: I traced through one cell by hand and tested using `nr = r + dr[i]` and `nc = c +dc[i]` inside a loop with index i from 0 to 3. 
- Final resolution: I eventually used the direction arrays in a loop to check up, right, down, and left in a smooth and consistent way.

Entry #4 04/22/26
- Issues/Error messages or symptoms: The path couldn't print correctly unless the parent arrays were filled in the right places.
- Attempts made: I first thought about assigning the parent after recursion, but then realized `printPath()` needs each child cell to stor the cell it came from before continuing.
- Final resolution: I assigned `parent_r[nr][nc] = r` and `parent_c[nr][nc] = c` right before the recursive DFS call on that neighbor.

Entry #5 04/24/26
- Issues/Error messages or symptoms: I wasn't sure how the DFS would stop once the exit was found, since it's mentioned in the assignment description. 
- Attempts made: I checked if the current cell was the exit, and if it was, I returned true so the recursive calls would keep returning true and the DFS would stop
- Final resolution: I added an exit check `if (r == exit_r && c == exit_c)` to return true if the exit was found, and made the recursive neighbor call return true right away if the exit was found.

Entry #6 04/26/26
- Issues/Error messages or symptoms: I wanted to make sure DFS wouldn't try and move outside the maze boundaries, which would be an invalid indexing. 
- Attempts made: I added checks for row and column values before allowing DFS to continue. I also checked neighbors before assigning parents and the recursion line. 
- Final resolution: I used bounds checks both at the top of the function and inside the neighbor loop too, to prevent access to anything out of range.

Entry #7 04/27/26
- Issues/Error messages or symptoms: I needed to make sure that the walls weren't treated as available path cells.
- Attempts made: I reviewed the maze generator and checked to make sure that 0 means open and 1 means wall.
- Final resolution: I added a wall check with `if (maze[r][c] == 1) return false;` so DFS only explores open cells and not walls.

Entry #8 04/29/26
- Issues/Error messages or symptoms: I looked back at the `OUTPUTguide.md` and the `README.md` while testing to make sure everything was correct. I know this wasn't a requirement, but when inputting any dimension values less than 2 it would either do nothing or crash.
- Attempts made: I tried fixing the problem with a simple if statement in `dfs(...)`, but that did nothing. I'm not allowed to touch the other functions, so I tried fixing the problem in main.
- Final resolution: I wanted the program to allow you to try again until you input valid dimensions, so I wrote an if statement printing "Invalid dimen...." and calling `main()` again, but the code still wouldn't end properly sometimes, so I just added a `return 0;`.