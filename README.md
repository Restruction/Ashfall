## Ashfall
Wildfire simulator in Rust with some basic rules
### Tiles
Green = Live tree

Brown = Dead tree

Orange = On fire

Black = Ashes

### State changes
Each state change has a chance to occur which increases based on the 8 surrounding tiles

Green/Live -> Brown/Dead (increased chance by number of surrounding live trees)

Green/Live -> Orange/Burning (only has a chance when adjacent to other burning tiles. Increases chance for each burning tile)

Brown/Dead -> Orange/Burning (increased chance by number of surrounding dead trees)

Orange/Burning -> Black/Ashes (always happens)

Black/Ashes -> Green/Live (increased chance by number of surrounding live trees)
