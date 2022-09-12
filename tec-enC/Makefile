LIB=tec

CC=gcc
CPPFLAGS=-I ${LIB}
CFLAGS=-std=c99 -W -Wall 
LDFLAGS=-L ${LIB}

all: simple

clean:
	rm -rf simple tec/*.o tec/*.c~ tec/*.h~

cleanall: clean
	cd ${LIB}; make cleanall

simple: simple.c ${LIB}/libtec.a
	$(CC) ${CPPFLAGS} ${CFLAGS} $(LDFLAGS) simple.c -ltec -o $@ 

${LIB}/libtec.a: ${LIB}/*.c
	cd ${LIB}; make

