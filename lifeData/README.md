 To add an Example you want to know how to build it and send it to me :

 1) Start on the Preset screen of your Toon and click '3 x 3'.
    Next select "Captured Cross" and switch to the Life screen.
    On the Life screen click "No Clicks/Click Cells" so you see the grid.
    Select the theme Black/White.

 2) Think there is a rectangle exactly around the live cells.
    It is 2 rows and 3 columns. So not the full screen.
    The upper left cell in your rectangle is just to the left of the 
    upper cell which is alive. 
    This cell which is not alive has row,column coordinates 0,0.

 3) Column numbers count up when going to the right.
    BUT note Rows numbers count UP when going DOWN.
    The live cell on top has coordinates 0,1 because it is in column 1
    1 Row lower is row 1 with 3 cells :  1,0  ;  1,1  ;  1,2 
    Coordinates are what you need to describe your example.

 4) To build and test your example you can resize the screen on the
    Presets screen, then go to the Life screen and select Wall or Wrap
    mode and click "No Clicks/Click Cells" so you see the grid.
    Click Clear to clear the screen and start clicking the cells.
    When ready...
    Note the coordinates of the cells or make a picture with your phone.
    Click Start Life to test and repeat until ready.

 5) Put your example in lifeData.json in my github in 
    https://github.com/JackV2020/appDataTest/tree/main/lifeData (fork, add, PR etc.)
    The first entry is "CommentsExamples" and is about all the fields.
    You may want to check "Captured Cross" which you checked in 3).
    This is one of the few using SetRowsCols. The Positioning is
    [1,1,1,1]. First 1 puts the composition on row 1, second 1 puts it
    on column 1. Third 1 makes rows to be added downwards and fourth 1
    makes columns be added to the right. You may also want to check
    the positioning of "3 Small Spaceships" which uses different numbers
    and also a -1 for the row direction.

 To add a Theme you want to know how to build it and send it to me :

 1) To get started you open lifeData.json in
    https://github.com/JackV2020/appDataTest/tree/main/lifeData
    and find the section "CommentsThemes"
    
 2) Select a theme on your Toon and compare whith what it looks like 
    in the section "lifeThemes" in lifeData.json. 
    Do this for some themes to get an idea of what is possible and what
    values you may need for your theme.

 3) Put your theme in the right section in lifeData.json in 
    https://github.com/JackV2020/appDataTest/tree/main/lifeData.
    (fork, add, PR etc.)
