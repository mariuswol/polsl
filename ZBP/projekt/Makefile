CC=g++
CFLAGS=-std=c++11 -Wall -W -O3
LIBS_M=MatrixGenerators.cpp Graph.cpp BoostGraphWrapper.cpp main.cpp
LIBS_T=MatrixGenerators.cpp Graph.cpp BoostGraphWrapper.cpp test.cpp
OBJECTS_M=$(LIBS_M:.cpp=.o)
OBJECTS_T=$(LIBS_T:.cpp=.o)

all: main.out test.out

main.out: $(OBJECTS_M) 
	$(CC) $(CFLAGS) $(OBJECTS_M) -o $@

test.out: $(OBJECTS_T) 
	$(CC) $(CFLAGS) $(OBJECTS_T) -o $@

.cpp.o:
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -rf *.o *.out
