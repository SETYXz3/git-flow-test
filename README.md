## 参考
### ローカルJenkins起動方法(MacOS)

```bash
# 起動
$ brew services start jenkins-lts

# 再起動
$ brew services restart jenkins-lts

# 停止
$ brew services stop jenkins-lts

# 画面から停止や再起動もできる
http://localhost:8080/exit

http://localhost:8080/restart

```

# git-flow-test

### git flowの初期化

```bash
$ git flow init
$ git branch

# developブランチ作成
$ git push origin develop
```

### featureブランチの作成
**この時はまだファイルの修正はしていない、ただブランチを作成するだけ。**
作成
cicdという名前の場合

```bash
$ git flow feature start cicd
```

確認
```bash
$ git branch
```

リモートに新規ブランチの反映
```bash
$ git flow feature publish cicd
```

### 開発作業開始
```bash
$ git flow feature pull origin cicd
```

### 開発作業完了
ここからファイルの修正が入りまして、リモートへ反映する

```bash
$ git add .
$ git commit -m "first commit."

# または以下でも一行でできます
$ git commit -am "first commit."

# 全てローカルの修正が完了後、リモートへ反映
$ git push origin feature/cicd
```

--- end ---
