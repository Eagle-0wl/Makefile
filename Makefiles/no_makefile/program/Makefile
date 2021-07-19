CC:=gcc
CFLAGS:=-Wall -I`pwd`
OBJS:=main.o maths.o usage.o
BIN:=calculator

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $(CFLAGS) -o $(BIN) $^

clean:
	rm -f $(BIN) $(OBJS)
