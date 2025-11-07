Project: zuul-bad
Authors: Michael Kölling and David J. Barnes

This project is part of the material for the book

   Objects First with Java - A Practical Introduction using BlueJ
   Seventh edition
   David J. Barnes and Michael Kölling

This project is a simple framework for an adventure game. In this version,
it has a few rooms and the ability for a player to walk between these rooms.
That's all.

To start this application, create an instance of class "Game" and call its
"play" method.

This version of the game contains some very bad class design. It should NOT
be used as a basis for extending the project without fixing these design
problems. It serves as an example to discuss good and bad design (chapter 8
of the book).

Chapter 8 of the book contains a detailed description of the problems in this
project, and how to fix them.

The project 'zuul-better' contains a version of this project with better
designed class structure. It includes the fixes discussed in the book.

Answers: 

1- It creates a text based game where users can walk around some scenery.
   Go: It enables you to move in a direction where you indicate (east,west,south,north).
   Quit: It enables you to quit the game.
   Help: It shows you the command words.
   5 rooms: outside, theater, pub, lab, office;
   
2- Game: Creates and initialises all the others: it creates all rooms, creates the parser and starts the game. It also evaluates and executes the commands that the parser returns.
   Parser: This parser reads user input and tries to interpret it as an "Adventure" command. Every time it is called it reads a line from the terminal and tries to interpret the line as a two word command. It returns the commandas an object of class Command.
   Command: This class holds information about a command that was issued by the user. A command currently consists of two strings: a command word and a second word (for example, if the command was "take map", then the two strings obviously are "take" and "map").
   CommandWords: This class holds an enumeration of all command words known to the game. It is used to recognise commands as they are typed in.
   Room:A "Room" represents one location in the scenery of the game. It is connected to other rooms via exits.  The exits are labelled north, east, south, west.  For each direction, the room stores a reference to the neighboring room, or null if there is no exit in that direction. 


   

