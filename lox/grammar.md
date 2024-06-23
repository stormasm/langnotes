
program        → declaration* EOF ;

#### Declarations

declaration    → classDecl   
               | funDecl   
               | varDecl   
               | statement ;

classDecl      → "class" IDENTIFIER ( "<" IDENTIFIER )?   
                 "{" function* "}" ;   
funDecl        → "fun" function ;   
varDecl        → "var" IDENTIFIER ( "=" expression )? ";" ;   
