# C++

## 1. Setting up cpp

### 1. Create CMakeLists.txt
```md
cmake_minimum_required(VERSION 3.20)

project(capture-first-productivity LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)  # compilier
set(CMAKE_CXX_STANDARD_REQUIRED ON) # Standard is required

add_executable(capture-first-productivity src/main.cpp) # create executable named 'capture-first-productivity' using src/main.cpp file
```

---

### 2, Builds the cmake files in the folder build (one timer)
```
mkdir build

cd build

cmake ..
```

---

### 3. compliling
```
cmake --build .
```

---

### 4. Running 
```
./cpf
```

---

### 5. Combined
```
cmake --build . && ./cpf
``` 
