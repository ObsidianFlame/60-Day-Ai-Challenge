Build an AI-Powered Face Puzzle Game with Claude

What I built
A neuro-rehabilitation puzzle game designed for patients recovering from stroke, TBI, and concussion. 
It runs entirely in the browser — no server, no login — with a five-image gallery including two built-in shapes for early-recovery patients, three difficulty levels from 3×3 to 5×5, and a drag-and-drop board where pieces lock permanently green when placed correctly. 
The reference image stays visible throughout. A progress modal tracks every session and plots completion time and moves on an SVG line chart, surfacing a trend across sessions.

What i learned.

The iterations started out very difficult but evolved to the point that puzzle peices were highlighted when in the correct position, giving a 'dopamine effect' or small-win as the puzzle is solved. 
The edges have subtle hints to connect the pieces without additional markups needed. The clinical design helped me understand that locked pieces resist accidental displacement and generous snap zones mean that neurological complexities such as tremors are accounted for. 
Designing for reduced motor control makes the interaction better for everyone.

Prompt:
Include these considerations:
Concept itself, clinical design constraints.

1. Digital files upload into the tool
2. Session tracking, number of moves
3. Caregiver/clinician mode

Here is the prompt:
You are an expert front-end developer. Build me a complete, fully working puzzle game as a single self-contained HTML file (no external dependencies except what can load digitally from my computer). The game is a clinical tool for neuro-rehabilitation.

FEATURES REQUIRED — deliver ALL of these in one complete response:
1. UPLOAD FILE
   - On load, request user to upload their desired file
   - Show a preview of the upload 
   - Display a 'Ready' button to capture the puzzle
2. PUZZLE GENERATION
   -  User must set the difficulty to low / medium / high

* After 'Ready' let the user choose difficulty: 3×3, 4×4, or 5×5 grid
   - puzzle must be in a simple square format for low diffulty, jigsaw style format for medium and high difficulty
   - Randomly scramble the pieces (guarantee it is solvable)
   - Render each piece as a draggable tile at its scrambled position
3. DRAG & TOUCH GESTURE CONTROLS
   - Support both mouse drag (desktop) and touch drag (mobile/tablet)
   - When a piece is dropped onto another piece's cell, swap their positions
   - Snap pieces to the nearest grid cell on release
   - Highlight a piece with a coloured border while it is being dragged
   - Show a green border on pieces that land in their correct position
4. TIMER & MOVE COUNTER
   - Start the timer the moment the puzzle begins
   - Display elapsed time live (format: mm:ss.t)
   - Count and display total moves made
   - Show how many pieces are correctly placed out of the total
5. WIN DETECTION & RESULTS SCREEN
   - Detect automatically when all pieces are in the correct position
   - Stop the timer immediately on win
   - Show a results overlay with: final time, total moves, and difficulty
   - Save the top 5 best times to localStorage with date, time, moves, and difficulty
   - Display a leaderboard of saved best times
6. UI & POLISH
   - Clean, modern design
   - Works on desktop and mobile
   - 'Retake Photo' button
   - 'Play Again' button
   - 'New Photo' button
   - Responsive layout
TECHNICAL REQUIREMENTS:
- Single HTML file
- All CSS and JS inline
- No frameworks
- Must work in Chrome, Firefox, and Safari
- Camera must work over HTTPS or localhost
- Handle camera permission denied gracefully
- Do NOT leave placeholder comments
Output the complete HTML file in one code block. Do not truncate or summarise any section.

You may ask up to 5 clarifying questions and 3 suggestions to improve the output.
