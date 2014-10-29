Restore-Render-Parts
====================

Restores the old render option in blender of defining tiles by amount rather than pixels.

Blender used to have a useful option to be able to divide your image into render tiles by specifying 'x' and 'y' values. E.g. 4 'x' tiles and 4 'y' tiles would result in the render being divided into 16 equal parts. While less useful with GPU rendering, where the size of the tile is more important than how many tiles, this still remains useful for CPU rendering whereby you might want to make sure tiles were even in size so that all cores were more likely to do an even amount of work. 

However, this option was later removed in favour of defining the tile size by pixels, which can often lead to small 'slices' of tiles being present at the sides of a render if your pixel-defined tile doesn't perfectly multiply up to the width or height of the image, e.g. a 512 x 512 pixel-defined tile cannot pefectly multiply up to a 1280 x 720 render. This would result in 2.5 x 1.4 tiles.

Of course, I may not be correct about it being more optimal to render evenly sized tiles, but I certainly do prefer to think about dividing my render into, for example, thirds (3 x 3 tiles) than try to work out the equivalent in pixels.

This addon restores this ability by placing two new properties in the 'Performance' panel of the 'Render' tab, 'x tiles' and 'y tiles'.
