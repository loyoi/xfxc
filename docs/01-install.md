# 01 安装与更新

玄如意控制台是一个 **AE 插件（AEGP 类型）**，安装方式就是把插件文件放进 AE 的公共插件目录，
重启 AE 后生效。

---

## 系统要求

| 项目 | 要求 |
| ---- | ---- |
| 系统 | Windows 10 / 11（x64）；macOS（Intel / Apple Silicon 通用） |
| 宿主 | Adobe After Effects（支持 AEGP 的版本） |

---

## 下载

两种方式任选一种：

- ⚡ **一键安装（推荐，Windows）**：<https://my.feishu.cn/wiki/N7GEwUmAWinqtTkzqvkcbRyfnCg>
- 🐙 **手动下载（含 macOS）**：<https://github.com/loyoi/xfxc/releases/latest>

| 平台 | 文件 |
| ---- | ---- |
| Windows | `XFXConsole_<版本>.aex` |
| macOS | `XFXConsole_<版本>.zip`（解压后得到 `XFXConsole.plugin`） |

---

## Windows 安装

1. **关闭 After Effects**。
2. 下载 `.aex` 文件。
3. 把它复制到插件目录（`LoYoi` 文件夹不存在就自己新建）：

   ```
   C:\Program Files\Adobe\Common\Plug-ins\7.0\MediaCore\LoYoi\
   ```

   > 复制到 `Program Files` 需要管理员权限；文件管理器会弹出确认提示，点「继续」即可。
4. 启动 After Effects。

## macOS 安装

1. **关闭 After Effects**。
2. 解压 `.zip`，得到 `XFXConsole.plugin`。
3. 打开「访达 → 前往 → 前往文件夹」，输入：

   ```
   /Library/Application Support/Adobe/Common/Plug-ins/7.0/MediaCore
   ```

   若目录下没有 `LoYoi` 文件夹，先新建一个；把 `XFXConsole.plugin` 放进去。
4. 启动 After Effects。

> ⚠️ **Mac 用户务必先做这一步**：`Ctrl + 空格` 和 macOS 系统自带的「选择上一个输入源」快捷键冲突，
> 会导致快捷键按不出来，让人误以为插件没装上。请前往
> **系统设置 → 键盘 → 键盘快捷键 → 输入法**，取消勾选「选择上一个输入源」的 `Ctrl + 空格`。

---

## 验证是否安装成功

重启 AE 后，用以下任一方式呼出控制台：

- 按 `Ctrl + 空格`；
- 打开 AE 菜单 **窗口（Window）**，在最底部找到 **XFXConsole** 并点击。

能看到搜索框，就说明安装成功。

> 插件目录是 AE 所有版本的**公共目录**：装一次，本机安装的所有 AE 版本都能用。
> 如果某段时间升级了 AE 却没看到插件，先确认插件文件还在上述目录中。

---

## 更新

1. 关闭 AE。
2. 下载新版本，**覆盖**插件目录里的旧文件（Windows 覆盖 `.aex`，macOS 替换 `.plugin`）。
3. 启动 AE。

> 更新不会影响你的配置、按钮面板、收藏与云同步数据。

## 卸载

1. 关闭 AE。
2. 删除插件文件（Windows 的 `.aex` / macOS 的 `.plugin`）。
3. （可选）若想彻底清除数据，删除下面「数据与配置位置」中的目录与注册表项。

---

## 数据与配置位置

玄如意控制台的数据分成三类存放：

| 类型 | Windows | macOS | 内容 |
| ---- | ------- | ----- | ---- |
| 用户数据 | `文档\LoYoi\xfxconsole\` | `~/Documents/LoYoi/xfxconsole/` | `config.json`（收藏 / 面板 / 扫描设置）、拼音与效果名覆写文件 |
| 应用数据 | `%APPDATA%\LoYoi\xfxconsole\` | `~/Library/Application Support/LoYoi/xfxconsole/` | 字体扫描缓存、云同步状态与历史、回滚备份 |
| 本机设置 | 注册表 `HKEY_CURRENT_USER\Software\loyoi\XfxConsole` | `~/Library/Application Support/xfxc/config.json` | 界面语言、快捷键开关、附加扫描源等**本机**设置 |

> 「用户数据」目录就是 [07 云同步](07-webdav-sync.md) 的同步范围。
> 界面语言、快捷键开关、附加扫描源保存在「本机设置」里，**不参与云同步**，每台机器各自独立。

---

## 常见安装问题

**杀毒软件提示文件有风险？**
`.aex` 插件本质是 DLL，部分杀毒软件会对这类插件产生误报，这是常见现象。
若被拦截，把插件目录加入杀软白名单即可。

**复制文件时提示没有权限？**
Windows 需要管理员权限才能写入 `Program Files`。用管理员身份运行文件管理器，
或先把文件复制到别处再粘贴（系统会提示授权）。

**重启 AE 后没看到 XFXConsole？**
- 确认插件文件确实在插件目录中（`...\MediaCore\LoYoi\`）；
- Windows 注意文件后缀是否为 `.aex`（而不是 `.aex.zip` 之类的下载残留）；
- macOS 确认 `.plugin` 是一个整体（右键 → 显示包内容 可以查看）；
- 仍无法解决：带上 AE 版本与系统版本，到 QQ 群（552876393）或 QQ 客服（1019748371）反馈。