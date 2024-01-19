# sun-panel-ssh 一键部署sun-panel

## 介绍
sun-panel-ssh.sh 是一个用于一键部署 sun-panel 的 Docker 容器的 Bash 脚本。该脚本可用于快速设置 Docker 容器并启动 sun-panel 服务。

## 使用方法
### SSH 使用
```bash
bash -c "$(curl -fsSL https://github.com/kokojacket/sun-panel-ssh/blob/main/sun-panel-ssh.sh)" -- --file_location="/目录位置" --container_name="容器名称" --port_number="端口号"
```
#### 参数说明：
- `--file_location="/目录位置"`: 指定要挂载到容器内的目录位置。
- `--container_name="容器名称"`: 指定要创建的 Docker 容器的名称。
- `--port_number="端口号"`: 指定要映射的端口号。

也可以不附加参数:
```bash
bash -c "$(curl -fsSL https://github.com/kokojacket/sun-panel-ssh/blob/main/sun-panel-ssh.sh)"
```

### 示例
```bash
bash -c "$(curl -fsSL https://github.com/kokojacket/sun-panel-ssh/blob/main/sunpanel.sh)" -- --file_location="/home/user/data" --container_name="my_container" --port_number="8080"
```
上述示例将会创建一个名为 my_container 的 Docker 容器，并将本地 /home/user/data 目录挂载到容器内，并映射端口 8080。

## 注意事项
1. 请确保已经安装 Docker 并且具有足够的权限来执行 Docker 相关操作。
2. 在执行命令时，请确保网络连接正常，以便能够通过 curl 下载必要的脚本文件。

[脚本链接](https://github.com/kokojacket/sun-panel-ssh/blob/main/sunpanel.sh)

希望这样能够帮助到你！
