.PHONY: all
all:
	# $(CXX) -O0 -std=c++11 src/memory.cc -o O0.out
	$(CXX) -O0 -std=c++11 src/cpu.cc src/libs/md5.cpp -Isrc -o O0.out
	@# lscpu

.PHONY: test
test: 
	time ./O0.out ${ARGS}

.PHONY: valg
valg:
	valgrind --tool=cachegrind ./O0.out ${ARGS}

.PHONY: install
install:
	sudo apt-get install -qq g++-4.8
	export CXX="g++-4.8"

.PHONY: clear
clear:
	rm -f *.out 
	rm -f *.tmp