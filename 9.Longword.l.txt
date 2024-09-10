%{
#include <stdio.h>
#include <string.h>
char longest_word[256];
int longest_length = 0;
%}
%%
[^\n\t ]+ {
    int length = strlen(yytext);
    if (length > longest_length) {
        longest_length = length;
        strcpy(longest_word, yytext);
    }
}
%%
int main(int argc, char *argv[]) {
    yylex();
    printf("The longest word is: %s\n", longest_word);
    return 0;
}
int yywrap() {
    return 1;
}
