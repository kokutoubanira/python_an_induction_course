# induction_course

# Introduction
本研修ではgoogle Cokabratoryを使用します。初めにIntroduction.ipynbに記載されているチュートリアルを開始してください。

# なぜPythonを使うのか

## シンプルで分かりやすい文法

PythonはRubyのような柔軟性が高い言語に比べてルールが厳密なので、誰がコーディングしても同じようなコードになるのが特徴です。

なんでそれが良いの？という疑問が浮かぶと思いますが、それは開発はチームで行うことがほとんどなので、自分だけでプログラムを組むということはほとんどないわけです。

そのため、他人が書いたコードを理解して修正したり追加したりするわけなのですが、その時にコーディングのルールが厳密で分かりやすいものだと現状のコードを把握しやすいし、修正もしやすいわけなのです。

## コミュニティと民間企業のサポート
オープンソースプロジェクトは開発リソース(おもにマンパワー)が限られ、開発の中心メンバーが何らかの理由で参加しなくなった場合、一気にそのプロジェクトが衰退する場合がありますが、特に科学技術計算関係のパッケージについては民間企業が本格的にサポートとしており、オープンソースソフトウェアとして公開する体制が整っています。

民間企業の代表的なのが、Enthought社とContinuum Analytics社である。
Enthought社は科学技術計算用パッケージ群「Scipy Stack」を提供し、科学技術計算向けの「SciPy Conference」と呼ばれる会議の開催を支援している。Continuum Analytics社はPythonディストリビューション「Anaconda」を提供し、データ分析向けの「Py Data」と呼ばれる会議の開催を支援している。
また、GoogleもPython作者のGuido van Rossum氏を2005年に雇用したり、「Google Summer of Code」というオープンソースの開発に資金を提供するプロジェクトを2005年に作成し、機械学習ライブラリの「scikit-learn」や多変量回帰分析・時系列分析ライブラリ「statsmodels」がリリースされています。

## 汎用性が高い

AIや機械学習、データ分析などで注目を集めたPythonですが、Pythonはできることが非常に多い言語です。

AIを活用したIoTの開発やロボット制御といった研究分野での実績から、Webアプリケーションやデスクトップアプリケーション、ゲームなど身近なものの開発にも採用されています。

## 将来性が高い

Pythonは日本だけでなく世界的に見ても高い人気を誇るプログラミング言語です。その理由はさまざまで、AIや機械学習の開発ができることや、データサイエンスに強みを持っている点などが挙げられます。

- AI・機械学習の開発
- データサイエンスに優れている
- C言語系と連携しやすい
- Webサービス・Webアプリの開発

## google colab状でgithubからcloneする方法
### 手順
Driveマウント→clone<br>
マウントは最初の1回だけでOK。
### 1. Google Driveをマウントする
Google Driveをマウントする
ご存知の通りColabはインスタンスの12時間ルール＆90分ルールがあるので、作業ディレクトリの内容が一定時間で消えてしまいます。
当然.gitなども保存されず、これではコード管理もやりようがないので、まずはGoogle Driveをマウントします。
UI上で左側のファイルボタンを押し、「ドライブをマウント」でマウントできます。
![](./utils/mount.png)
<br>
これで自分のGoogleDrive上のファイルをノートブック上で扱えるようになり、保存もできるようになります。

## GitHubのリポジトリをGoogle Driveにclone

Google ColabのNotebook上でGoogle Driveをマウントする
なんでもいいのでGoogle Colabのノートブックを作成するか、既存のてきとうなノートブックを開きます。
マウントするためだけのノートブックなので、ほんとにてきとうで良いです。

作成したノートブック上で以下のようなコードをし実行ます。
```
from google.colab import drive
drive.mount('/content/gdrive')
```
Google ColabのNotebook上でGit Cloneする
基本的にはただGit Cloneするコマンドを実行するだけです。
が、微妙に書き換えないといけないところがあります。
私はこの「微妙に書き換えないといけないとこ」が良くわからずマジで時間を無駄にしました。しにたい。

ポイントとしては以下の通りです。

Git Cloneするリンクに、自分のGitアカウントをGitパスワードを含める
ローカルリポジトルを作るディレクトリはGoogle ColabにマウントしたGoogle Driveを指定
この二つを踏まえたGit Clone用コマンドは以下のような感じです。
```
!git clone  https://<自分のGitアカウント>:<Gitパスワード>@github.com/<Gitアカウント>/<リポジトリ>.git "gdrive/My Drive/<ローカルリポジトリを作るディレクトリ>"
```

以下clone下ディレクトリのノートブックを開いて実行

### 使用するノートブックをアップロードする
使用するノートブックをgithubからアップロードして実行できるようにします。

![](./utils/アップロード.PNG)

ノートブックをアップロードを選択します。
以下のような表示が出てくると思いますので、
`Github URLを入力するか、組織またはユーザーで検索します`にhttps://github.com/kokutoubanira/induction_course.git　
を入力しノートブックを選択すれば開始できます。


# 1章 pythonの使い方100本ノック
本章では、Pythonの基礎的な文法について学びます。次章以降に登場するコードを理解するにあたって必要となる最低限の知識について最短で習得するのが目標です。より正確かつ詳細な知識を確認したい場合には公式のチュートリアルなどを参照してください。

# 2章 Numpy 50本ノック
最初にPythonにおけるNumPyの役割やNumPyを使ってできることを解説します。
まずはNumPyで何ができるのかを理解しましょう。

# 3章　Pandas 100本ノック
データ処理の基本ツールとしてPandasの使い方を紹介します。Pandasには便利な機能がたくさんありますが、特に分析業務で頻出のPandas関数・メソッドを重点的に取り上げました。
Pandasに便利なメソッドがたくさんあることは知っている、でも知りたいのは分析に最低限必要なやつだけ！、という人のためのPandasマニュアルです。単に機能を説明するだけでは実際の処理動作がわかりにくいため、タイタニックのデータに対してpandasの処理を適応していくことで一連のpandasの操作を体験できる様にしています。

# 4章　自然言語処理 100本ノック
自然言語処理を理解するために必要な最低限の知識と実装の仕方を学びます。自然言語処理には様々なタスクにについても学びます。

# Create Chat bot
ここでは、1~4章で学んだ知識を活用して、チャットボットを作成してみます。4章で学んだ知識を応用すれば様々なものが作成することができます。

# additional edition１ 画像処理　

画像処理に欠かせない「[OpenCV](https://opencv.org/)」について、機能や基本的な使い方について 解説します。
OpenCVは、インテルのエンジニアが開発した、無料で配布されている画像処理・画像解析のためのライブラリです。
ライブラリは、プログラムに詳しい人が難しい機能のプログラムを作成してパッキングしたもので、プログラムに詳しくない人でも、そのライブラリを使用することによりすごいことが出来ます。
例えば、「顔検出」です。１からプログラムを作成して実現するのはかなり大変ですが、OpenCVのライブラリを使用すれば、初心者の方が十数行のプログラムを書くことで実現出来ます。

OpenCVを利用し、画像処理技術を学習してみましょう

# additional edition2 手書き文字認識

この章ではpytorchを使用した機械学習の一般的なタスクのAPIについて説明します。
- データの操作
- modelの作成
- modelの保存・読み込み
- テンソル

# additional edition3 顔認識

＊随時更新

# additional edition4 ニュースコーパスを使用した検索システムの作り方

＊随時更新



