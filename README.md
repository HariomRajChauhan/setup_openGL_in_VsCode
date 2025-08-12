# Build the OPENGL projects in vsCode using c++ with the help of code runner

## This project demonstrates how to set up a basic OpenGL application using C++ with GLFW and GLEW libraries
## Prerequisites
- Install [Visual Studio Code](https://code.visualstudio.com/)
- Install [MinGW](https://www.mingw-w64.org/) or any C++ compiler
- Install [GLFW](https://www.glfw.org/download.html) and [GLEW](http://glew.sourceforge.net/) libraries
- Download the GLFW and GLEW libraries and extract them to a directory (e.g., `C:\glfw-3.4.bin.WIN64` and `C:\glew-2.2.0`)
- Install [Code Runner extension](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
- Install [C/C++ extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
- Install [C/C++ Theme](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-themes)

## to run the app just run the following command

```bash
ctrl + shift + b
```

### and then run the executable file

## Another way using code runner

### just click the shortcut key

```bash
ctrl + r
or just run the coderunner icon in the top right corner
```

### this is the previous command in the settings.json file

```json
{
    "code-runner.executorMap": {
        "cpp": "cd $dir && g++ $fileName -o $fileNameWithoutExt -I C:\\glfw-3.4.bin.WIN64\\include -I C:\\glew-2.2.0\\include -L C:\\glew-2.2.0\\lib\\Release\\x64 -L C:\\glfw-3.4.bin.WIN64\\lib-mingw-w64 -lglfw3dll -lglew32 -lopengl32 && ./$fileNameWithoutExt",
    }
}
```

### after this project complition please change the code-runner.executorMap to this:

```json
{
    "code-runner.executorMap": {
        "cpp": "cd $dir && g++ $fileName -o $fileNameWithoutExt && $dir$fileNameWithoutExt",
    }
}
```

### note: that please replace the dll files with the static files in the lib folder



git init
git add .
git commit -m "setup for openGL in vsCode using c++"
git branch -M main
git remote add origin https://github.com/HariomRajChauhan/setup_openGL_in_VsCode.git
git push -u origin main