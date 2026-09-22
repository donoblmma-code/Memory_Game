Antigravity Memory Game Plan

Goal: Build a polished browser-based memory card matching game using HTML, CSS, and JavaScript.

Project files:

index.html
style.css
script.js

Core gameplay:

Create a grid of face-down cards.
Each symbol/image must have exactly one matching pair.
Shuffle all cards randomly whenever a new game starts.
Player can flip only 2 cards at a time.
Matching cards stay face-up.
Non-matching cards stay visible briefly, then smoothly flip back.
Ignore clicks while two cards are being checked.
Ignore clicks on cards that are already matched or already flipped.
End the game when every pair has been found.

Game modes:

Easy — 12 cards / 6 pairs
Medium — 16 cards / 8 pairs
Hard — 24 cards / 12 pairs
Changing difficulty should automatically start a fresh game.

UI design:

Modern, simple interface.
Center the game on the screen.
Responsive on desktop and mobile.
Large title: Memory Game
Show:
Timer
Move counter
Matches found
Difficulty
Include a clear Restart Game button.
Cards should have rounded corners and subtle shadows.
Use a real 3D flip animation with transform: rotateY().
Add smooth hover feedback, but keep the visual style clean rather than overly flashy.

Animations and feedback:

Smooth card flipping.
Correct matches should have a small success animation.
Incorrect matches should have a very subtle shake.
When the final pair is found, show a polished victory animation.
Add lightweight confetti on victory.
Avoid excessive particles or distracting effects.

Win screen:
Display a modal containing:

You Win!
Completion time
Number of moves
Accuracy percentage
Best time
Best move count
Play Again button
Next Difficulty button when applicable

Game statistics:

Start the timer when the player flips their first card.
One move = one completed attempt involving two cards.
Calculate accuracy based on successful matches versus total attempts.
Save best times and best move counts separately for each difficulty using localStorage.

Sound:
Add optional simple sounds for:

Card flip
Correct match
Incorrect match
Victory

Include a sound on/off button. Do not autoplay music.

Code requirements:

Use vanilla HTML/CSS/JavaScript only.
Do not use React or external frameworks.
Keep the code organized and readable.
Separate game state from UI logic where practical.
Use CSS variables for frequently reused styling values.
Avoid duplicated code.
Make restarting the game reset every relevant variable correctly.
Make sure rapid clicking cannot break the game.

Responsive behavior:

Cards must resize automatically on smaller screens.
The full board should fit comfortably without horizontal scrolling.
Buttons must work well with mouse and touch.
Prevent accidental text selection while playing.

Testing Antigravity should perform after implementation:

Launch the game locally.
Open it in the browser.
Verify that cards shuffle.
Verify matches stay visible.
Verify incorrect cards flip back.
Test rapid clicking.
Test restarting halfway through a game.
Test every difficulty.
Complete a full game and verify the victory modal.
Refresh the page and verify best scores remain stored.
Test desktop and mobile viewport sizes.
Check the browser console and fix all errors.

Important: Do not stop after creating the initial files. Run the game, inspect it visually in the browser, test all major interactions, fix any broken behavior or poor spacing, and continue iterating until it feels like a finished small web game.