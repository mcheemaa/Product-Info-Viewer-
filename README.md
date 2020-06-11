# Product Info Viewer

**Product Info Viewer:**

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

**How To Run The Program:**

![image](https://user-images.githubusercontent.com/54610255/84450196-71b5f280-ac1d-11ea-9dfd-437140d4ab73.png)

the program can be started by running it in python by typing python apireader.py. one
thing to note is we need the title picture file to be present in the same folder as the program
which is a gif file named lol. it then requires the user to choose what things they want to view
about that specific product and after they are done checking the checkboxes they should input the
code of the product they want to view and it can be done using a barcode reader or the keyboard
(i have attached a list of sample codes that are present in the walmart api). lastly they need to hit
enter and they will see the output. the image of that product will be saved with the name “pici” in
the same folder that contains the file. after one product and selection is done they just need to
enter the new barcode and hit submit. the picture will be updated in the same file and folder.

![image](https://user-images.githubusercontent.com/54610255/84450220-81cdd200-ac1d-11ea-8568-8ba3fbeb80fa.png)


**Problems Encountered & Future Improvements Or Modification:**

during the course of this program we did various kinds of testing like in the beginning we
only made the program to show the information from the check boxes but it didnt delete when a
new code was entered or the checkbox was unchecked so it added the new information to the
previous one. we then fixed the program to update the information by deleting the previous one
every time the submit button was pressed with a new code. it was also really hard to put the text
boxes and entry widgets in front of the label and check boxes as tkinter had a weird column
spacing and everytime we put a column number of 1 the widget went way far and we were also
unable to use the pack function. we came across the sticky idea of east and west after some time
and before that everything was left aligned. we also tried to add the saved product image and
display it on the screen but apparently the saved image was jpg format even though we saved it
with the name .gif and so it gave the error that python can't open jpg file. another problem was
converting the json strings to usable format and we didn't know about json at first were unable to
read a dictionary as it was just a block of strings. moreover there were various other problems
that i can mention. however, we are looking forward to make plenty of improvements to our
program like giving an option to choose which stores api does the user wants to view and use
checkboxes to use that one. we are also looking forward to find a way to change the jpeg to gif
and open it or somehow open the jpeg product picture in the main window frame. we are also
looking forward to integrate the second part of our project to the first one and instead of
hardcoding the data we are looking to use the prices and availability from the api. i think that this
program has the potential to be improved forever and ever and we can release updates on timely
bases.


**Point Of Sale System:**

customerbill.py consists of a main function. It takes barcode of a product as an input
using the barcode scanner and asks the customer number of quantity of the product they want to
buy. The program consists of lists of barcodes and another lists that has names, price and
quantity in the store corresponding to that barcode. As the user scans an item, the program adds
it to the empty values list of a dictionary inside a separate list called bill.
The program appends name, price and the quantity of the scanned item in the list bill and
asks if the customer wants to buy more. When the customer is done with the purchase, it prints
out the bill in a table form with the grand total. It asks for the amount paid by the user as an input
and shows the amount of change to be returned to the user. This program also keeps track of the
quantity of item in the shop. It decreases the quantity purchased by the customer from the
quantity in the shop and displays a warning message if the quantity in the shops falls below 10.

**How To Run The Program:**

1. Run the program using python customerbill.py.
2. Scan the barcode of the product or enter it using the keyboard.
3. Enter the quantity you want to buy.
4. Enter y if you want to buy more and n if you want the bill.
5. Repeat from scanning the barcode if you chose y.
6. If n , bill will be shown and enter the amount you paid.
7. It shows the change you will be returned.

![image](https://user-images.githubusercontent.com/54610255/84450234-8eeac100-ac1d-11ea-9fd9-75553cb19425.png)


