%{
%}

%%

[A-Z] {printf("\nCapital Letter: %s\n",yytext);}
. {printf("\nNot Caps: %s\n",yytext);}

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
