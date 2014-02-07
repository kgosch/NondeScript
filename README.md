NondeScript
===========

![So Interesting](http://static.tvtropes.org/pmwiki/pub/images/nondescript_4147.jpg "So Interesting")

Summary
===========

  non·de·script: adjective
  1. lacking distinctive or interesting features or characteristics.

This language is intended to operate and appear in such a way that it blends into one's mind. Writing it should not feel like writing code, but rather like talking to the computer as you would a person, telling it what to do in a natural feeling way (for engish speakers at least!). It does come across as slightly more verbose and some choices for its syntax and grammar may seem strange, but too bad! If it feels nice to write, then mission accomplished.

All examples have NondeScript on the left and JavaScript on the right.

**The Basics**

When doing the basic "hello world" example, you want the computer to display those words, so simply type...

            display "Hello World";                                    console.log("Hello, World");

As you can see, semicolons are used at the end of statements. This is because it feels "safe" and very distincly shows where a statement ends. You wouldn't start leaving the periods off of sentences in a novel now would you?

**Declaring and Assigning Variables**

To declare a variable, you type 'declare'. To say a varible is something, you type 'is'. Pretty simple really...

            declare x;                                                var x;
            declare y is 5;                                           var y = 5;
            x is "cool";                                              x = "cool";
            
Variables can be declared with out being initialized and types are not required, as NondeScript uses dynamic typing.



repo for the NondeScript compiler project
