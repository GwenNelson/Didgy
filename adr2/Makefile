.DEFAULT_GOAL := all
.PHONY: all clean

CC	:= gcc
BIN     := ./bin
OBJ     := ./obj
SRC     := ./src
INCLUDE := ./include
SRCS    := $(wildcard $(SRC)/*.c)
OBJS    := $(patsubst $(SRC)/%.c,$(OBJ)/%.o,$(SRCS))
CFLAGS  := -I$(INCLUDE) 
LDFLAGS :=
LDLIBS  :=
EXE     := $(BIN)/adr2

all: $(EXE)

$(EXE): $(OBJS)
	$(CC) $(LDFLAGS) $^ -o $@ $(LDLIBS)

$(OBJ)/%.o: $(SRC)/%.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(EXE)
	rm -f $(OBJS)

