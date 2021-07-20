CC:=gcc
CFLAGS:=-Wall -fpic
LDFLAGS= -shared
LIB:=libcalculator.so

SRCS = math_functions.c
OBJS =$(SRCS:.c=.o)

PREFIX =/usr
all: $(LIB)

$(LIB):$(OBJS)
	$(CC) $(CFLAGS) $(LDFLAGS) -o $(LIB) $^

install: $(LIB)
	install -m 644 math_functions.h $(DESTDIR)/$(PREFIX)/lib
	install -m 644 libcalculator.so $(DESTDIR)/$(PREFIX)/lib
uninstall:

clean:
	rm -f $(LIB) math_functions.o
	
#gcc -L/usr/lib -Wall -o test main.c -lcalculator
