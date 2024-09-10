%{
%}

%%

[a-zA-Z_][a-zA-Z0-9_]* {printf("\nIdentifier: %s\n",yytext);}
.+ {printf("\nOther Character: %s\n",yytext);}

%%

int yywrap() 
{
return 1;
}

int main()
{
printf("Enter Input: ");
yylex();
return 0;
}
