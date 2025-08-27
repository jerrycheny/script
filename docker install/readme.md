


          
# Rocky Linux 9 Docker 安装脚本 🐳🪨

## 功能概述 🛠️

本脚本专为 **Rocky Linux 9** 系统设计，用于自动化安装和配置 Docker 环境，主要功能包括：

- ✅ 配置阿里云 Rocky Linux 镜像源
- ✅ 系统更新和依赖包安装
- ✅ Docker CE 安装与配置
- ✅ Docker 镜像加速设置
- ✅ 防火墙和 SELinux 配置优化
- 📝 详细的日志记录功能

## 使用说明 📖

### 1. 下载脚本
```bash
wget https://example.com/setup_docker.sh
```

### 2. 赋予执行权限
```bash
chmod +x setup_docker.sh
```

### 3. 以 root 用户执行
```bash
sudo ./setup_docker.sh
```

## 代码功能详解 🔍

### 主要函数说明

1. **`configure_repos`** - 配置阿里云镜像源
   - 替换默认 mirrorlist
   - 备份原始 repo 文件

2. **`update_system`** - 系统更新
   - 清理 dnf 缓存
   - 更新所有系统包

3. **`install_docker`** - Docker 安装
   - 添加阿里云 Docker 源
   - 安装最新版 Docker CE

4. **`configure_docker`** - Docker 配置
   - 设置镜像加速器
   - 启用开机自启

5. **`disable_selinux`** - SELinux 配置
   - 临时设置为 Permissive 模式
   - 永久禁用（需重启生效）

## 重要配置项 ⚙️

```bash
# 日志文件路径
LOG_FILE="/var/log/setup_docker.log"

# Docker 镜像加速器
REGISTRY_MIRROR="https://dockerhub.icu"
```

## 注意事项 ⚠️

1. **必须使用 root 权限执行**
2. 脚本执行后会 **禁用 firewalld**
3. SELinux 配置 **需要重启系统** 才能完全生效
4. 完整日志保存在 `/var/log/setup_docker.log`

## 适用场景 🖥️

- 全新 Rocky Linux 9 系统初始化
- 批量部署 Docker 环境
- CI/CD 流水线环境准备

## 技术亮点 ✨

- 全自动化安装流程
- 完善的错误处理和日志记录
- 针对 Rocky Linux 9 特别优化
- 关键操作前的系统状态检查

Happy Dockerizing on Rocky Linux! 🎉
        
