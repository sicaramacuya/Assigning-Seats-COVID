# Assigning Seats COVID

## Table of Content
* [Introduction](#Introduction)
* [Motivation](#Motivation)
* [Implementation](#Implementation)
    * [Assumed measurements](#Assume-measurements)
    * [Classes](#Classes)
* [Illustrations](#Illustrations)
    * [Coliseum](#Coliseum)
    * [Stands](#Stands)
* [Technologies](#Technologies)
* [Project Status](#Project-Status)


## Introduction
The objective of this project is to automate the decision making of sitting people on a coliseum. The catch is that people need to be seated 6 feet apart, as recommended by the World Health Organization (WHO) and the Center of Disease Control and Prevention (CDC). In the case there is a group of people that want to be seated they all are going to be seated together and the next group or person is going to be 6 feet apart.

## Motivation
The motivation came from two places:
* This project was my last assignment of the CS 1.1 - Object Oriented Programming (OOP) class. I had the liberty of choosing anything to work on but I needed to implement an OOP design.
* Little before starting CS 1.1 I was talking with a friend and this idea came of sitting people on a coliseum with 6 feet apart of each other. He don't have the knowledge to program the solution and I just didn't had enough time. Then this opportunity where I can test my skills and also do something meaningful came. So, I took the challenge!

## Implementation
I'm sure there are countless ways to approach this problem, but I went with an Object Oriented Program (OOP) design. There are several classes, that are going to be explain briefly further down, which manipulate different pieces of the program.

To approach the problem I decided that there are going to be what I called buffer rows. This buffer rows just represent individual rows that are not going to be occupied because a distance of 6 feet will be needed. In this project I assume some measurements, shown further down, to complete the project.

From this measurements we can conclude that the buffers rows that are going to be needed are 3. Also, we can conclude that 4 seats are going to be needed to separate one person or group from another in the same row.


### Assumed measurements:
* Seats: 
    * 20x20 inches
* Legroom:
    * 20 inches

### Classes:
* Terminal
    * Manage everything from sitting the people to creating a coliseum, stands or pods. It has also features like getting reports of the entire coliseum.
* Coliseum
    * A Coliseum will have instances of other classes, classes that will represent stands. This is better know as composition. 
* Stand
    * The Stand is an abstract class. An abstract class can't be instantiated. A programmer can only create other classes that inherit from an abstract class and those classes can be instantiate. This class is to honor the DRY principle (Don't Repeat Yourself).
    * Classes that inherit from Stand:
        * BoxStand
        * GrandStand
        * TelescopicStand
* Pods
    * Pods are the name that I choose to give to the group of seats. The way I choose to represent each seat was as matrixes but there is a drawback when the stands in a coliseum are not rectangular or squares. A drawback that I need a solution but for now the code is good enough, just for now.


## Illustrations
### Coliseum
Using this coliseum I model the program and found problems and solutions. As I said before, there are some problems I have to find solutions but as of right now the program can create a coliseum, stands and sit people but the stands have to have a rectangular shape.

<img width="757" alt="Coliseum - Seats Configuration" src="https://user-images.githubusercontent.com/69913812/102847466-50269680-440a-11eb-8712-f9e1aac165b9.png">

### Stands
After creating stands and pods like "Pod #1", in the image below. The program will set some rows as Buffer Rows as seen in "Pod #2". After all this depending on the amount of people that want to be seated together, as a group. The program will seat them and seat the next group with 6 feet apart as seen in "Pod #1".

![Lateral Grand Stand](https://user-images.githubusercontent.com/69913812/102842837-cd98d980-43ff-11eb-9f8f-9b403cca3346.jpg)



## Technologies
* Python 3.8

## Project Status
The project right now is on standby, but I do planned to keep innovating it. 

Add more features like storing the coliseum, report to the person using the terminal the actual seats used to seat the person or group and work with the "irregular" stands, the ones that are not rectangular or square's shape.