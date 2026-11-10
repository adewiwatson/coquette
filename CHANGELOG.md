0.5.10 / 2016-02-04

[CHANGE] Make background color optional.  Allows use of Coquette as a (partly) transparent layer in a stack of canvases. (Thanks, cdosborn!)

[NEW] Add `setBackground()` color function.  (Thanks, cdosborn!)

[BREAKING CHANGE] Reorder main update loop sequence to:

* Update game
* Update entities
* Tell entities about collisions
* Render

Before, entities were told about collisions first.  This meant that, for example, an entity could move and be rendered in an impossible position, before collision resolution could be run.

This is probably not a breaking change, but I marked it as so just in case your game logic relies on the old behaviour.

(Thanks, cdosborn!)

[NEW] .gitignore support for vim.  (Thanks, cdosborn!)
