# 为UBML做出贡献

首先，热烈欢迎对UBML感兴趣的你。我们非常鼓励这种意愿。这里有一份对你有帮助的指南。

## 主题

* [报告安全性问题](#reporting-security-issues)
* [报告一般性问题](#reporting-general-issues)
* [贡献文档和代码](#code-and-doc-contribution)
* [贡献测试用例](#test-case-contribution)
* [参与任何有帮助的事请](#engage-to-help-anything)
* [的艾玛书写风格](#code-style)

## 报告安全性问题

安全问题永远会被认真对待。按照我们一贯的原则，我们不鼓励任何人传播安全问题。如果你发现了一个UBML的安全问题，请不要公开讨论它，并且不要放到公共问题中。我们鼓励您向[ubml_user@groups.163.com](mailto:ubml_user@groups.163.com)或[ubml_dev@groups.163.com](mailto:ubml_dev@groups.163.com)发送私人电子邮件报告此事。

## 报告一般性问题

平心而论，我们认为UBML的每一个用户都是非常友善的贡献者。在体验过UBML之后，您可能会对项目有一些反馈。然后通过[新建问题](http://open.inspur.com/open-igix/ubml/issues/new)自由地创建一个问题。

因为我们是以分布式的方式协作项目UBML，所以我们青睐**写得很好的**，**详细的**，**明确的**问题报告。为了使交流更有效率，我们希望每个人都可以提问前先搜索你的问题是否存在于列表中。如果您发现它存在，请在现有问题下的评论中添加您的详细信息，而不是开一个全新的问题。

为了使问题细节尽可能标准化，我们为问题设置了一个[问题模板](./.gitee/ISSUE_TEMPLATE)
记者。请**确保**按照说明填写模板中的字段。

很多情况下，你可以开启一个提问:

*错误报告
*功能要求
*性能问题
*功能建议
*功能设计
*寻求帮助
*文档缺失
*测试改进
*任何项目中的问题
*等等

我们也必须提醒您，当填写一个新的问题时，请记得从您的帖子中删除敏感数据。敏感数据包含密码、密钥、网络位置、私有业务数据等等。

## 贡献文档和代码

我们鼓励每一个使UBML项目更好的行为。在GitHub上，UBML的每一个改进都可以通过一个PR (pull request的缩写)实现。

*如果你发现一个拼写错误，试着修复它!
*如果你发现一个bug，试着修复它!
*如果你发现一些多余的代码，试着删除它们!
*如果你发现一些测试用例缺失，尝试添加它们!
*如果您可以增强一个功能，请**不要**犹豫!
*如果你发现代码是不易理解的，试着添加注释使它更明确!
*如果你发现代码很丑，试着重构它!
*如果你能帮助改进文档，那就再好不过了!
*如果你发现文档不正确，请立刻修复它!
*……

实际上，我们不可能把它们全部列出来。只要记住一个原则:

> 我们期待着你的任何PR。

既然您已经准备好用PR来改进UBML，我们建议您可以在这里查看一下PR规则。

*(准备工作区)(# workspace-preparation)
*(定义分支)(# branch-definition)
*(提交规则) (# commit-rules)
*(PR说明)(# pr-description)

### 工作区准备

为了提一个PR，如果您已经注册了GitHub ID，那么您可以按照以下步骤进行准备:

1. **FORK** UBML到你的本地代码库。要做到这一点，您只需要单击[ubml
/ubml-standard](https://gitee.com/ubml/ubml-standard)主页右侧的Fork按钮。然后您将在 `https://gitee.com/<your-username>/ubml-standard`获取到，其中`your-username`是你的Gitee用户名。

1. **克隆**到本地自己的开发仓库。使用`git clone git@gitee.com:<your-username>/ubml-impl.git`将代码库克隆到本地。然后，您可以创建新的分支来完成您希望进行的更改。

1. **设置远程仓库地址** 使用如下两条命令更新远程链接为`git@gitee.com:ubml/ubml-impl.git`:

```
git remote add upstream git@giteee.com:ubml/ubml-impl.git
git remote set-url --push upstream no-pushing
```

完成这个远程设置，你可以像这样检查你的git远程配置:

```
$ git remote -v
origin     git@gitee.com:<your-username>/ubml-impl.git (fetch)
origin     git@gitee.com:<your-username>/ubml-impl.git (push)
upstream   git@gitee.com:ubml/ubml-impl.git (fetch)
upstream   no-pushing (push)
```

通过添加这个功能，我们可以很容易地同步本地分支和远程分支。

### 分支合并

现在，我们假设每个通过pull请求的贡献都是为了UBML[分支发展](https://gitee.com/ubml/ubml-standard/tree/develop)。在做出贡献之前，了解分支定义将会有很大帮助。

作为贡献者，再次记住，通过pull请求的每个提交都是为了分支开发。而在UBML项目
，还有其他几个分支，我们通常称之为发布分支(比如0.9.0,0.9.1)，特性分支，热修复分支和主分支。

当正式发布一个版本时，会有一个发布分支并以版本号命名。

在发布之后，我们将把发布分支的提交合并到主分支中。

当我们发现某个版本有bug时，我们会决定在以后的版本中修复它，或者在特定的热修复版本中修复它。当我们决定修复热修复版本时，我们将基于相应的发布分支检出热修复分支，执行代码修复和验证，并将其合并到开发分支和主分支中。

对于更大的特性，我们将抽出特性分支进行开发和验证。


### 提交规则

实际上，在UBML中，我们在提交时会参考两个原则:

* [提交消息](#commit-message)
* [提交内容](#commit-content)

#### 提交消息

提交消息可以帮助审稿人更好地理解提交的PR的目的。 它还可以帮助加快代码审查过程。 我们鼓励贡献者使用** EXPLICIT **提交消息而不是模棱两可的消息。 一方面，我们通常提倡以下提交消息类型：

* docs: xxxx. 例如, "docs: add docs about ubml-models introduction".
* feature: xxxx.例如, "feature: support VO customization".
* bugfix: xxxx. 例如, "bugfix: fix panic when input nil parameter".
* refactor: xxxx. 例如, "refactor: simplify to make codes more readable".
* test: xxx. 例如, "test: add unit test case for func InsertIntoArray".
* 其他可读和显式的表达方式.

另一方面，我们不鼓励贡献者像以下方式提交消息：

* ~~fix bug~~
* ~~update~~
* ~~add doc~~

如果你现在有点懵, 请参考 [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/) 从头开始学习^^.

#### 提交内容

提交内容表示一次提交中包含的所有内容更改。 我们最好将所有内容包含在一个提交中，这样可以在没有任何其他提交帮助的情况下支持审阅者的完整审阅。 换句话说，一次提交中的内容（应当）是可以通过CI的，以避免代码混乱。 简而言之，我们要记住三个小规则：

* 一次提交避免特别大的修改;
* 每次提交均应当完整且可审查.
* 提交时，检查git配置项(`user.name`, `user.email`) ，确保它与您的github ID相匹配.


另外，在代码更改部分，我们建议所有贡献者都应阅读UBML的 [代码样式](#代码样式).

无论提交消息还是提交内容，我们都更加注重代码审查.


### PR 说明

PR是更改UBML项目文件的唯一方法。 为了帮助审稿人更好地达到目标，PR说明不能太详细. 我们鼓励贡献者遵循 [PR 模板](./.gitee/PULL_REQUEST_TEMPLATE.md) 完成拉取请求.

## 测试用例贡献

欢迎任何测试用例. 当前, UBML 功能性测试的优先级是最高的.

* 对于单元测试，您需要在同一模块的测试目录中创建一个名为`xxxTest.java` . 推荐您使用 junit5 UT 框架
* 对于集成测试，可以将集成测试放在测试目录或UBML-test模块中。 建议使用模仿测试框架.

## 致力于帮助任何事情

我们选择Gitee作为UBML合作的主要场所。 所以这里是UBML最新更新的.虽然通过PR贡献是一种明确的帮助方式，我们仍然鼓励其他方式.

* 如果可以的话，回复他人的问题;
* 帮助解决其他用户的问题;
* 帮助审查他人的PR设计;
* 帮助查看PR中其他人的代码;
* 讨论有关UBML的问题，以使事情更加明确;
* 在GitHub之外倡导UBML技术;
* 在UBML上撰写博客，等等.


## 代码样式

UBML代码样式符合阿里巴巴Java编码准则.


### 指导方针
[Alibaba-Java-Coding-Guidelines](https://alibaba.github.io/Alibaba-Java-Coding-Guidelines/) 


### IDE插件安装（非必须）

*如果要在编码时发现问题，则无需安装.*


#### idea IDE
[p3c-idea-plugin-install](https://github.com/alibaba/p3c/blob/master/idea-plugin/README.md) 

#### eclipse IDE
[p3c-eclipse-plugin-install](https://github.com/alibaba/p3c/blob/master/eclipse-plugin/README.md)


总之几句话, **任何帮助都是贡献.**