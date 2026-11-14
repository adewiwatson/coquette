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

0.5.8 / 2014-12-16

[FIX] Mouse coordinates are now correct when window is scrolled.

0.5.7 / 2014-12-15

[FIX] Mouse coordinates are now correct for a canvas that has a parent that is "position:relative".  (Thanks, cdosborn.)

0.5.5 / 2014-12-15

[NEW] Add Racecar demo.

0.5.2 / 2014-12-01

[FIX] Fix Left Right Space to destroy ALL asteroids in group when one member hit with bullet.

0.5.1 / 2014-12-01

[FIX] Typo in docs.

0.5.0 / 2014-12-01

[BREAKING CHANGE] Coquette no longer distingishes between initial collisions and sustained collisions.  `collision()` is still called for every tick that an entity intersects with another entity, but no collision type is passed.

[BREAKING CHANGE] Coquette no longer calls `"uncollision()` on entities.

0.4.5 / 2014-09-12

[FIX] Spinning shapes demo uses relative paths for script loading. (Thanks, douglascalhoun.)

[FIX] Box2D demo uses relative paths for script loading.

0.4.4 / 2014-06-26

[FIX] Remove unused callback params from `entities.create()` and `entities.destroy()`.

0.4.3 / 2014-03-07

[FIX] Draw people in correct place in simple demo.  (Thanks, tmcw.)
