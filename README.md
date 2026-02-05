# Plex Media Server for fnOS

Auto-build Plex Media Server packages for fnOS - Daily updates from official releases

## Download

从 [Releases](https://github.com/conversun/plex-fnos/releases) 下载最新的 `.fpk` 文件。

| 架构 | 文件名 | 适用设备 |
|------|--------|----------|
| x86_64 (amd64) | `plexmediaserver_x.x.x_amd64.fpk` | Intel/AMD 处理器 |
| aarch64 (arm64) | `plexmediaserver_x.x.x_arm64.fpk` | ARM64 处理器 |

## Install

1. 根据你的设备架构下载对应的 `.fpk` 文件
2. 在 fnOS 应用管理中选择「手动安装」
3. 上传 fpk 文件完成安装

## Web UI

安装后访问 `http://<your-nas-ip>:32400/web`

## Auto Update

GitHub Actions 每天自动检查 [Plex 官方下载](https://www.plex.tv/media-server-downloads/)，有新版本时自动构建并发布。

## Architecture

- **Platform**: fnOS (飞牛私有云)
- **Supported Architectures**: 
  - x86_64 (amd64) - Intel/AMD 64-bit
  - aarch64 (arm64) - ARM 64-bit

## Local Build

```bash
# 自动检测架构，构建最新版本
./update_plex.sh

# 指定架构
./update_plex.sh --arch arm64
./update_plex.sh --arch amd64

# 指定版本
./update_plex.sh --arch arm64 1.42.2.10156

# 查看帮助
./update_plex.sh --help
```

## Version Tags

Release 版本号规则：
- `v1.42.2.10156` - 首次发布
- `v1.42.2.10156-r2` - 同版本的打包修订（上游未更新时重新发布）

## Credits

- [Plex](https://www.plex.tv/) - Media Server
