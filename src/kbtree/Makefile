CC=			gcc
CFLAGS=		-g -Wall -O2
OBJS=		../benchmark/benchmark.o ../runit/runlib.o test.o
DFLAGS=
INCLUDES=	-I../benchmark -I../runit
LIBS=		

.SUFFIXES:.c .o

.c.o:
		$(CC) -c $(INCLUDES) $(CFLAGS) $(DFLAGS) $< -o $@

all:test

test:$(OBJS)
		$(CC) $(CFLAGS) -o $@ $(OBJS) $(LIBS)

test.o:kbtree.h

cleanlocal:
		rm -f *.o a.out *~ test

clean:cleanlocal

