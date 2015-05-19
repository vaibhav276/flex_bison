all: scanner.l grammar.y
	bison -d grammar.y
	flex scanner.l
	cc -o calc grammar.tab.c lex.yy.c -lfl