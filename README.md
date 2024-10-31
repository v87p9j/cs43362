java c




ECS 140A  Fall 2024
Midterm 1 Review
Derivation, Parse Tree, EBNF, Ambiguity, First Sets, Construct a Parser, Java, Semantics
In addition to the following topics, make sure you have studied all the lecture and discussion    slides (everything before functional programming in lecture 9), as well as the relevant textbook chapters.
Table of Contents:
BNF Grammar
Derivation
Parse tree
Ambiguity
Recursion and associativity
EBNF
First sets
Parser
Java
Binding
Scoping
BNF Grammar
This BNF grammar will be used in all of the subsequent review problems.
 ::=  +  |  -  |   ::=  *  |  /  |       ::= num | -num | (  )
Assume num is a terminal symbol and can be 0..9.
Derivation
Show the left-most derivation for 8 - 2 * ( 1 + (-4)). Assume your start symbol is . Is the following derivation correct for 8 - 2 * ( 1 + (-4))?Incorrect.
 ::=  - 
 ::=  -  - 
 ::=  -  - 




 ::= num -  - 
 ::= num -  -  * 
 ::= num -  -  * 
 ::= num -  -  * 
 ::= num - num -  * 
 ::= num - num - (  ) * 
 ::= num - num - (  +  ) * 
 ::= num - num - (  +  ) * 
 ::= num - num - (  +  ) * 
 ::= num - num - ( num +  ) * 
 ::= num - num - ( num +  ) * 
 ::= num - num - ( num +  (  ) ) * 
 ::= num - num - ( num +  (  ) ) * 
 ::= num - num - ( num +  (  ) ) *  
 ::= num - num - ( num + ( - num ) ) * 
 ::= num - num - ( num + ( - num ) ) * num
Parse tree
Show the parse tree for 8 - 2 * ( 1 + (-4))
Ambiguity
Is this grammar ambiguous? Why or why not?
D代 写ECS 140A Fall 2024 Midterm 1 ReviewC/C++
代做程序编程语言oes + and - have higher or lower precedence than * and / in this grammar?
Recursion and associativity
Are there left recursions or right recursions in the grammar? Left associative or right associative?
EBNF
Convert the grammar to EBNF.
First sets
Compute the ﬁrst sets for all non-terminal symbols based on EBNF.


Parser
Based on the EBNF grammar and ﬁrst sets you created, construct a simple parser like the
example we went through in lecture and discussion. Assume you have access to next(), error(), f_X, and sym.
Java
Implement a basic StringManipulator class in Java with methods to reverse a string,
convert a string to uppercase, and check if a string is a palindrome. Make sure you use correct data types. Here is a sample test class that will be used to test your StringManipulator
class.
public class StringManipulatorTest {
public static void main(String [] args) {
StringManipulator manipulator = new StringManipulator (); //
create a new StringManipulator instance
String riginal = "level";
String reversed = manipulator.reverseString (original);
System.out.println ("Reversed string: " + reversed);
// Should print: Reversed string: level
String uppercase = manipulator.toUpperCase (original);
System.out.println ("Uppercase string: " + uppercase);
// Should print: Uppercase string: LEVEL
boolean isPalindrome = manipulator.isPalindrome (original);
System.out.println ("Is palindrome: " + isPalindrome);
// Should print: Is palindrome: true
}
}
Binding
Given the following simple assignment statement in C++:
`a = b + c;`
The statement contains the following components:
- Identifies: a, b, c
- Operators: =, +
For each component of the statement, list the various bindings that are required to
determine the semantics when the statement is executed. For each binding, indicate the binding time used for the language. Explain your answer.
Scoping
Consider the following program. If static scoping is in use, what is written?
begin
integer x;
procedure f;
begin
x = x + 3;
end
x = 20;
begin
integer x;
x = 10;
f;
write x;
end
f;
write x;
end
Consider the following program. If dynamic scoping is in use, what is written?
begin
integer x;
procedure f;
begin
x = x + 3;
end
x = 20;
begin
integer x;
x = 10;
f;
write x;
end
f;
write x;
end

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
