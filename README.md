# fintalk_holiday

## Pythonドリル

+ 組わけは難易度。英語のアルファベット順に組分けしました。


### :ant: ありさん(ant)組

はじめてのPythonレベル

### :bird: とりさん(bird)組

### :cat:ねこさん(cat)組

### :dog:いぬさん(dog)組

### :elephant: ぞうさん(elephant)組

### :frog: かえるさん(frog)組


## 最初にすること

1. ローカルマシンにgit のインストールと初期設定
1. github にアカウント作成 https://github.com/
1. https://github.com/shinseitaro/fintalk_holiday で自分のブランチを作る
1. ローカルマシンのお好きなところに `fintalk` ディレクトリを作成（任意）
1. `fintalk` ディレクトリ に git clone する
	```bash=
	$ cd fintalk
	$ git clone https://github.com/shinseitaro/fintalk_holiday.git
	$ cd fintalk_holiday
	``` 
1. remote から fetch する
	```bash=
	$ git status
	ブランチ master
	Your branch is up-to-date with 'origin/master'.
	nothing to commit, working directory clean

	$ git fetch
	From github.com:shinseitaro/fintalk_holiday
	* [new branch]      test       -> origin/test
	```
1. ブランチの確認
	```bash=
	$ git branch -a 
	* master
	remotes/origin/HEAD -> origin/master
	remotes/origin/master
	remotes/origin/test
	```
1. 自分のブランチに移動. `test` のところは自分のブランチ名を入れる．
	```bash=
	$ git checkout test
	Branch test set up to track remote branch test from origin.
	Switched to a new branch 'test'

	$ git branch -a 
	master
	* test
	remotes/origin/HEAD -> origin/master
	remotes/origin/master
	remotes/origin/test

	```





## 問題の参考集

+ [Python入門](https://www.javadrive.jp/python/)
+ [Python-izm ](https://www.python-izm.com/)
+ [Practice Python](http://www.practicepython.org/)
+ [Python Exercises, Practice, Solution - w3resource](https://www.w3resource.com/python-exercises/)
+ [応用プログラミング演習問題集](http://www.logopt.com/mikiokubo/Programming/pythonprob.txt)




