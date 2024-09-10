%{
#include<stdio.h>
%}
%%
"jayasankar" { printf("King "); }
. { printf("%c", yytext[0]); }
%%
int yywrap(){}
int main()
{
 yylex();
}
