# 大文件上传到github教程
根据你提供的文件路径 `"D:\Desktop\高数\神资料.pdf"`，以下是详细的步骤来帮助你将此文件上传到GitHub仓库，使用Git LFS处理该PDF文件。

### 1. 创建GitHub仓库
- 在GitHub上创建一个新仓库，假设你命名为 **GaoShu-Resources**。
- 创建好后记下仓库的URL，例如：`https://github.com/yourusername/GaoShu-Resources.git`。

### 2. 下载并安装Git LFS
- 访问[Git LFS官网](https://git-lfs.github.com/)下载并安装适用于你的操作系统的Git LFS工具。

### 3. 初始化本地仓库和Git LFS
- 打开Git Bash并导航到你想要初始化Git仓库的位置。例如，如果你想在`D:\Desktop\高数`目录下创建本地Git仓库：
  
  ```bash
  cd /d/Desktop/高数
  ```

- 初始化Git仓库：

  ```bash
  git init
  ```

- 安装并初始化Git LFS：

  ```bash
  git lfs install
  ```

### 4. 配置Git LFS追踪大文件
- 由于你要上传的是一个PDF文件，可以将该类型文件加入到Git LFS的追踪列表中：

  ```bash
  git lfs track "*.pdf"
  ```

- 这会创建一个`.gitattributes`文件，它用于告知Git LFS哪些文件类型需要被追踪（此处为`.pdf`）。

### 5. 添加和提交文件
- 将你想要上传的文件添加到Git仓库中。具体到你提到的文件：

  ```bash
  git add "神资料.pdf"
  ```

- 确保`.gitattributes`文件也被添加，因为它是LFS追踪文件的配置：

  ```bash
  git add .gitattributes
  ```

- 提交更改：

  ```bash
  git commit -m "Add 高数 神资料.pdf with LFS"
  ```

### 6. 推送到GitHub仓库
- 将本地仓库与远程GitHub仓库关联：(这个是github仓库的http链接)

  ```bash
  git remote add origin https://github.com/yourusername/GaoShu-Resources.git
  ```

- 推送代码和大文件到GitHub：

  ```bash
  git push origin master
  ```

### 7. 验证上传结果
- 上传完成后，访问你的GitHub仓库页面，确保文件已上传成功。GitHub不会直接存储大文件，而是通过Git LFS存储和管理这些文件。
  
这样，你就成功将超过25MB的文件上传到了GitHub。
