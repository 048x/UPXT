# Ventoy 多系统启动盘指南

> 一个 U 盘装下所有系统镜像，开机菜单直接选，不用反复制作启动盘。

## 一、关于 Ventoy

传统启动盘「一个盘一个系统」，换系统就要重新格式化重做。Ventoy 则把 U 盘做成一块「镜像容器」：把 ISO 文件拖进去，开机时从菜单选择启动任意一个镜像即可。

- 不用反复格式化，加/删镜像像管理普通文件一样简单
- 支持 Windows、Linux 等各类 ISO，以及 PE 维护盘
- 镜像放在 U 盘里，随时离线携带

## 二、制作步骤

1. 去官网 [ventoy.net](https://www.ventoy.net) 下载 Windows 版压缩包
2. 插上 U 盘（会被格式化，先备份数据），运行 `Ventoy2Disk.exe`
3. 选对 U 盘盘符 → 点击「安装」（首次安装和后续升级都是同一个按钮）
4. 安装完成后，把下载好的 ISO 文件**直接拷贝进 U 盘**即可，无需解压、无需关心格式

以后要换系统或加镜像，直接往 U 盘里拖 ISO / 删 ISO 就行，不用重新制作。

## 三、Ventoy 里放哪些系统（3~5 个够用）

| 类型 | 推荐系统 | 用途 | 官方下载 |
|------|---------|------|---------|
| 主力系统 | Windows 11 ISO | 日常装新机、重装 | https://www.microsoft.com/zh-cn/software-download/windows11 |
| 备用系统 | Windows 10 ISO | 老机器或兼容模式 | https://www.microsoft.com/zh-cn/software-download/windows10 |
| PE 维护 | 微PE 工具箱 | 救数据、重置密码、分区 | https://www.wepe.com.cn/download.html |
| Linux | Ubuntu LTS | 体验、救援、杀毒 | https://ubuntu.com/download/desktop |
| Linux | Deepin | 中文体验好 | https://www.deepin.org/zh/download/ |
| 工具盘 | DiskGenius | 硬盘分区、坏道检测 | https://www.diskgenius.cn/download.php |

> ⚠️ 镜像本体（每个 4~7GB）无法存进 GitHub 仓库，请从上方官方地址下载后自行拷贝到 U 盘。

建议：**1 个主力 + 1 个备用 + 若干工具**，不要贪多。3~5 个最顺手，多了菜单翻着累。

## 四、注意事项

- **U 盘格式**：默认 exFAT，兼容性最好；老主板不支持时可选 NTFS
- **安全启动（Secure Boot）**：部分机型需在 BIOS 中关闭，或导入 Ventoy 的 MOK 密钥
- **镜像位置**：放根目录或新建文件夹都行，Ventoy 会自动扫描并在菜单中按文件名显示
- **升级 Ventoy**：出新版后直接运行 `Ventoy2Disk.exe` 点升级，U 盘里的 ISO 不会丢
- **文件过大提示（>4GB）**：说明 U 盘是 FAT32 格式，重新格式化为 exFAT 或 NTFS 即可

## 五、小技巧

- 安装 **Ventoy 主题插件**（官网有），开机界面更清爽
- Linux 发行版支持 **持久化存储**，可保存改动，折腾 Linux 时很实用
