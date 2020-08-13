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

## performance
```code
bytell_hash_map   insert:28959506,mem:273.066MB,find:16006
emilib6_hash_map  insert:28154966,mem:256.004MB,find:11617
dense_hash_map    insert:26935917,mem:256.012MB,find:24873
boost_hash_map    insert:35571720,mem:446.137MB,find:61376
std_hash_map      insert:32292225,mem:300.918MB,find:85920
sparse_hash_map   insert:42955370,mem:135.695MB,find:79769
```
