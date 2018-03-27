# Github Flow 实战

假设各位是负责给某软件开发功能的开发者，并且所在团队已经开发了一款叫做 Fizzbuzz 的软件。

我们现在需要为该软件添加一个新的功能。

## 准备工作

*   如果尚未 clone 仓库……

	那么需要 Fork https://github.com/ituring/fizzbuzz 仓库，然后将该仓库 clone 到本地环境。
	
	```
	$ git clone git@github.com:tequlia2pop/fizzbuzz.git
	```
	
*   如果之前 clone 过仓库……

	那么应该将 master 分支更新成远程仓库最新 master 分支的状态。

	```
	$ git checkout master
	$ git pull
	```
	
## 创建新的分支

创建并切换到新的分支，同时在 Github 端的远程仓库上也创建一个同名的分支。

```
$ git checkout -b 7-case-output-github
$ git push -u origin 7-case-output-github
```

## 实现新功能

在 lib/fizzbuzz.rb 中增加代码后提交，然后将其 push 到远程仓库。

```
$ git commit -am "Add output Github"
$ git push
```
 
## 创建 Pull Request

从 7-case-output-github 分支创建一个 Pull Request 发送给 master 分支，请求与 master 分支合并。

## 培育 Pull Request

我们在接收到其他开发者的反馈后，可能需要对代码进行修正。完成后，还需要将编写的新功能合并到 master 分支。

```
$ git commit -am "Fix ..."
$ git push
```

确认 Pull Request 没有问题后，便可以通过评论请求与 master 合并了。这一系列的接受反馈与代码更新的过程，称作培育 Pull Request。

## 合并 Pull Request

最终，代码通过了其他开发者的审查，并顺利合并至 master 分支。

合并完成后，这个 master 分支将被立刻部署至正式环境。 