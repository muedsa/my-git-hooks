# my-git-hooks
在某些情况下你可能需要的GIT HOOKS  
- pre-merge-commit  
防止把`develop`(请在脚本中自行修改名称)分支合并到其他分支  
**需要merge时禁用fast forward**，使用`--no-ff`命令或全局配置`git config --global merge.ff false`

- prepare-commit-msg  
防止直接向`develop`分支提交代码  

## 把hooks脚本分发到所有项目中
可以使用名称
```bash
for ghpath in ./*/*/.git/hooks; do cp ./githooks/* $ghpath; done
```
Windows可以使用Git Bash运行命令  
