
OBJ=hello.o
EXE=hello
CFLAGS=-g -Wall
LDFLAGS=-lm

all: $(EXE)
	
$(EXE): $(OBJ)
	$(CC) $(LDFLAGS) -o $@ $^

clean: 
	@rm -fv $(EXE) $(OBJ)
