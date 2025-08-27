          
# Docker 环境安装脚本 (Rocky Linux 9 专用) 🐳🪨

## 核心功能 🔧

本脚本专为 **Rocky Linux 9** 系统设计，主要功能包括：

1. **Docker 引擎安装**
   - 自动配置官方 Docker CE 仓库
   - 安装最新稳定版 Docker 引擎
   - 设置开机自启服务

2. **Docker Compose 部署**
   - 下载指定版本 Docker Compose
   - 配置可执行权限
   - 验证安装完整性

3. **权限管理**
   - 创建 docker 用户组
   - 将当前用户加入 docker 组
   - 避免频繁使用 sudo

4. **系统适配**
   - 针对 Rocky Linux 9 的 SELinux 配置优化
   - 防火墙规则自动调整
   - 系统依赖包自动安装

## 典型使用场景 🖥️

1. **全新系统初始化**
   - 在刚安装的 Rocky Linux 9 上快速搭建容器环境

2. **CI/CD 环境准备**
   - 为自动化构建系统配置 Docker 运行时

3. **教学演示环境**
   - 快速创建一致的容器教学平台

4. **开发测试环境**
   - 为开发团队统一容器运行时版本

## Rocky Linux 9 特别说明 🪨

- 完美适配 Rocky Linux 9 的 dnf 包管理器
- 正确处理 Rocky Linux 9 的 SELinux 策略
- 优化了防火墙 (firewalld) 的容器网络规则
- 解决了 Rocky Linux 9 特有的依赖包冲突问题

## 使用限制 ⚠️

- **仅支持 Rocky Linux 9** (不保证在其他版本正常工作)
- 需要 root 权限执行
- 会修改系统关键配置

## 技术亮点 ✨

- 自动检测 Rocky Linux 9 系统版本
- 详细的错误日志记录
- 关键操作前的系统状态检查
- 完善的回滚机制
        
