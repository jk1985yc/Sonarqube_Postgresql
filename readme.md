```
ERROR: 
[1] bootstrap checks failed
[1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]
```
```
sysctl -w vm.max_map_count=262144
```
