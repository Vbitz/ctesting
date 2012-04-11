all: build

build:
	g++ -o ctesting main.cpp

cibuild: build winbuild
	
winbuild:
	i586-mingw32msvc-cc -o ctesting.exe main.cpp