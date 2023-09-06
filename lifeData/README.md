The text below explains how to add an example or a theme.

First you need to fork https://github.com/JackV2020/appDataTest, 
next make your local changes like described below
and finaly create a pull request for me.

There are 2 methods to add an example.
The difference is the way the cells are described.
Both methods ask you to create a file with 1 required field 
and add that file to all_examples.json.

 Example method 1 : "Text"

 1) Start on the Preset screen of your Toon and click '3 x 3'.
    Next select "Glider" and switch to the Life screen.
    On the Life screen click "No Clicks/Click Cells" so you see the grid.
    Select the theme Black/White.

 2) Think there is a rectangle exactly around the live cells.
    It is 3 rows and 3 columns. So not the full screen.
    The upper left cell in your rectangle is just to the left of the 
    upper cell which is alive. 
    This cell which is not alive has row,column coordinates 0,0.

 3) For each row write down a series of dots (dead cells) and zeros (live cells).
    For the example this would be :
    <br>.0.
    <br>..0
    <br>000
    
 4) Copy example_glider.json to example_<some_descriptive_name>.json.
    
 5) Put the rows in 1 string and seperate the rows by a space like :
    ".0. ..0 000" and use this for the Text field in your file.
    "Text" is the only required field. Optional fields are described below.

 6) Add your entry at the top of all_examples.json.
    The 3 fields Type, Name and file are required fields.

 Example method 2 : "Array"

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

 4) Copy example_captured_cross_fixed.json to example_<some_descriptive_name>.json

 5) Put the coordinates in 1 array like you see in the file you just copied : 
    [[0,1],[1,0],[1,1],[1,2]] and use this for the Array field in your file.
    "Array" is the only required field. Optional fields are described below.

 6) Add your entry at the top of all_examples.json. 
    The 3 fields Type, Name and file are required fields.

Optional fields of example_<some_descriptive_name>.json :

    Type : T1 | T2 , T1 for Toon 1 and Toon 2, T2 for Toon 2 only. 
            T1 restrictions performance and size max 33x33, Toon 2 size 51x51
    Name : text which comes up in the pull down menu
    WrapMode : true | false     , true makes it wrap, false causes closed walls
    MinRowsCols : [r.c]         , sets the minimum number of rows and columns
    SetRowsCols : [r,c]         , sets the exact number of rows and columns
    Speed : 1..9                , sets the speed
    PreferredTheme : theme name , Name of theme (see all_themes.json)
    Positioning : [ [r,c,rdir,cdir] [ [ , [r,c,rdir,cdir] ] , [r,c,rdir,cdir] .....] ]
        array of 1 or more arrays describing where to position and in which direction to build
        the construction. An example is in example_4_gliders.json.

 To add a Theme you want to know how to build it and send it to me :

 1) To get started you open theme_black_white.json.
    
 2) Select the Black White theme on your Toon and compare with what
    you see in the file. Use "No Clicks/Click Cells" so you see the grid.

 3) Do the same for some themes to get an idea of what is possible and what
    values you may need for your theme.

 4) Copy any theme file to theme_<some_descriptive_name>.json and put
    your idea in. All fields are optional but I advise to use them all
    to avoid surprises from the theme the user selected before your theme.

 5) Add your entry at the top of all_themes.json
    The 2 fields Name and file are required fields.
