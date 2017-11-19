INCDIR := -I/usr/arm-linux-gnu/include
LIBDIR := -L/usr/arm-linux-gnu/lib

CC := $(CROSS_COMPILE)gcc

.PHONY: all clean

all:
	$(CC) -print-search-dirs
	$(CC) -Wall  $(INCDIR) $(LIBDIR) -lm analog_clock.c -o analog_clock
	


clean:
	rm -f *.o analog_clock

