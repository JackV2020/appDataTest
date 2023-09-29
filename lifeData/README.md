The text below explains how to add an example or a theme.

The easiest way, for you ;-) that is, is to open an issue at https://github.com/JackV2020/appDataTest
and describe what you want me to add.

Keep in mind that the size limits for Toon 1 are 31 x 31 cells and for Toon 2 61 x 61 cells

However, you may want to do it yourself.....

First you need to fork https://github.com/JackV2020/appDataTest, 
make your changes like described below
and create a pull request for me.

There are 3 methods to add an example.
The difference is the way the cells are described.
All 3 methods ask you to create a file with 1 required field
and add that file to all_examples.json.

 Example method 1 : "Array"

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

 Example method 2 : "RLET" (based on standard RLE)

 1) Start on the Preset screen of your Toon and click '3 x 3'.
    Next select "Blinker" and switch to the Life screen.
    On the Life screen click "No Clicks/Click Cells" so you see the grid.
    Select the theme Black/White.

 2) Think there is a rectangle exactly around the live cells.
    It is 1 row and 3 columns. So not the full screen.
    The upper left cell in your rectangle is the upper left cell and
    it is alive.
    This cell which is alive has row,column coordinates 0,0.

 3) The RLE standard part used are :
    <br>[count]o    for live cells like 3o for 3 live cells
    <br>[count]b    for dead cells like 14b for 14 dead cells
    <br>[count]$    to end a row and to skip rows like 3$ to end and skip 2

 4) Copy example_wasp.json to example_<some_descriptive_name>.json.

 5) Put the rows in 1 string and seperate the rows with $'s like
    "3o8$3b3o" and use this for the RLET field in your file.
    "RLET" is the only required field. Optional fields are described below.

 6) Add your entry at the top of all_examples.json.
    The 3 fields Type, Name and file are required fields.

 Example method 3 : "PTA" (based on standard Plaintext)

 1) Start on the Preset screen of your Toon and click '3 x 3'.
    Next select "Glider" and switch to the Life screen.
    On the Life screen click "No Clicks/Click Cells" so you see the grid.
    Select the theme Black/White.

 2) Think there is a rectangle exactly around the live cells.
    It is 3 rows and 3 columns. So not the full screen.
    The upper left cell in your rectangle is just to the left of the
    upper cell which is alive.
    This cell which is not alive has row,column coordinates 0,0.

 3) For each row write down a series of dots (dead cells) and characters (live cells).
    For the example where I use a '0' as character this would be :
    <br>.0. <- dead cell at the end of the row
    <br>..0
    <br>000
    <br>Note that dead cells at the end of a row are not required.

 4) Copy example_glider.json to example_<some_descriptive_name>.json.

 5) Put the rows in the PTA array like you see in the file you copied :
    <br>,"PTA":[ 
    <br>[".0."],
    <br>["..0"],
    <br>["000"]
    <br>]
    <br>"PTA" is the only required field. Optional fields are described below.

    About dead cells and empty rows.... If you want to you can leave out
    dead cells at the end of a row and use [""] for an empty row.

 6) Add your entry at the top of all_examples.json.
    The 3 fields Type, Name and file are required fields.

Optional fields of example_<some_descriptive_name>.json :

    Name : just a descriptive text which you could keep the same as in all_examples.json
    WrapMode : true | false     , true makes it wrap, false causes closed walls
    MinRowsCols : [r.c]         , sets the minimum number of rows and columns
    SetRowsCols : [r,c]         , sets the exact number of rows and columns
    Speed : 1..9                , sets the speed
    PreferredTheme : theme name , Name of theme (see all_themes.json)
    Positioning : [ [r,c,rdir,cdir] [ [ , [r,c,rdir,cdir] ] , [r,c,rdir,cdir] .....] ]
        array of 1 or more arrays describing where to position and in which direction to build
        the construction. An example is in example_4_gliders.json.
    All other fieldnames are ignored so you could add :
        "Comment":"Just some comment about this creation"

 To add a Theme you follow the next steps :

 1) To get started you open theme_black_white.json.

 2) Select the Black White theme on your Toon and compare with what
    you see in the file. Use "No Clicks/Click Cells" so you see the grid.

 3) Do the same for some themes to get an idea of what is possible and what
    values you may need for your theme.

 4) Copy any theme file to theme_<some_descriptive_name>.json and put
    your idea in. All fields are optional. I advise to use them all
    and not fall back on default values.

    Default value for all colors "transparent", text values "", PixelSizes 1 and other numbers 0.

    Also here you can add other fields which will all be ignored like :
        "Comment":"Just some comment about this creation"

 5) Add your entry at the top of all_themes.json
    The 2 fields Name and file are required fields.
