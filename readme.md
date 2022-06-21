## 注意事项

- 出现  Native controller process has stopped - no new native processes can be started 错误，es容器无法启动，docker虚拟内存大小限制原因

  windows wsl2 引擎docker可执行下边命令
```
wsl -d docker-desktop
sysctl -w vm.max_map_count=262144
```

- 具体其他环境解决方案 https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html#_set_vm_max_map_count_to_at_least_262144