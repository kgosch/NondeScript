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

To declare a variable, you type 'declare'. To say a variable is something, you type 'is'. Pretty simple really...

            declare x;                                                var x;
            declare y is 5;                                           var y = 5;
            x is "cool";                                              x = "cool";
            
Variables can be declared without being initialized and types are not required, as NondeScript uses dynamic typing.

**Loops, While and For**

While loops rely on the 'until' keyword, and For loops use the same sort of set up as JavaScript. Note however that braces are not used, but rather the naked indents show where the loops block is located.

            declare i is 0;                                           var i = 0;
            loop until i is 10                                        while ( i != 10 ) {
                increment i by 2;                                         i += 2;
            end loop                                                  }
            
            
            loop declare i is 0, until i is > 5, increment i          for ( var i = 0; i <= 5; i++ ) {
                display i;                                                console.log( i );
            end loop                                                  }

Also seen here is incrementing number variables, which defaults to '1' when no amount to increment 'by' is given.

**Functions**

Functions 'take' something in and then 'return' something back. Again note no braces.

            function noArguments takes in nothing                     function noArguments () {
                declare x is "everything";                                var x = "everything";
                return x;                                                 return x;
            end function                                              }
            
            
            function withArguments takes in y                         function withArguments ( y ) {
                return y + 3;                                             return y + 3;
            end function;                                             }

When a function takes in no arguments, type 'takes in nothing'. Again, NondeScript should be typed and feel like the actual thing you are trying to make the program do.

**Objects**

TOO DOO


**Syntax**

          Script         ::= Stmt+
          
          Stmt           ::= Declaration
                          |  Increment ';'
                          |  'display'  Exp  ';'
                          |  Assignment ';'
                          |  While
                          |  Call ';'
                          |  ForLoop
                          |  Return ';'
          
          Declaration    ::= VarDec | FunDec
          
          VarDec         ::= 'declare' Id  ('is'  Exp)?  ';'
          
          FunDec         ::= 'function'  Id  Params  Block Return
          
          Increment      ::= ('increment' | 'decrement') Id ('by' Int)?
                    
          Assignment     ::= Id  'is'  Exp
          
          While          ::= 'loop'  Exp  Block
          
          Call           ::= Id  Args
          
          ForLoop        ::= 'loop' (VarDec)? ',' Exp  ','  Increment  Block
          
          Return         ::= 'return' Exp
          
          Block          ::= '    '  Stmt*  'end' ('loop' | 'function')
          
          Args           ::= 'takes in'  ('nothing' | Exp)  (',' Exp)*
          
          Exp            ::= UnaryOp  Exp
                          |  Exp  BinaryOp  Exp
                          |  'until' Exp
                          |  IntLit | StringLit | true | false | Call
          
          UnaryOps       ::= '-' | 'not'
          
          BinaryOps      ::= 'AND' | 'OR' 
          
          ComparisonOps  ::= 'is ('>' | '<') | 'is = OR ('>' | '<') | 'is' | 'is not'
          
          AddOps         ::= '+' | '-'
          
          MultOps        ::= '*' | "/"
          
          Type           ::= Int
                          |  Boolean
                          |  String
                          |  Id
