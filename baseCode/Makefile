# This is a Makefile for compiling Fall 2010 CSE 167 projects.
# It includes all .cpp files in the current directory.
# To use on a different (non-lab) Linux setup, change the INCDIRS and LIBDIRS
#   directories to point to the locations of the header files on your machine.
NAME	= triangle
ECHO	= @echo
CC	= @g++
LIBS	= -lglut -lGLU -lGL -lXmu -lXi -o triangle
LDFLAGS	= $(LIBS)
CFLAGS	= 
SOURCES = $(wildcard *.cpp)
OBJS = $(patsubst %.cpp, %.o, $(SOURCES))

.SUFFIXES: .cpp .h .o

.cpp.o:
	$(ECHO) "Compiling $<"
	$(CC) $(CFLAGS) -c -o $@ $<

$(NAME): $(OBJS)
	$(ECHO) "Linking $@..."
	$(CC) -o $@ *.o $(LIBS)
	$(ECHO) "Built $@!"

clean:
	$(RM) core *.o $(NAME)
	$(ECHO) "All clean!"

new:
	make clean
	make 