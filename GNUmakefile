CC = g++
FLAGS = -std=c++17 -Wall -Werror -Wextra -Wpedantic
VPATH = src:lib
OBJECTS = PPlot.o SVGPainter.o util.o test.o main.o 

assignment1: $(OBJECTS)
	$(CC) $(OBJECTS) -o assignment2

PPlot.o: PPlot.cpp PPlot.h
	$(CC) $(FLAGS) -c lib/PPlot.cpp

SVGPainter.o: SVGPainter.cpp SVGPainter.h
	$(CC) $(FLAGS) -c lib/SVGPainter.cpp

util.o: util.cpp util.h search.h
	$(CC) $(FLAGS) -c src/util.cpp

test.o: test.cpp search.h util.h
	$(CC) $(FLAGS) -Ilib -c src/test.cpp

main.o: main.cpp
	$(CC) $(FLAGS) -Ilib -c src/main.cpp

clean:
	rm assignment2 *.o *.svg
