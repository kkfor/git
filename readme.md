## 一. 配置全局
### 1. 设置用户名/邮箱
* git config --global user.name "zhangsan"
* git config --global user.email "zhansan@163.com"
### 2. 修改用户名/邮箱
* git config --global --replace-all user.name "lisi"
* git config --global --replace-all user.email "lisi@162.com"
### 3. 查看全局设置
* git config --global -l/(list)
## 二. 提交
### 1. 分开提交
* git add \<filename> // 添加到暂存区
* git commit \<filename> // 添加到本地库
* git push // 推送到服务器
### 2. 合并提交
* git add -am "注释" // tracked文件的修改快速提交到本地库
## 三. 查看
### 1. 查看文件状态
* git status \<filename>
### 2. 查看提交记录
* git log \<filename>
* git log --pretty=oneline \<filename> // 单行查看
## 三. 撤销
### 1. 撤销工作区修改内容
* git checkout -- \<filename>  [HEAD~aabbcc]// 用版本库中的版本替换工作区的版本
### 2. 撤销暂存区修改内容
* git rm --cached \<filename>
* git reset HEAD \<filename>
## 四. 回退版本
### 1. git reset --hard HEAD^ 
回退到上一个版本，--hard表示工作区同时恢复, --soft表示版本库回退，但是工作区不回退
### 2. git reset --hard commit-id
回退到某个commit-id
