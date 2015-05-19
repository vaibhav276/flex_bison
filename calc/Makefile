ROOT_DIR:=$(shell dirname $(realpath $(lastword $(MAKEFILE_LIST))))

all: scanner.l grammar.y
	bison -d grammar.y
	flex scanner.l
	cc -o calc grammar.tab.c lex.yy.c -lfl
	
install:
	rm /usr/bin/calc
	ln -s ${ROOT_DIR}/calc /usr/bin/calc