#=====================================================================#
#                      HAPI PROGRAM MAKEFILE                          #
# This is the Makefile for a HAPI program.                            #
#                                                                     #
# "make autoclean" will remove temporary files (.pip and .cpp)        #
# "make clean" will remove the executable as well.                    #
# "make" or "make build" will build the application executable        #
#                                                                     #
# Enjoy!                                                              #
# - Lasse Nielsen.                                                    #
#=====================================================================#
name1 = sol1
name2 = sol2

CPP = cpp
HAPI = hapi
Copt = -O3
CC = g++ -std=c++11

default: build

all: build

phony: build clean

build: $(name1) $(name2)

$(name1): $(name1).cpp
	@echo "=== Building executable from C++ code in $(name1).cpp"
	$(CC) $(Copt) $(name1).cpp -o $(name1) -lpi -lpthread -lgmp

$(name1).cpp: $(name1).pip
	@echo "=== Compiling $(name1).pip to $(name1).cpp"
	$(HAPI) -compile -f $(name1).pip > $(name1).cpp

$(name1).pip: $(name1).pi
	@echo "=== Preprocessing $(name1).pi to $(name1).pip"
	$(CPP) $(name1).pi -I/opt/hapi/include | grep -v "^#" > $(name1).pip

$(name2): $(name2).cpp
	@echo "=== Building executable from C++ code in $(name2).cpp"
	$(CC) $(Copt) $(name2).cpp -o $(name2) -lpi -lpthread -lgmp

$(name2).cpp: $(name2).pip
	@echo "=== Compiling $(name2).pip to $(name2).cpp"
	$(HAPI) -compile -f $(name2).pip > $(name2).cpp

$(name2).pip: $(name2).pi
	@echo "=== Preprocessing $(name2).pi to $(name2).pip"
	$(CPP) $(name2).pi -I/opt/hapi/include | grep -v "^#" > $(name2).pip

clean:
	@rm -f $(name1) $(name2)
	@rm -f $(name1).pip
	@rm -f $(name1).cpp
	@rm -f $(name2).pip
	@rm -f $(name2).cpp
