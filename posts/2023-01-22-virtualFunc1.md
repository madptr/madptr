---
title: "Virtual Functions I"
date: 2023-01-22T16:45:51+05:30
description: A dive into virtual functions
tags: [CPP, virtual function, programming]
---

Have you ever come across the keyword `virutal` in CPP and felt that you haven't fully understood it yet?
In this post, I'll try to explain one basic use case where `virtual` really helps us. 

Just consider we have two types a `Player` and an `Enemy`.

```c++
class Player {
    // members and methods
};

class Enemy {
    // members and methods
};
```

Here, all the `Enemy` and the `Player` objects cannot be stored under a variable of some type. 

```c++
<what_type_is_items?> items [] = {
    Player(),
    Enemy(),
    Enemy()
}

```
Sure we cannot do something like the above, thus we will have to maintain a variable for each type we create. Consider making a roguelike game, with 100s of monster types, as a programmer we will be lost in the sea of variables. For ease of handling and to improve the flexibility of the program, we derive them from a common base type.

```c++
class Actor {
    // common members and methods
};

class Player : public Actor {
    // local/unique members and methods
};

class Enemy : public Actor {
    // local/unique members and methods
};
```

Eventually, we can do the following and access all the types without worrying about their base type.

```c++
int main(){
    Actor* actors [] = {
        new Player(),
        new Enemy(),
        new Enemy()
    };

    for(auto a : actors){
        a->doStuff();
    }
}
```
Here, `actors` can hold all the variables of different types using the reference to the base type from which they are derived. 
Each item, be it a `Player` or an `Enemy`; will be referred to using the reference of the base type.
How sure are we that all the objects in the array `Actor` have a method `doStuff()`? If the compiler figures out that this function call is not valid i.e. there is no method to call at this point, it will generate a compiler error. Ideally, it is not a problem at all. 

What if some `Actor` behaves differently? Let's consider we have a type called `Car`.

```c++
class Car : public Actor {
    // local/unique members and methods in relation to Actor
    ...
    // common members and methods related to Car
    int getNumDoors();
    // other common members and methods related to Car
};

class Fiat : public Car {
    // local/unique members and methods
};

class RangeRover : public Car {
    // local/unique members and methods
};
```
*Note: Here `Fiat` and `RangeRover` are also a type of `Actor` because they inherit the `Actor`'s properties via `Car` which is derived from the `Actor`.*

Since all the cars in our game are going to have 4 doors, let us consider we have implemented it in the base class's scope, and it returns `4`. 
Now, we got to introduce a sports car into the game. 
Alas! the `getNumDoors()` of the `Car` is defined to return 4 doors only! 
Now, we have a few options ahead.

1. Introduce a variable `numDoors` in the base class and set its value, maybe via a constructor.
2. Move the `getNumDoors()` function from the base class to the derived classes.
3. Introduce virtual function.

*Note: If you feel **option 1** works perfectly fine, it must be because of my bad example. Handling one integer is easy. Assume the integer is a placeholder for a problem bigger than an integer.*

While the first two methods are bound to work fine, it demands a lot of code refactorings. This is where the **virtual function** comes to the rescue. 

```c++
class Car : public Actor {
    // local/unique members and methods in relation to Actor
    ...
    // common members and methods related to Car
    virtual int getNumDoors(){ return 4; }
    // other common members and methods related to Car
};

class Fiat : public Car {
    // local/unique members and methods
};

class RangeRover : public Car {
    // local/unique members and methods
};

class SuperCar : public Car {
    // local/unique members and methods
    virtual int getNumDoors(){ return 2; }
};

void main() {
    Car* cars [] = {
        new Fiat(),
        new RangeRover(),
        new Car()
    };

    for(auto c : cars){
        c->getNumDoors();
    }
}
```
Virtual functions enforce the compiler to link to the definition of a derived type if exists. This is a very useful feature at times like this.

To be continued...