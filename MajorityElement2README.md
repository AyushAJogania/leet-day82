# leet-day82

# MyHashMap Implementation

## Introduction

The `MyHashMap` class is a basic implementation of a HashMap with three core operations:

1. `put(key, value)`: Inserts a (key, value) pair into the HashMap. If the key already exists in the map, it updates the corresponding value.
2. `get(key)`: Returns the value to which the specified key is mapped or -1 if this map contains no mapping for the key.
3. `remove(key)`: Removes the key and its corresponding value if the map contains the mapping for the key.

## How to Use

1. Include the `MyHashMap` class in your C++ project.
2. Create an instance of `MyHashMap`:

    ```cpp
    MyHashMap myHashMap;
    ```

3. Use the methods `put`, `get`, and `remove` to interact with the HashMap:

    ```cpp
    myHashMap.put(1, 1);
    myHashMap.put(2, 2);
    int value1 = myHashMap.get(1); // returns 1
    int value2 = myHashMap.get(3); // returns -1
    myHashMap.put(2, 1);
    int value3 = myHashMap.get(2); // returns 1
    myHashMap.remove(2);
    int value4 = myHashMap.get(2); // returns -1
    ```

## Example

```cpp
#include "MyHashMap.h"

int main() {
    MyHashMap myHashMap;
    myHashMap.put(1, 1);
    myHashMap.put(2, 2);
    int value1 = myHashMap.get(1); // returns 1
    int value2 = myHashMap.get(3); // returns -1
    myHashMap.put(2, 1);
    int value3 = myHashMap.get(2); // returns 1
    myHashMap.remove(2);
    int value4 = myHashMap.get(2); // returns -1

    return 0;
}
```

## Constraints

- 0 <= key, value <= 10^6
- At most 10^4 calls will be made to put, get, and remove.
