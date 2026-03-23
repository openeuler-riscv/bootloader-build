CC = gcc
CFLAGS = -Wall -Wextra -g -O2
LDLIBS =
TARGET = pack
SRCS = $(wildcard *.c)
OBJS = $(patsubst %.c,%.o,$(SRCS))

.PHONY: all clean

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) $(CFLAGS) $(OBJS) -o $@ $(LDLIBS)

%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

pack.o: pack.c pack.h

clean:
	$(RM) $(OBJS) $(TARGET)
