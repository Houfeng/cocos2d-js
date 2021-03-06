<img src="http://www.cocos2d-x.org/attachments/801/cocos2dx_portrait.png" width=200>

cocos2d-js
===========

Cocos2d-JS is Cocos2d-x engine's javascript version. It support full Cocos2d-x features with a set of simplified javascript friendly APIs.

Cocos2d-JS provides a consistent development experience for whichever platform you want to distribute to, both web and native. "Code once, run everywhere" is incredibly easy and natural in Cocos2d-JS. With one single javascript code base, you can run your game on both web browsers and native platform including Mac OS, Windows, iOS, Android. This will bring your game great opportunities in almost all canals of distribution.

Furthermore, javascript friendly API makes your game development experience a breeze, easy to code, test and distribute. Cocos2d-JS also offers Cocos Console, a script tool, to simplify the creation of projects and let you start coding right away. You can use it to create a new project and publish it to android, iOS, Mac OS or web.

##Setup

First step, you need to setup before using this tool. Please clone Cocos2d-JS repository and update all submodule. Open console in Cocos2d-JS folder, then just run `./setup.py` on console. You may need to provide your NDK, Android SDK and ANT's path during the setup. Note that this tool is developed with python, so you will need python (32bit) 2.7.5 or later installed on your machine (but it doesn't support Python3).

Some useful links:

* [Android SDK](https://developer.android.com/sdk/index.html?hl=sk)
* [NDK](https://developer.android.com/tools/sdk/ndk/index.html)
* [Ant binary release](http://ant.apache.org/)
    - Download Ant.
    - Uncompress the downloaded file into a directory.
    - Set environmental variables JAVA_HOME to your Java environment, ANT_HOME to the directory you uncompressed Ant to, and add ${ANT_HOME}/bin (Unix) or %ANT_HOME%/bin (Windows) to your PATH.
    
    ```
    // Example: Execute in console or add into .bash_profile(Mac)
    export ANT_ROOT=/usr/local/ant/bin
    export JAVA_HOME=/usr/local/jdk1.7.0_51
    ```

##Usage

After setup correctly done, you can start to use `cocos` command in your console.

###Create a new project

* Create a project contains Cocos2d-x JSB and Cocos2d-html5:

	```
	cocos new projectName -l js
	```

* Create a project contains Cocos2d-html5 only:

	```
	cocos new projectName -l js --no-native
	```

* Create a project in a specified directory:

	```
	cocos new projectName -l js -d ./Projects
	```

###Run the project

* Run Cocos2d-html5 project with a Websever:

	```
	cd directory/to/project
	cocos run -p web
	```

* Compile and run project in Cocos2d-JSB :

	```
	cd directory/to/project
	cocos compile -p ios|mac|android|web
	cocos run -p ios|mac|android
	```

* Useful options

	```
	-p platform : The platform can be ios|mac|android|web.
	-s source   : Your project directory, if not specified the current directory will be used.
	-q          : Quiet mode, remove log messages.
	-m mode     : Mode debug or release, debug is default
	--source-map: General source-map file. (Web platform only)
	```

###Help

And if you have any doubt about the usage, please use `-h` with any command to have some help messages. Here are all three commands:

* `new` for create
* `compile` for compile
* `run` for run
