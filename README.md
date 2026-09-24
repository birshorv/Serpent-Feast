# Serpent Feast — design and playable prototype 0.2

## Pitch
A high score survival game for touch and desktop. Steer the mint snake around several rival snakes. Eat fruit and bread to grow. If a rival touches any snake body, its segments become fruit and bread that anyone can collect. If the player's snake touches a rival or its own body, the run ends. There are no levels; the objective is to beat a saved personal best.

## Rules
- Grid: 24 × 30 with wraparound edges. The player starts alone at a slower pace. Rival snakes begin entering after about six seconds and reappear when defeated. The mint player has a larger glowing body, white head outline, and a visible YOU label.
- Fruit grants 10 score and one growth; bread grants 15 score and two growth.
- Fallen rivals leave food along their body: 20 score for fruit and 25 for bread. The food is contested by all surviving snakes.
- Rivals steer toward nearby food while avoiding bodies when they can. Traps and collisions produce fresh food. Rivals touching the player become food; the player touching a rival ends the run. Head movement is processed in turn order.
- Player speed rises gradually with score. The result screen lists score, personal best, food collected, and longest length, with Play Again and Main Menu.

## Controls and publishing
Swipe the board, use the directional pad, or press arrows/WASD. The game loads the YouTube Playables SDK before its own code, uses readiness and pause callbacks, sends score, and stores the high score with Playables cloud data. Local browser testing uses localStorage. HTML, CSS and JavaScript use relative bundle paths with no external art. Before submission, complete hands-on touch testing, difficulty balancing, SDK test suite and metadata.
