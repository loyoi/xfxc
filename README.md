# 玄如意控制台 (XFXConsole)

Adobe After Effects 原生插件（AEGP），提供快速搜索与命令面板，支持效果、预设、字体、脚本与表达式的高效调用，内置云同步与多语言界面。

## 下载

最新版本见 [Releases](https://github.com/loyoi/xfxc/releases/latest)：

- Windows：`XFXConsole_<版本>.aex`
- macOS：`XFXConsole_<版本>.zip`

## 手动安装

安装前请先完全退出 After Effects；若曾安装在其它路径，请先删除旧版以避免冲突。

### Windows

1. 关闭 After Effects。
2. 下载 `XFXConsole_<版本>.aex`。
3. 复制到：
   `C:\Program Files\Adobe\Common\Plug-ins\7.0\MediaCore\LoYoi\`
   若 `LoYoi` 文件夹不存在请手动新建（复制到 Program Files 需要管理员权限）。
4. 重启 After Effects。

### macOS

1. 关闭 After Effects。
2. 下载 `XFXConsole_<版本>.zip` 并解压，得到 `XFXConsole.plugin`。
3. 打开“访达 → 前往 → 前往文件夹”，输入：
   `/Library/Application Support/Adobe/Common/Plug-ins/7.0/MediaCore`
   在该目录下新建 `LoYoi` 文件夹（若不存在），并将 `XFXConsole.plugin` 复制进去。
4. 解除 macOS 安全隔离（否则可能提示“已损坏”或无法加载），在终端执行：

   ```
   sudo xattr -dr com.apple.quarantine "/Library/Application Support/Adobe/Common/Plug-ins/7.0/MediaCore/LoYoi/XFXConsole.plugin"
   ```

5. 重启 After Effects。

## 系统要求

- Windows 10 / 11（x64）
- macOS（Intel / Apple Silicon 通用二进制）
- Adobe After Effects（支持 AEGP 的版本）

## 授权

本插件为专有软件，采用专有许可协议，详见 [LICENSE](./LICENSE)。

## 关于本仓库

本仓库仅用于分发文档与构建产物，不包含源代码。源码由作者私有维护。
