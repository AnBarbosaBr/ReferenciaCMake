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

# Utilização
Após adicionar o CMakeLists.txt à raiz de seu código, e adaptá-lo a seu projeto, acesse o diretório *build*, e utilize o comando *cmake ..*
Em seguida, utilize o comando *make* para criar o arquivo.

```sh
$ cd ./build
$ cmake ..
-- The C compiler identification is GNU 6.4.0
-- The CXX compiler identification is GNU 6.4.0
-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++
-- Check for working CXX compiler: /usr/bin/c++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done
-- Generating done
-- Build files have been written to: .../build

$ make

```
	
## Tutoriais Úteis
[DerekMolloy - Introdução ao CMake](http://derekmolloy.ie/hello-world-introductions-to-cmake/)


