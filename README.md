# jnz-sakura_word_ttl

## 概要
サクラエディタにおいて、TTL(TeraTermマクロ)の作成をサポートする為のキーワードファイルやキーワードヘルプファイル一式です。

## 対象バージョン
- サクラエディタ 2.2.0.1
    - ※他verでも恐らく問題無くインポート&使用ができると思われます。

## キーワード・キーワードヘルプの情報元
こちらの情報を基に作成致しました。(2019/08/18 時点の情報)  
[TTL コマンドリファレンス](https://ttssh2.osdn.jp/manual/ja/macro/command/index.html)

## ダウンロード
このページにある「Clone or Download」のボタンをクリックし、「Download ZIP」をクリックして任意の場所に保存してください。  
![DL1](https://user-images.githubusercontent.com/51849000/63220366-98072f00-c1c0-11e9-81a0-0604f15377d6.JPG)

## サクラエディタへのインポート手順
### 手順1
ダウンロードしたzipファイルを解凍し、中にある「ttl」ディレクトリを、サクラエディタがインストールされているフォルダへコピーします。  
![Import1](https://user-images.githubusercontent.com/51849000/63220345-1b745080-c1c0-11e9-8640-86a02d3de77c.JPG)

### 手順2
サクラエディタを起動し、「設定」＞「タイプ別設定一覧」をクリックし、タイプ別設定画面を開きます。  
![Import2](https://user-images.githubusercontent.com/51849000/63220424-20d29a80-c1c2-11e9-8434-b790db68b100.JPG)

### 手順3
タイプ別設定画面にて「追加」をクリックします。  
すると「設定◎◎」(◎◎は数字)が追加されます。  
![Import3](https://user-images.githubusercontent.com/51849000/63220449-c84fcd00-c1c2-11e9-9752-b920042f7b39.JPG)

### 手順4
新たに追加したタイプ(先ほどの『設定◎◎』)を選択した状態で「インポート」をクリックします。
ダイアログが開いたら、サクラエディタの実行ファイル(sakura.exe)と同じ場所に置いたttlディレクトリの中にある
「TTL.ini」を選択し、インポートしてください。  
![Import4](https://user-images.githubusercontent.com/51849000/63220459-1238b300-c1c3-11e9-954a-4d3271cc1580.JPG)
![Import5](https://user-images.githubusercontent.com/51849000/63220476-66439780-c1c3-11e9-9ec6-54a712de200c.JPG)

### 手順5
インポート確認画面が表示されます。  
「読込先」は「新規追加」ではなく、選択しているタイプ名の方にチェックを入れます。  
色選択は「--そのままインポート--」にします。  
OKをクリックするとインポートが実行されます。  
※ご使用のサクラエディタのバージョンによっては、ここで「サクラエディタのバージョンが違う」と警告が出る場合があります。  
![Import6](https://user-images.githubusercontent.com/51849000/63220491-b9b5e580-c1c3-11e9-9b31-c38e74232c0f.JPG)  
これで、  

- 強調キーワードの設定(キーワード,色)
- 入力補完の設定
- キーワードヘルプの設定

が完了しました。

__なおこれらの設定は、サクラエディタにて拡張子が「.ttl」のファイルを開いた場合のみ適用されます。__  

試しに適当に「test.ttl」とかファイルを作ってサクラエディタで読み込ませてみてください。  
適当に「e」などと入力し、Ctrl+スペースを押した時に入力補完候補が表示され、コマンドの説明文(キーワードヘルプ)が表示されればOKです。  
![Import7](https://user-images.githubusercontent.com/51849000/63220581-dce19480-c1c5-11e9-8706-45e9d0402f6c.JPG)

## 既知のバグ的なもの
一部のキーワードヘルプにて、説明文の中に「\n」が含まれるものがあります。
「\n」をそのままキーワードヘルプファイルに記述してみたんですが改行されてしまいました。
調べたんですがエスケープの仕方がわからなかったので、とりあえず
```
「\ n」(半角スペースを間に入れている)
```
で対処しています。  
![Import8](https://user-images.githubusercontent.com/51849000/63220618-98a2c400-c1c6-11e9-9cbf-6013920c6699.JPG)
