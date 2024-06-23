
program        → declaration* EOF ;

#### Declarations

<pre>
declaration    → classDecl   
		| funDecl   
  		| varDecl   
		| statement ;

classDecl      → "class" IDENTIFIER ( "<" IDENTIFIER )?   
                 "{" function* "}" ;   
funDecl        → "fun" function ;   
varDecl        → "var" IDENTIFIER ( "=" expression )? ";" ;   
</pre>

#### Statements

<pre>
statement      → exprStmt
               | forStmt
               | ifStmt
               | printStmt
               | returnStmt
               | whileStmt
               | block ;

exprStmt       → expression ";" ;
forStmt        → "for" "(" ( varDecl | exprStmt | ";" )
                           expression? ";"
                           expression? ")" statement ;
	
ifStmt         → "if" "(" expression ")" statement
                 ( "else" statement )? ;
	
printStmt      → "print" expression ";" ;
returnStmt     → "return" expression? ";" ;
whileStmt      → "while" "(" expression ")" statement ;
block          → "{" declaration* "}" ;
</pre>
