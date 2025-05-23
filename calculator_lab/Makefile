CXX = g++
CXXFLAGS = -Wall -std=c++11
AR = ar
ARFLAGS = rcs

all: calculator_app

calculator.o: calculator.cpp calculator.h
	$(CXX) $(CXXFLAGS) -c calculator.cpp

main.o: main.cpp calculator.h
	$(CXX) $(CXXFLAGS) -c main.cpp

libcalculator.a: calculator.o
	$(AR) $(ARFLAGS) libcalculator.a calculator.o

calculator_app: main.o libcalculator.a
	$(CXX) $(CXXFLAGS) -o calculator_app main.o libcalculator.a

clean:
	rm -f *.o *.a calculator_app

.PHONY: all clean
