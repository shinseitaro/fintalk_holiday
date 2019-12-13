# Fintalk Holiday Koan の始め方

## 始める前に

+ github account 作成
+ ローカルに git install 
    + windows
    + mac
    + linux
+ ローカルマシンのお好きなところに **fintalk** ホルダを作成。（任意ですが、推奨）

## 問題を解く人

### 最初にすること

> 以下はひよこさんという架空の人が問題を解く人として初参加するときの流れを説明しています． ひよこ（hiyoko）の部分は自分の名前に置き換えて，操作して下さい． 

#### 1. github で branch 作成
1. https://github.com/shinseitaro/fintalk_holiday

2. `master` にいることを確認

	![](https://i.imgur.com/q2DYIjP.jpg)

3. ①▼ボタンを押して `Switch branches/tag` のところに ②`hiyoko` と書く．すると **Crate branch: hiyoko** と出るので③押す

	![](https://i.imgur.com/RkuRSMe.jpg)

4. Branch: hiyoko にいるのを確認．▼を押すと他の人のブランチもあることが確認できる

	![](https://i.imgur.com/zic3bTh.jpg)
	
	![](https://i.imgur.com/hz9X7UC.jpg)


#### 2. git clone

1. **Clone or download** を押すと，**Clone with HTTPS** というのが出る．（もし，**Clone with SSH**が出たら，`User HTTPS` を押せば変わる）．:clipboard:マークを押すとリンクがコピーされる．

	![](https://i.imgur.com/HrD1tMJ.jpg)

1. 自分のローカルマシンで以下実行
	```
	$ cd fintalk 
	$ git clone https://github.com/shinseitaro/fintalk_holiday.git 
	$ cd fintalk_holiday
	```
#### 3. git checkout 

`git checkout` で， `hiyoko` ブランチに移動。

```bash
$ git checkout hiyoko
```

↑実行すると、このようなメッセージが出る。これでOK。
```
Branch hiyoko set up to track remote branch hiyoko from origin.
Switched to a new branch 'hiyoko'
```

#### 4. subscriber に移動して、自分の名前のディレクトリを作成
```
$ cd subscriber
$ mkdir hiyoko 
```

#### 5. 最初の問題に取り組む

練習として、ant の 問題0番を一緒にやってみましょう。

1. `hiyoko`の下に `ant` 作成
2. `ant`の下に `try_0.py` 作成
3. `git add subscriber/hiyoko/` して hiyoko ディレクトリを add する
4. コードを書く
	上記で作成した `try_0.py` に解答を書く． 
	```python
	# try_0.py （わざと間違ってみる）
	print("はろーーー")
	```
	`python try_0.py` で実行してみる．もしやってみたけど，エラーが出る，といった状態でも，悩んだ状態でいいから何か書いて先に進む（15分以上悩まない）

#### ファイルを add & commit 

まずは git status をして，try_0.py が modified になっている事を確認
```bash
$ git status

# いろいろメッセージがずらずら出たあと
	modified:   try_0.py
    
# というようなメッセージが出ればOK
```
add して commit する．-m 以降のメッセージは何でもOK．書きたい事を書いて下さい．
```bash
$ git add try_0.py 
$ git commit -m"try_0 解答しました．"
```

#### 8. git push

```bash
$ git push
# ~~~~ ながーいメッセージが出るが，とりあえず最後のここだけ確認できればOK
To git@github.com:shinseitaro/fintalk_holiday.git
   e2b7f4f..359a3e7  hiyoko -> hiyoko

```

#### 9. github 上で確認

1. https://github.com/shinseitaro/fintalk_holiday/tree/hiyoko (hiyokoは自分の名前に変えて)
2. `subscriber` > `hiyoko` > `ant` に行くと先程addしたファイルが追加されていることが確認できます

#### 10. 添削してもらう

1. https://github.com/shinseitaro/fintalk_holiday/tree/hiyoko に戻り

2. Branch が `hiyoko` であることを確認してから、`New pull request` を押す

	![](https://i.imgur.com/78Ypekz.jpg)

3. ここが一番大切！必ず **base: answer** と **compare: hiyoko** を選択、Reviewer を shinseitaro と かめちゃん選択する。コメント書くところに、悩んだところや、質問などなんでも書いてよいのでメッセージを残してください。最後に **Create pull request** を押してレビューを待ちます。 

	![](https://i.imgur.com/kMqN2yr.jpg)

これがよく言われる **【プルリクエスト】** です。

#### 11. プルリクエストがマージされる

回答がOKだった場合、プルリクエストが承認されます。
承認されると、 `answer` ブランチにマージされます。https://github.com/shinseitaro/fintalk_holiday/tree/answer で、自分の回答が取り込まれていることを確認してください。

#### 12. 次の問題を解く。

あとは5番からの手順を繰り返すだけです。クラスが上がったら（ant->birdなど）それ用のディレクトリを作って問題を解いてください。


## レビューする人

commit されたファイルで気になるところがある場合は、コードの気になるところに行くと:heavy_plus_sign:ボタンがでるのでそこでコメントしてください。

![](https://i.imgur.com/k9fDGtx.jpg)


## 問題を作る人

```bash
$ git checkout candidates
$ git pull
```
問題を作ってプッシュしたあと master に マージリクエストしてください。







