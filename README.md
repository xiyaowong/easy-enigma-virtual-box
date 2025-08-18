# EEVB - Easy Enigma VirtualBox 封装工具

**仅支持 Windows 系统**

EEVB 是一个简化 Enigma Virtual Box 命令行调用的封装工具，通过 JSON 配置文件快速构建虚拟化可执行文件。

## 安装

```bash
pip install eevb
```

## 使用方法

### 初始化配置文件

生成一个模板配置文件 `eevb.json`：

```bash
eevb init
```

自定义输出路径：

```bash
eevb init --output myconfig.json
```

### 构建虚拟化程序

使用配置文件构建输出：

```bash
eevb build
```

指定配置文件：

```bash
eevb build myconfig.json
```

或简写（直接传入 JSON 文件）：

```bash
eevb myconfig.json
```

### 查看帮助

```bash
eevb --help
eevb init --help
eevb build --help
```

### 配置说明

配置文件为 JSON 格式，主要字段：

- `input`: 原始可执行文件路径
- `output`: 输出虚拟化文件路径
- `files.delete_on_exit`: 是否运行后删除解压文件
- `files.compress`: 是否压缩嵌入文件
- `files.items`: 各虚拟目录下要包含的文件或文件夹路径列表

支持的虚拟目录包括：`DefaultFolder`, `SystemFolder`, `WindowsFolder`, `MyDocumentsFolder`, `ProgramFilesFolder` 等（见模板）。

---

# EEVB - Easy Enigma VirtualBox Wrapper

**Windows Only**

EEVB simplifies Enigma Virtual Box command-line usage by building virtualized executables via a JSON configuration file.

## Installation

```bash
pip install eevb
```

## Usage

### Initialize Configuration

Generate a template config file:

```bash
eevb init
```

With custom path:

```bash
eevb init --output myconfig.json
```

### Build Virtual Executable

Build using default config:

```bash
eevb build
```

Specify config file:

```bash
eevb build myconfig.json
```

Or shorthand (pass JSON directly):

```bash
eevb myconfig.json
```

### Show Help

```bash
eevb --help
eevb init --help
eevb build --help
```

### Configuration

The JSON config includes:
- `input`: input executable path
- `output`: output executable path
- `files.delete_on_exit`: delete files after exit
- `files.compress`: compress embedded files
- `files.items`: lists of files/folders for each virtual directory

Supported virtual folders: `DefaultFolder`, `SystemFolder`, `WindowsFolder`, `MyDocumentsFolder`, `ProgramFilesFolder`, etc. (see template).