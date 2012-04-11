all: build

build:
	g++ -o ctesting main.cpp

cibuild: build winbuild-ci
	mkdir -p ../build
	cp ctesting ../build/ctesting-linux
	cp ctesting.exe ../build/ctesting-win.exe
	cd ..
	rm build-pkg.zip
	zip -r build-pkg.zip build/
	
winbuild-local:
	mingw32-c++ -o ctesting.exe main.cpp

winbuild-ci:
	i586-mingw32msvc-c++ -o ctesting.exe main.cpp