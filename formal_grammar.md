# formal grammar
definition of the formal grammar of the lox programming language, updated as we go along

> program -> declaration* EOF ;
>
> declaration -> varDecl | statement ;
>
> statement -> exprStmt | printStmt | block ;
>
> block -> "{" declaration* "}" ;
> 
> varDecl -> "var" IDENTIFIER ( "=" expression )? ";";
>
> exprStmt -> expression ";" ;
> printStmt -> "print" expression ";" ;
>
> expression -> assignment ;
> assignment -> IDENTIFIER "=" assignment | equality ;
> equality -> comparison ( ( "!=" | "==" ) comparison )* ;
> comparison -> term ( ( ">" | ">=" | "<" | "<=" ) term )* ;
> term -> factor ( ( "-" | "+" ) factor )* ;
> factor -> unary ( ( "\" | "\*" ) unary )\* ; // (IGNORE \'s) ;
> unary -> ( "!" | "-" ) unary | primary ;
> primary -> NUMBER | STRING | "true" | "false" | "nil" | "(" expression ")" | IDENTIFIER ;

