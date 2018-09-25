# Your first Level

Click on *Level Editor* from the title menu. Then *New level subset*. Give it a name and click *OK*. To make your first level click on *New level* and for the sake of free software we will release our level under [CC-BY-SA](https://creativecommons.org/licenses/by-sa/4.0/).

## The Interface

The panel on the right side is the place where you get all of your blocks (*Tilegroups*) and enemies (*Objects*) into your level. With the bottom panel you can easily switch between the tile maps (let 0 enabled for now – we will cover that later) and change background, music and the size of your sector.

When you press <kbd>ESC</kbd>, you can play and save your level and exit the editor. You can move the viewport of your level with the arrow keys. Use this to navigate through your level.

## Build a basic Level Framework

### Define the Theme of your Level

Do you want to make a forest level or an underground level or a sky level? You should have a plan for your level **first** before you start adding tiles. Everything should suit your level theme:

#### The Music

Left click on *Sector: main* at the bottom left, choose *Sector Settings* and *Music*. There is great track list to choose from. I will help you choose:

- **Antarctica:** chipdisko.ogg, voc-daytime.ogg, voc-daytime2.ogg
- **Sky:** airship_remix.ogg
- **Castle:** fortress.ogg
- **Cave:** cave.ogg, voc-dark.ogg
- **Ice Bridge:** wisphunt.ogg
- **Forest:** forest.ogg, forest2.ogg, forest3.ogg
- **Forest Castle:** fortress.ogg, darkforestkeep.ogg
- **Halloween/Ghostforest:** ghostforest.ogg, ghostforest2.ogg, greatgigantic.ogg

#### The Background

![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/background.png) Right click this icon in the bottom panel. You can change the top, middle and bottom of the background separately, which allows you to mix certain images. Since this is also a complete mess, I suggest you to open `/usr/share/games/supertux2/images/background/` with your file manager on Linux and pick your images there (Windows users may find this somewhere in `%AppData`). Then you can define top, middle and bottom in the editor.

#### The Ambient

If you go for a ghostforest-themed level or just want to make your level look more interesting, you can add a ambient in *Objects* > *Ambient*. The options you have include:

![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/ghostparticles.png "ghost particles")
![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/rain.png "rain")
![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/thunderstorm.png "thunderstorm")
![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/snow.png "snow")
![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/clouds.png "clouds")

Click on one of these icons in the editor, then click on the level window. The ambient will be added to the bottom panel and is activated instantly.

### Let’s get started

What are the requirements for every level?

1. A Sector called *main* (we already have this – Tux will start in this sector)
2. A Spawn point called *main* (we already have this – Tux will start the level from this point)
3. Something for Tux to walk on
4. A Goal

Now we want to work on point number 3.

#### Adding Tiles

Click on Tilegroups in the top-right corner and choose a category that suits your level theme (in *Block* are tiles you need for every level). Select a tile you like by clicking on it or select multiple tiles by dragging a rectangle with your mouse. Your selection is now displayed besides the cursor. You can place it in your level as many times as you want.

![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/Editor-AddingTiles.gif)

- By right clicking on a tile you can copy it. It is also possible to copy a whole area by dragging a rectangle with your mouse.
- The red rectangle![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/select-mode0.png)is the normal insert tool. By clicking this icon you can switch tools.
- With the green rectangle![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/select-mode1.png)you can fill rectangular areas.
- The bucket fill tool ![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/select-mode2.png)lets you fill the air tiles framed by blocks with another tile. Be careful with this tool! The editor has no undo button – so keep in mind to save your levels regularly!
- If you have nothing in your selection the tools work as erasers.
- You can clear your selection with the rubber ![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/rubber.png)or by copying an air tile.
- Clicking the wrench ![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/settings-mode0.png) invokes the same menu as pressing the <kbd>ESC</kbd> key.
- This arrow ![](https://raw.githubusercontent.com/Ordoviz/wiki/master/images/move-mode0.png) only takes affect for objects. It has no use for tiles.

#### Adding the Goal

A SuperTux level usually ends like this:

![goal with igloo](https://raw.githubusercontent.com/Ordoviz/wiki/335563cad2d1c28c7674e2a5c886c86b323aec92/images/Editor-Goal.png)

To make the goal poles, go to *Tilegroups* > *Misc*. For the first pole you have to switch to tile map *&minus;100*. Then you can draw the pole. For the second pole you have to switch to tile map *+100*. Then you can draw the pole. Like this we have one pole in the background and the other one in the foreground which creates this cool 3D effect.

To make the igloo, go to *Tilegroups* > *Exits*. Tux’ Igloo is split up into two parts to make it look more 3D. Select the first part and paste it in tile map *&minus;100*. Then select the second part and paste it in tile map *+100*.

Now we are done visually but we still have to tell the game where the level ends. Go to *Objects* > *Ambient* and select ![Seq. Trigger](https://raw.githubusercontent.com/Ordoviz/wiki/335563cad2d1c28c7674e2a5c886c86b323aec92/images/Sequencetrigger.png). We are adding a object now. Objects work a little different than tiles. See the detailed explanation below when you have problems. Click on the level window and place the sequence trigger like shown in the picture. I suggest you to press <kbd>f7</kbd> to enable “Snap objects to grid”. Make sure the first sequence trigger triggers the action “end sequence“ You can change this by right clicking on the object. The sequence trigger in the igloo is used to prevent Tux from walking farther right out of the igloo. Make sure its action is set to “stop Tux”.

Congratulation! You have got everything you need for your first level. Now it is time to be creative and build your level. You can come back to this guide at any time and look up your specific problems. What do you want to do next? Add particular kinds of objects, use secret areas or work with multiple tile maps? It’s your choice!

# Adding Objects

TODO

# Working with multiple Tile Maps

TODO

# Working with Lightmaps

TODO

# Making a Worldmap for your Levels

TODO

# Making an auto-scrolling Level

TODO

This page is licensed under [CC-BY-SA](https://creativecommons.org/licenses/by-sa/4.0/).