# Kondo(今度) 🧹

清理项目中的 `node_modules`、`target`、`build` 等目录。

非常适合以下情况：

- 💾 你想备份代码，但不想包含数GB的依赖项
- 🧑‍🎨 你尝试了很多项目，但讨厌它们占用的空间
- ⚡️ 你喜欢保持你的磁盘精简且快速

<br />

<p align="center">
    <strong>支持20+种项目类型</strong>
</p>

<p align="center">
<a href="https://doc.rust-lang.org/cargo/">Cargo</a>  (Rust),
<a href="https://cmake.org">CMake</a>  (C, C++),
<a href="https://getcomposer.org/">Composer</a>  (PHP),
<a href="https://elixir-lang.org/">Elixir</a>, 
<a href="https://godotengine.org/">Godot 4.x</a> (C#, GDScript)
</p>
<p align="center">
<a href="https://gradle.com/">Gradle</a>  (Java)
<a href="https://jupyter.org/">Jupyter Notebook</a> (Python),
<a href="https://pixi.sh/">Pixi</a>  (Python),
<a href="https://maven.apache.org/">Maven</a>  (Java),
<a href="https://nodejs.org/">Node</a>  (JavaScript)
</p>
<p align="center">
<a href="https://dart.dev/">Pub</a>  (Dart),
<a href="https://www.python.org/">Python</a> 
<a href="https://www.scala-sbt.org/">SBT</a>  (Scala),
<a href="https://docs.haskellstack.org/">Stack</a>  (Haskell),
<a href="https://cabal.readthedocs.io/en/stable/">Cabal</a>  (Haskell),
<a href="https://swift.org/">Swift</a> 
</p>
<p align="center">
<a href="https://unity.com/">Unity</a>  (C#),
<a href="https://www.unrealengine.com/">Unreal Engine</a> (C++),
<a href="https://ziglang.org/">Zig</a>, 
<a href="https://dotnet.microsoft.com/">.NET</a>  (C#, F#)
<a href="https://turbo.build/repo">Turborepo</a>  (JavaScript)
</p>

<img width="972" alt="kondo cli cleaning projects" src="https://user-images.githubusercontent.com/2771466/222950622-475bc6cc-7b91-47c2-86b2-5948bee4fe8e.png">

<img width="1112" alt="kondo gui displaying projects" src="https://user-images.githubusercontent.com/2771466/222950846-964162a1-80c9-4cdf-a9a8-d818ba4cb34a.png">

<details>
<summary>CLI 视频</summary>

[kondo-cli.webm](https://user-images.githubusercontent.com/2771466/222949617-0ed621bc-ac4e-495a-9165-036a3a597d34.webm) 

</details>

<details>
<summary>GUI 视频</summary>

[kondo-ui.webm](https://user-images.githubusercontent.com/2771466/222951044-13484711-6107-45d4-aaa3-3140bbbba898.webm) 

</details>

## 安装

> **警告**
>
> Kondo 本质上是带有提示的 `rm -rf`。请自行斟酌使用。请始终备份你的项目。

### 命令行

**winget**

```powershell
winget install kondo
```

**Homebrew**

```sh
brew install kondo
```

**MacPorts**

```sh
sudo port install kondo
```

**Arch Linux**

```sh
pacman -S kondo
```

**源代码**

需要 [Rust](https://www.rust-lang.org/tools/install)。

```sh
git clone https://github.com/tbillington/kondo.git 
cargo install --path kondo/kondo
```

**其他**

二进制文件可在[发布页面](https://github.com/tbillington/kondo/releases)上找到。

<a href="https://repology.org/project/kondo/versions"> 
    <img src="https://repology.org/badge/vertical-allrepos/kondo.svg"  alt="打包状态">
</a>

### 图形用户界面

**Windows**

```powershell
winget install kondo-ui
```


**Arch Linux**

```sh
pacman -S kondo-ui
```

**源代码**

需要 [rust](https://www.rust-lang.org/tools/install)。 你可能需要[Linux平台上特定的依赖](https://github.com/xi-editor/druid#platform-notes)。

```sh
git clone https://github.com/tbillington/kondo.git 
cargo install --path kondo/kondo-ui
```

二进制文件可在[发布页面](https://github.com/tbillington/kondo/releases)上找到。

<a href="https://repology.org/project/rust:kondo-ui/versions"> 
    <img src="https://repology.org/badge/vertical-allrepos/rust:kondo-ui.svg"  alt="打包状态">
</a>

## 使用

> **警告**
>
> Kondo 本质上是带有提示的 `rm -rf`。请自行斟酌使用。请始终备份你的项目。

### 命令行界面

运行 `kondo` 而不指定目录将在当前目录运行。

```sh
kondo
```

提供路径将告诉 `kondo` 从哪里开始。支持多个路径。

```sh
kondo code/my_project code/my_project_2
```

传递一个时间将过滤出至少指定时间未被修改的项目。查看 `kondo --help` 获取完整选项列表。

```sh
kondo --older 3M # 仅选择最后修改时间超过3个月的项目
kondo -o3M # 简写形式
```

更多选项，如静默模式、跟随符号链接和文件系统限制，可通过 `kondo --help` 查看。

## 构建/开发

要构建 cli `kondo`，你可以在项目的根目录运行 `cargo build` 和 `cargo run`。

要构建 gui `kondo-ui`，你必须首先导航到 `kondo-ui` 目录，然后你可以运行 `cargo build` 和 `cargo run`。

输出的二进制文件将位于 `target/debug/` 或 `target/release/`，遵循 [Cargo](https://doc.rust-lang.org/cargo/index.html) 默认设置。

## 类似项目

- [The Tin Summer](https://github.com/vmchale/tin-summer) 
- [Detox](https://github.com/whitfin/detox) 
- [Sweep](https://github.com/woubuc/sweep) 
- [npkill](https://github.com/voidcosmos/npkill) 
- [Cargo Cleanall](https://github.com/LeSnake04/cargo-cleanall) 
- [Cargo Sweep](https://github.com/holmgr/cargo-sweep) 
- [Cargo Wipe](https://github.com/mihai-dinculescu/cargo-wipe) 
- [cargo-clean-recursive](https://github.com/IgaguriMK/cargo-clean-recursive)
