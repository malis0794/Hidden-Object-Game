# Hidden-Object-Game
This is my first web game created using HTML, CSS and JavaScript.

The body of the HTML contains all the elements you would see in the game: the meter (to show how far you are from the object), the score box, the “x” and “y” coordinates and the number of objects in the game. Moreover, the body tag declares that the “init” function will be called when the game is loaded, this will run the code between the HTML tags when the game is loaded. This body function enables you to see the elements in the game when playing it e.g. NumbOfObjects.

The style contains all of the positioning, size, border and font of the elements that you see in the game. In addition, the style tag is important in the code since you couldn’t make the game look neat and not get squashed together without it. Henceforth, the style function is to style the game so that everything is not squashed together and that the game matches the design i have drawn.

The script contains all of the javascript code that programs the game elements so that it could actually work. Furthermore, the script tag enables the user to play the game with the elements working as they should, for example the “x” and “y” coordinates change when you use the arrow keys.

The function(s) of the game is the main part that makes the game work. It contains all of the javascript code that makes each element work in the game. Moreover, the functions process everything that happens in the game. The functions are important because without it the game can’t work.

The variables stores most of the data of the game that helps to process things easily and enables us to easily change the value or code of the elements. This is important because it helps us to change the value and code of anything in the game, hence it makes it easier to put the code, of something we created, into another part of code without wasting lines of code and much quicker than it would take without the variables.

Some detail on the Game implementation:
The init function is invoked once the html page has been loaded. This function perform the following actions:
  - It initialise the various page components: x,y positions, initial score
  - it creates an empty grid of hidden objects

The number of object component (NbObjects) registers the NbObjectUpdate function that is called every time the user change the number object. This function populate the grid of hidden object with the given number of of object that the user entered in the NbObjects components randomly located. 

Every time a key is pressed the onKeyPress is invoked with the pressed key object as argument.
When a key is pressed, the x,y positions is updated based on the key that is pressed. When the x,y positions are updated, the DistanceToNearest updates based on where the HiddenObject is and what the x,y positions are.

Every time the x,y position gets updated the dist_closest finds the nearest distance to an object based on the x,y positions. Moreover, when the dist_closest updates its value it updates the distanceMeter’s value depending on its own value. This increases or decreases the green meter you see on the game.

When the user updates the nbObjects the createHiddenObjects function creates random objects on the grid depending on the amount of objects created. The createHiddenObjects allows the distanceMeter to be updated because it gives it an object to base its find_closest(x,y).distance on. If the closest object has a distance of zero then it increases the score and removes the object from the grid.

When the objects are removed from the game (grid) then the player has won.








