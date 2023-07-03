# libFSBC-Android-Windows
This library allows you to convert ogg packets to FSB5.

## License
For simplicity purpose the license is the same as used for libogg and libvorbis.

## How to link (Windows-VisualStudio)
To compile for windows you will need visual studio.
You will have to do the linker stuff your own.
Tho just add the include file and start doing your work.

## How to link (Android-AndroidStudio)
I still havent figured this out so I will need some time over this.

## How to use
First of all include the header file in your source and then write the code.
THe first is the argc.
its the arguement count.
I will make it more simple in the next releases.
The next is the argv.
Its a char** or char[][] or string[] that holds the arguements.
The first string in the string[] or char** is the random string input, second is the input path, third is output path, fourth is loop start, fifth is loopEnd.

You can write the code as follows for a console application

```#include "FSBC.h"
#include <string>

int main()
{
	int argc = 4;
	char* random = "random";
	char* input = "Path to your ogg file";
	char* output = "Path to save your fsb";
	char* loopStart = "3333";
	char* loopEnd = "4444";

	char** argv = malloc(sizeof(char**) * 4);
	argv[0] = random;
	argv[1] = input;
	argv[2] = output;
	argv[3] = loopStart;
	argv[4] = loopEnd;

	ConvertToFSB(argc, argv);
}

If you dont want the Loop Points then simply remove them as follows

```#include "FSBC.h"
#include <string>

int main()
{
	int argc = 4;
	char* random = "random";
	char* input = "Path to your ogg file";
	char* output = "Path to save your fsb";

	char** argv = malloc(sizeof(char**) * 2);
	argv[0] = random;
	argv[1] = input;
	argv[2] = output;

	ConvertToFSB(argc, argv);
}```

You can only use C objective for now.
In the next releases I will improve it for sure.
