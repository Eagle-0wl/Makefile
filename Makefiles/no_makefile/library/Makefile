CC:=gcc
CFLAGS:=-Wall -fpic
LDFLAGS= -shared
LIB:=file_reader.so

SRCS = file_reader.c
OBJS =$(SRCS:.c=.o)

PREFIX =/usr
all: $(LIB) main

$(LIB):$(OBJS)
	$(CC) $(CFLAGS) $(LDFLAGS) -o $(LIB) $^

	
main: main.c 
	$(CC) -c main.c
	$(CC) -o main main.c file_reader.o

LIBRARY:$(OBJS)
	$(CC) $(CFLAGS) $(LDFLAGS) -o $(LIB) $^
clean:
	rm -f $(LIB) file_reader.o main.o main
