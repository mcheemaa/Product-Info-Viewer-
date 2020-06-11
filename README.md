# Product Info Viewer

*Product Info Viewer:*

apireader.py contains a main function and a class window. the class first takes in frame
from tkinter which acts as a container for all other widgets. it then calls the grid and create
functions. the create function reads the image from the gif file first and then sets it on the grid. it
then prints using the label widget and takes in using the entry widget. checkbuttons are then set
to a boolean variable and set onto the screen. the enter button takes in the command from the
update fill and everytime it is pressed it does all the functions in the update fill. the updatefill
function contains all sub functions for the check buttons and makes sure that every time the
submit button is pressed it refreshes the data according to the new or present barcode. it first
deletes all the data and then re calls the functions to print it on the screen. the functions for the
check boxes use the pool manager to define http and then retrieves data from the website in form
of json strings. the json strings are then converted and they consist of dictionaries. they contain if
and elif statement to delete the information if the checkbox is unchecked and put the information
if it is checked using insert. this works the same with all four of the availability, price,
description and name functions. the updatepic function saves the image from the url of the image
retrieved from the api records. the main function makes the main window frame from tkinter and
sets the dimensions to the required pixels using geometry. it also changes the title to the requried
one. the code runs as : python3 apireader.py
