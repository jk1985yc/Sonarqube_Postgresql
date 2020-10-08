### Default Admin Credentials
When installing SonarQube, a default user with Administer System permission is created automatically:

Login: admin
Password: admin

#### Error Solution
```
ERROR: 
[1] bootstrap checks failed
[1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]
```
#### For Temp,Restart Failure
```
sysctl -w vm.max_map_count=262144
```
#### For Permanent

修改/etc/sysctl.conf 添加
```
vm.max_map_count=2621441
```
```
sysctl -p /etc/sysctl.conf
```
