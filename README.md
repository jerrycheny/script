          
# Proxmox VE 虚拟机备份脚本 📂⚡

## 功能简介 🛠️

本脚本用于自动化备份 Proxmox VE 上的虚拟机，主要功能包括：
- 批量备份多个虚拟机 🖥️🖥️
- 支持并行备份任务 ⚡
- 自动清理过期备份 🗑️
- 详细的日志记录 📝
- 邮件通知功能 📧

## 快速开始 🚀

1. **修改配置参数**：
   ```bash
   VMIDS=(100 101 102 103)      # 需要备份的虚拟机ID
   BACKUP_STORAGE="local-hdd"   # Proxmox存储名称
   TARGET_DIR="/mnt/vm_backup"  # 备份目标路径
   RETENTION_DAYS=3             # 备份保留天数
   ```

2. **运行脚本**：
   ```bash
   chmod +x pve_vm_backup.sh
   ./pve_vm_backup.sh
   ```

## 主要特点 ✨

- **智能备份**：自动检测并备份指定虚拟机
- **三重验证**：确保备份文件正确生成和复制
- **并行处理**：支持同时备份多个虚拟机（可配置）
- **过期清理**：自动删除旧备份，节省存储空间
- **详细日志**：记录每个步骤和操作结果

## 通知设置 🔔

如需邮件通知，请设置：
```bash
NOTIFY_EMAIL="your_email@example.com"
```

## 日志查看 📜

日志默认保存在：
```
/var/log/pve_backups/pve_backups_YYYYMMDD.log
```

## 注意事项 ⚠️

1. 确保目标目录有足够空间
2. 需要root权限执行
3. 备份期间虚拟机会短暂停机

## 版本信息 ℹ️

当前版本：3.1
最后更新：2024-06-15

Happy Backing Up! 🎉
        
