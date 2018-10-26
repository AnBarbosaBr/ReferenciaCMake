# Referencias CMake
Diretório criado para praticar e obter modelos para referencia futura sobre o uso de CMake e Make.

# Estrutura
O exemplo CMakeLists supõe uma estrutura que contém os arquivos de implementação(*.cpp) em *src*, os headers (*.h) em *include* e o executável será gerado em *build*

```cmake
cmake_minimum_required(VERSION 2.8.9)
project(directory_test)

#Bring the headers, such as Student.h into the project
include_directories(include)

#Can manually add the sources using the set command as follows:
#set(SOURCES src/mainapp.cpp src/Student.cpp)

#However, the file(GLOB...) allows for wildcard additions:
file(GLOB SOURCES "src/*.cpp")

add_executable(teste ${SOURCES})
```
## Tutoriais Úteis
[DerekMolloy - Introdução ao CMake](http://derekmolloy.ie/hello-world-introductions-to-cmake/)


