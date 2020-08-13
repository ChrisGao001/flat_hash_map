## How to Use
```code
#include "bytell_hash_map.hpp"
#include "unordered_map.hpp"
#include <iostream>
#include <memory>
#include <utility>

int main(int argc, char** argv) {
	ska::unordered_map<int, int> m;
	// ska::bytell_hash_map<int, int> m;

    for (int i=0; i<10; ++i) {
		m.emplace(i, 2*i);
	}
    for (const auto& iter : m) {
		std::cout << "key:" << iter.first << ",value:" << iter.second << std::endl;
	}

	return 0;
}
```
