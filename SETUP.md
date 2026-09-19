# 仓库使用说明

## 首次配置

GitHub 仓库名称应为 `grad-prep-hanlinjie`，可见性为 **Public**。

在需要下载仓库的电脑上运行（提交署名和邮箱替换为自己的实际值）：

```sh
git clone https://github.com/han-lingjie/grad-prep-hanlinjie.git
cd grad-prep-hanlinjie
git config user.name "你的提交署名"
git config user.email "你的 GitHub 已验证邮箱或隐私邮箱"
```

如果本地文件夹已经初始化并配置了远程地址，直接在该文件夹继续工作，无需重复 clone。

## 日常提交

```sh
git status
git diff
git add README.md research engineering
git diff --cached
git commit -m "docs: update research and engineering progress"
git push origin main
```

提交前检查暂存内容。若修改其他文件，按实际路径补充 `git add`。

## 开始科研任务

1. 在 `research/README.md` 填写论文的正式标题、年份、发表 venue、论文及代码来源。
2. 复制 `research/paper-notes/TEMPLATE.md`，命名为 `01-论文简称.md`，填写自己的理解。
3. 复制 `research/reproduction/00-template/`，命名为 `01-论文简称/`，放入实际复现代码。
4. 记录环境、数据、配置、随机种子和命令，把实际指标、曲线与分析放入该论文的 `results/`。
5. 模板目录可保留作参考，不计入已完成论文或实验数量。

## 开始工程任务

在 `engineering/README.md` 确定项目类型、功能和技术栈，将源代码放入 `engineering/src/`。实现后补充可执行的环境安装、启动命令及实际截图。

## 文件管理

- `.gitignore` 默认排除密钥文件、依赖目录、缓存、数据集及模型权重。
- 小型实验指标、曲线和运行截图可以提交；大型数据集及权重在文档中给出来源或下载方法。
- 论文优先保留合法来源链接；确认允许分发后再提交 PDF。
- 引入第三方代码时保留原有版权及许可证说明。
