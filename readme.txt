Git is a distributed version control system
Git is a free SoftWare distributed under the GPL
Git has a mutable index called stage.


我实在是看不下去了，一会儿暂存区一会儿版本库的，请先分清概念，经过我的实验，提交代码的更改一共分2个阶段。

1).从工作目录，提交到stage。
2).从stage提交到master。

从工作目录提交到stage，需要用add或者rm命令，只提交到stage，而没有提交到master，是不会自动同步到master的。

从stage提交到master用commit命令。

退回也是要分两步，一个是从master退回到stage，然后再从stage退回到工作目录。

对于还没有提交到stage的，可以从stage用checkout命令退回，这一步会取stage中的文件状态，覆盖掉工作目录中文件的状态，跟master完全没关系。

对于已经到达stage的，想把state中的文件状态用master中的覆盖掉，就用reset命令，这样就把stage中修改用master的状态覆盖掉了，完全跟工作目录没关系

rm file:删除工作区内容
git rm file:删除工作区与暂存区内容。
git rm file + git commit:删除版本库内容，必须使用git reset --hard ID返回。
git checkout -- file:用暂存区的内容覆盖工作区的内容，当两区内容一致或不存在暂存区内容时出错。
git reset HEAD --file:用版本库的内容覆盖暂存区内容，对工作区无影响。

ssh-key:so are you ok anny

SHA256:xubh+cRNrLoMwBgV4QwVUnC3m+sNtBu5qp3x9OIDejI Charlotte514@163.com
