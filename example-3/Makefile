.PHONY: all debug release clean


CXX = g++


RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall -Wextra


RELEASE_EXEC  = casino-royale
DEBUG_EXEC    = casino-royale-dbg

SOURCES       = $(wildcard *.cpp)
OBJECTS       = $(SOURCES:.cpp=.o)

all: debug release

debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): $(SOURCES)
	$(CXX) $(DEBUG_FLAGS) $(SOURCES) -o $(DEBUG_EXEC)

release: $(RELEASE_EXEC)

$(RELEASE_EXEC): $(SOURCES)
	$(CXX) $(RELEASE_FLAGS) $(SOURCES) -o $(RELEASE_EXEC)

clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC) $(OBJECTS)
