# Compiler

A simple custom-generated code compiler made with C Bison and Flex, for the Formal Languages ​​course

### Author
* Alejandro Fajardo  

## Commands


To compile run: 

```bash 
./build
``` 

to evaluate code run
```bash 
./main.exec CODEFILE.jaja  
```

where CODEFILE is the name of the file you want to evaluate

## Reserved Words

~~~
FOR:  		                      for | FOR			
DO: 		                          do | DO
WHILE: 		                    while | WHILE	
FUNCTION: 	              function | FUNCTION	
IF: 		                          if | IF
ELSE:		                        else | ELSE
BREAK: 		                     break | BREAK
IN: 		                           in | IN
RETURN: 	                    return | ->
PRINT		                          printline|PRINTLINE
~~~

## Symbols

| Simbolo | Nombre | Uso                                                                         |
|---------|--------|-----------------------------------------------------------------------------|
| =       | Equals  | Variable assignment.                                                    |
| >>      | Range  | It is used in a for to indicate the range in which you want to iterate. |
 | =+     | Equals Plus| Add the value on the right to the value on the left of the symbol. |
|=- | Equals Minus | Subtract the value on the right from the value on the left of the symbol. |
|++ | Plus Plus | Increase 1 in the variable on the left. |
|-- | Minus Minus | Decrease 1 in the variable on the left. |
|- | Minus | Subtraction operation. |
|+ | Plus | Addition operation. |
|* | Product | Product operation. |
|% | Module| Module operation. |
|/ | Division | Division operation. |
|/^ | Raised | Operation of raising one value by another. |
|== | Comparison | Compares whether parameters are equal. |
| != | Different | Compare if parameters are different. |
| > | Greater than | Compares whether the parameter on the left is greater than the parameter on the right. |
| < | Less than | Compares if the parameter on the left is less than the one on the right. |
| >= | Greater than equal to | Compares whether the parameter on the left is greater than or equal to the parameter on the right. |
|<= | Less than equal to | Compares whether the parameter on the left is less than or equal to the parameter on the right. |
|\| | Or | Checks that at least one parameter, the one on the left or right of the symbol, is true. | 
|&& | And | Checks that both left and right parameters are true. |
|-> | Return | Symbol used to return a data type in a function, (the reserved word return can also be used). |
|, | Separator | Symbol to separate different parameters. |


## Delimiters

Punctuation in parentheses is used in various parts of grammar. a parenthesis open must always be paired with a closed parenthesis.
Parenthesis Type

* {  } Keys.
* [  ] Brackets.
* (  ) Parentheses.


## Type of data.

The different types of data supported by “Jaja” are listed below.

### Boolean.


The bool type is a data type that can be true or false. It is used in comparisons and operations like &, |.
```java
​var​ ​bool​ x = ​true
​const​ ​bool​ y = ​false
```
### Numeric types

#### Int

Negative and positive integers, from -99999999999999999999 to 999999999999999999999999999999.
```java
​var​ ​int​ x = ​ 1
​const​ ​int​ y = ​ 2
```
#### Long

Negative and positive integers, from -9999999999999999999999999999999999999999 until 9999999999999999999999999999999999999999999999999999999999.
```java
​var​ ​lng​ x = ​ 1
​const​ ​LNG​ y = ​ 2
```
#### Float

Negative and positive real numbers, from 0 to
99999999999999999999999999999,9999999999999999999999999999.

```java
var​ ​flt​ x = ​ 1
const​ ​FLT​ y = ​ 2
```
### Textual data


The char and str types contain textual data.
The char data types only accept one character and the str data types have a maximum length
2,999.

```java
​var​ ​char​ x = 'a'
​const​ ​str​ y = "example"
```
## Fuctions

A function consists of a block, along with a name and a set of parameters.
Other than the name, the parameters are optional. Functions are declared with the
keyword function or FUNCTION. Functions can declare a set of
input variables as parameters, through which when invoked they must be
pass arguments to the function, and the output type of the value that the function will return to the
Finally, these can be of simple and extended type
Simple functions designed for those functions without a return or empty return,
extended functions include a return data type associated with their result

```java
function​ ​save_person​ (​int​:age,​str​:name,​char​:gender){

}
```

```java

function​ ​save_person​ (​int​:age,​str​:name,​char​:gender) ​-​> ​str​ {

}
```

## Loops.

Below is the use of loops or cycles in the language.

### For

A for is a syntactic expression to loop over the provided elements.
For example.
```java
var​ ​int​ ​sum​ = ​ 0
for ​n​ in ​ 1 ​ >> ​ 11 ​ {
    sum​ =+ ​ 1
}
```

### while

A while loop begins by evaluating the conditional expression of the boolean loop. If the
loop conditional expression evaluates to true, the loop body block is
executes, and then the control re-evaluates the conditional expression in the loop. If the
The loop's conditional expression evaluates to false, the while expression completes.
For example.
```java
var​ int ​i​ = ​ 0
while(​i​ < ​10)​ {
    i​ =+ ​ 1
}
```
### Do While

A ​do​ ​while​ loop begins by executing the body block of the se loop and then evaluating
the conditional expression of the boolean loop. If the loop's conditional expression is evaluated
as ​true​, the loop body block is executed, and then the control re-evaluates the
loop conditional expression. If the loop's conditional expression evaluates to false,
the while expression completes.
For example.
```java
var​ int ​i​ = ​ 0
do {
  i​ =+ ​ 1
} while ( ​i​ < ​ 10 ​)
```
## if else

An if expression is a conditional structure in program control. The shape of a
if expression is a condition expression, followed by a consequent block. The
Condition expressions must have to be boolean. If a condition expression is
evaluates to true, the consecutive block and any subsequent ones are executed. Yes one


condition expression evaluates to false, the block inside the if is skipped and if you have a
else the code block is executed within it, then the program continues if
evaluates the condition.
For example.
```java
if​ ( ​i​ == ​ 1 ​){
    i​ = ​ 10
} ​else​ ​if​( ​i​ == ​ 2 ​){
    i​ = ​ 20
} ​else​ ​if​( ​i​ == ​ 3 ​){
    i​ = ​ 30
} ​else​ ​if​( ​i​ == ​ 4 ​){
    i​ = ​ 40
} ​else​ {
    i​ = ​ 0
}
```
