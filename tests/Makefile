CC = gcc
CFLAGS = -ansi -Wall -Wextra -pedantic -O3 -g -I ../src -L ../src
TESTS = http.test

all: ${TESTS}

%.test: %.c ../src/%.c
	$(CC) $(CFLAGS) -o $@ $^

%.o: %.c %.h
	$(CC) $(CFLAGS) -c $<

.PHONY: clean all

clean:
	rm -f *.o *.test