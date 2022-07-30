# rust-translator

一个用 rust 写的 PDF 论文简单实时翻译，翻译 API 为 Google 提供（主要支持 Linux 用户，Windows 用户也可以用但是貌似有比这还好的软件？）。

![example](./vids/example.gif)

# Linux 使用

## 使用之前请先安装 `xsel`

```bash
sudo apt install xsel
```

将 release 页面下的压缩包解压到本地，之后放到 `/usr/bin` 下或者直接执行即可。

## 如需要自己编译

编译之前请先安装依赖

```bash
sudo apt install xsel xcb libx11-xcb-dev libxcb-render-util0-dev libxcb-shape0-dev libxcb-xfixes0-dev
```


# Windows 使用

下载对应的 Windows 版本之后直接双击运行，和 Linux 版本不同的是，Windows 版本鼠标选出要翻译的文字之后，还要再按一个 `ctl-c`（复制）。

# 注

目前支持的翻译语种包含了
* english
* chinese
* japanese
* french
* german

如有需要，请使用如下命令来指定`源语言`和`目标语言`：

```bash
rust-translator -s enligh -t french
```

release 页面有多个版本下载：
* Linux 一个版本版本是使用 `x86_64-unknown-linux-gnu` 静态编译的
* Linux 另外个版本是使用 `x86_64-unknown-linux-musl` 静态编译的（占用空间小）
* Windows 一个版本版本是使用 `x86_64-pc-windows-gnu` 静态编译的
* Windows 还有一个版本版本是使用 `x86_64-pc-windows-msvc` 静态编译的
* ARM 唯一一个版本是使用 `aarch64-unknown-linux-gnu` 静态编译的

# 问题

还是无法找到一个可以获得单个单词详细翻译的 API...
