%{
int vow=0;
int cons=0;
%}

%%

[aeiouAEIOU] {vow++;}
[a-zA-Z] {cons++;}

%%

int yywrap() {}

int main()
{
	printf("Enter String: ");
	yylex();
	printf("\nVowel count: %d",vow);
	printf("\nConsonants count: %d",cons);
	return 0;
}
