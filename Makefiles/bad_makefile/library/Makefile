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
	install -m 644 math_functions.h $(DESTDIR)/$(PREFIX)/include
	install -m 644 libcalculator.so $(DESTDIR)/$(PREFIX)/include
uninstall:

clean:
	rm -f $(LIB) math_functions.o
	
#gcc -L/usr/include -Wall -o test main.c -lcalculator
