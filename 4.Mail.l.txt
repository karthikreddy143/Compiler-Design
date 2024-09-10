%{
%}

%%

[a-z.0-9_]+@[a-z]+".com"|".in" {printf("Valid Mail\n");}
.+ {printf("Invalid Mail\n");}

%%

int yywrap() {}

int main()
{
	printf("Enter Mail\n");
	yylex();
	return 0;
}
