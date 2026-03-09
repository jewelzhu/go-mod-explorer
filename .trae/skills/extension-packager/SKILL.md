---
name: "extension-packager"
description: "编译并打包 VS Code 插件为 .vsix 文件，并提供安装指南。当用户要求编译、打包插件或询问如何安装 .vsix 时调用此技能。"
---

# Extension Packager

此技能用于自动化 VS Code 插件的编译、打包流程，并提供安装指导。

## 编译与打包指令

1. **安装依赖** (如果尚未安装):
   ```bash
   npm install
   ```

2. **编译 TypeScript 源码**:
   ```bash
   npm run compile
   ```

3. **打包为 .vsix 文件**:
   ```bash
   npx @vscode/vsce package
   ```

## 如何安装 .vsix 文件

打包完成后，你可以通过以下几种方式安装生成的 `.vsix` 文件：

### 方式 1：通过 VS Code 界面安装
1. 打开 VS Code。
2. 进入 **Extensions** 视图 (快捷键 `Ctrl+Shift+X` 或 `Cmd+Shift+X`)。
3. 点击右上角的 `...` (More Actions) 按钮。
4. 选择 **Install from VSIX...**。
5. 在文件浏览器中选择生成的 `.vsix` 文件。

### 方式 2：通过命令行安装
在终端中运行以下命令：
```bash
trae --install-extension <path-to-your-vsix-file>
```

### 方式 3：拖拽安装
直接将 `.vsix` 文件从文件管理器拖入 VS Code 的扩展视图中即可触发安装。
