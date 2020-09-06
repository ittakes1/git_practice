## git_practice

# 初始設定
安裝以後，設定使用者名稱和email
```bash
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

# 追蹤新的檔案
要開始追蹤一個新的檔案,可以使用 git add 命令; 要開始追蹤 README 檔案,你可以執行:
```bash
$ git add README.md
```
如果再次執行檢查狀態命令,可以看到 README.md 檔案現在是準備好被提交的「已追蹤」和「已預存」狀態:
```bash
$ git status
```
On branch master
Your branch is up-to-date with 'origin/master'.

# 預存修改過的檔案 git add

# 提交你的修改
現在你的預存區已被建構成你想要的，你可以開始提交你的變更； 記住：任何未預暫存的檔案——新增的、已修改的，自從你編輯它們卻尚未用 git add 預存的——將不會納入本次的提交中； 它們仍以「已修改」的身份存在磁碟中。 在目前情況下，假設你上次執行 git status 時，你看到所有檔案都已經被預存，因此你準備提交你的變更。 最簡單的提交方式是輸入 git commit：
```bash
$ git commit  # 這麼做會啟動你選定的編輯器
```
或者
```bash
$ git commit -m "Story 182: Fix benchmarks for speed" # -m 選項後方直接輸入提交訊息
[master 463dc4f] Story 182: Fix benchmarks for speed  ← 提交到哪個分支（master）、提交的 SHA-1 校驗碼（463dc4f）
2 files changed, 2 insertions(+) ←有多少檔案被更動，以及統計此提交有多少列被新增和被移除
create mode 100644 README
```

# 將變更發送到遠端repo (例如github.com)
```bash
$git push origin master
```

# git clone 
使用https
```
$ git clone https://github.com/ittakes1/git_practice.git
'''
使用ssh
```
$ git clone git@github.com:ittakes1/git_practice.git
```
