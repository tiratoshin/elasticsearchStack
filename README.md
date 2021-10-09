# elasticsearchStack
elasticsearch, kibana, apm docker-compose file

If elasticsearch wont start and you get an error talking about vm max mem is too low, something like 

'max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]' 

then you need to set that in your wsl settings. The location of the file depends on the distro.

For one off setting you can run this in powershell, but after reboot it will revert. 

```
wsl -d docker-desktop
sysctl -w vm.max_map_count=262144
```
