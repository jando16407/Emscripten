# Emscripten
 
Emscripten can convert C/C++ code to JavaScript.

## How to activate it on Max OS X terminal (After installation)

#### Activate/Verify Emscripten

* Go to Emscripten folder (/Github/Emscripten/emsdk/)
* Update

		# Fetch the latest registry of available tools/
		git pull
        or
        ./emsdk update

		# Download and install the latest SDK tools.
		./emsdk install latest
        
        # Set up the compilar configuration to point to the "latest" SDK.
        
        # Activatr PATH and other environment variables in the current terminal
        source ./emsdk_env.sh

* Verify

		emcc -v


## How to compile C/C++ to JavaScript

#### Simple js convertion

Simply type emcc and name of file to compile.

	emcc hello_world.c

Use em++ to force compilation as C++

	em++ hello_world.c

This will generate two files. **a.out.js** and **a.out.wasm**.

You can run them using node.js

	node a.out.js

#### Generating HTML

You can also generate HTML file.
Just use **-o** command and specify an html file name.

	emcc hello_world.c -o hello.html

When open the html, use **localhost** to make sure it runs as it runs on a server.



For more information, check out the Emscripten website.

**https://emscripten.org/docs/getting_started/Tutorial.html#tutorial**