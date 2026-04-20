Minimum 6 entries.
Each entry must document:
- The issue encountered.
- Error messages or symptoms.
- Attempts made.
- Final resolution.

Entry #1 04/17/26 
- Issues/Error messages or symptoms: I wasn't sure how to start the DFS function or what order the checks should go in.
- Attempts made: I looked at the project README and looked at the function parameters to understand what variables were already given.
- Final resolution: I organized the DFS in the correct order so it first rejects invalid cells, then marks valid cells visited, checks for the exit, and explores neighbors.

Entry #2 04/19/26
- Issues/Error messages or symptoms: My DFS would keep revisiting cells, which could cause infinite recursion or repeated searches.
- Attempts made: I checked whether I had a visited condition and realized I needed to mark the current cell as visited before exploring neighbors.
- Final resolution: I added `visited[r][c] = true;` before the neighbor loop and returned false immediately for already visited cells.

Entry #3 MM/DD/YY
- Issues/Error messages or symptoms:
- Attempts made:
- Final resolution:

Entry #4 MM/DD/YY
- Issues/Error messages or symptoms:
- Attempts made:
- Final resolution:

Entry #5 MM/DD/YY
- Issues/Error messages or symptoms:
- Attempts made:
- Final resolution:

Entry #6 MM/DD/YY
- Issues/Error messages or symptoms:
- Attempts made:
- Final resolution:
