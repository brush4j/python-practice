## 魔术方法

在 Python 中，以双下划线 __ 开头和结尾的方法被称为“魔术方法”或“特殊方法”。这些方法并不是每个类中都默认存在的，而是由开发者根据需要定义的。它们主要用于实现特定的行为，使得类可以与 Python 的内置语法和功能进行交互。常见的魔术方法包括：

- `__init__(self, ...)`: 初始化对象时调用，用于设置对象的初始状态。
- `__str__(self)`: 定义对象被转换为字符串时的输出格式，例如在 print() 函数中使用。
- `__repr__(self)`: 定义对象的“官方”字符串表示形式，通常用于调试。
- `__len__(self)`: 定义对象的长度，例如在 len() 函数中使用。
- `__getitem__(self, key)`: 允许对象像字典或列表一样通过索引访问元素。
- `__setitem__(self, key, value)`: 允许对象像字典或列表一样通过索引设置元素。
- `__call__(self, ...)`: 允许对象像函数一样被调用。
- `__eq__(self, other)`: 定义对象之间的相等比较操作。
- `__add__(self, other)`: 定义对象之间的加法操作。

## 生态库与依赖管理

仓库：https://pypi.org/

使用 pip install 命令可以安装指定的包。

```shell
pip install matplotlib
```

如果你需要安装指定版本的包，可以在包名后面加上版本号：

```shell
pip install matplotlib==3.7.1
```

你可以通过空格分隔，使用 pip 一次安装多个包：

```shell
pip install numpy pandas scipy
```

使用 pip list 可以列出当前环境中安装的所有包及其版本。

```shell
pip list
```

你可以使用 pip show 命令查看包的详细信息（包括安装路径、版本、依赖关系等）。

```shell
pip show matplotlib
```

要升级某个已安装的包，可以使用 pip install --upgrade 命令。这个命令会将包升级到最新版本。

```shell
pip install --upgrade matplotlib
```

如果你想卸载已安装的包，可以使用 pip uninstall 命令。

```shell
pip uninstall matplotlib
```

查看包的依赖关系
你可以使用 pip show 查看包的依赖项（如果有的话）。在输出的信息中，会看到 Requires 字段，列出了该包的所有依赖项。

```shell
pip show matplotlib
```

从 requirements.txt 安装包
如果你有一个包含所有依赖包和版本号的 requirements.txt 文件，可以使用以下命令安装所有列出的包：

```shell
pip install -r requirements.txt
```

requirements.txt 文件通常包含像下面这样的内容：

```shell
matplotlib==3.7.1
numpy==1.24.2
pandas==1.5.3
```

导出已安装的包列表 ,你可以使用 pip freeze 命令将当前环境中的所有包及其版本导出到 requirements.txt 文件中，方便别人重现你的环境。

```shell
pip freeze > requirements.txt
```

安装本地包 ,如果你有一个本地包（例如 .tar.gz 文件或 .whl 文件），你可以通过以下命令安装：

```shell
pip install /path/to/package.tar.gz
```

查看 pip 的版本
你可以使用以下命令查看 pip 的版本：

```shell
pip --version
```

---

推荐阅读 docs\创建虚拟环境.md
