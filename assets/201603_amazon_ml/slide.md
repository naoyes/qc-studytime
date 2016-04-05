name: top
class: center, middle, inverse

# Amazon Machine Learning
# で機械学習

---

# Contents

## 1. 機械学習について
## 2. Amazon Machine Learning について
## 3. Amazon Machine Learning のチュートリアルを試す

---
class: center, middle, inverse

# 1. 機械学習について

---

# 機械学習とは？

--

### 人工知能における研究課題の一つで、人間が自然に行っている学習能力と同様の機能をコンピュータで実現しようとする技術・手法のことである。
### 検索エンジン、医療診断、スパムメールの検出、金融市場の予測、DNA配列の分類、音声認識や文字認識などのパターン認識、ゲーム戦略、ロボット、など幅広い分野で用いられている。

.right[
  [機械学習 - Wikipedia](https://ja.wikipedia.org/wiki/%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92) より
]

???
---

# アルゴリズム

---

# アルゴリズム

.left-column[
## 教師あり学習
]
.right-column[
入力とそれに対応すべき出力（人間の専門家が訓練例にラベル付けすることで提供されることが多いのでラベルとも呼ばれる）を写像する関数を生成する。

例えば、分類問題では入力ベクトルと出力に対応する分類で示される例を与えられ、それらを写像する関数を近似的に求める。
]

---

# アルゴリズム

.left-column[
## 教師あり学習
## 教師なし学習
]
.right-column[
入力のみ（ラベルなしの例）からモデルを構築する。
]

???
ディープラーニングもこれの一種
---

# アルゴリズム

.left-column[
## 教師あり学習
## 教師なし学習
## 半教師あり学習
]
.right-column[
ラベルありの例とラベルなしの例をどちらも扱えるようにしたもので、それによって近似関数または分類器を生成する。
]

---

# アルゴリズム

.left-column[
## 教師あり学習
## 教師なし学習
## 半教師あり学習
## 強化学習
]
.right-column[
周囲の環境を観測することでどう行動すべきかを学習する。行動によって必ず環境に影響を及ぼし、環境から報酬という形でフィードバックを得ることで学習アルゴリズムのガイドとする。例えばQ学習がある。
]

---

# アルゴリズム

.left-column[
## 教師あり学習
## 教師なし学習
## 半教師あり学習
## 強化学習
## トランスダクション（トランスダクティブ推論）
]
.right-column[
観測された具体的な（訓練）例から具体的かつ固定の（テスト）例の新たな出力を予測しようとする。
]

---

# アルゴリズム

.left-column[
## 教師あり学習
## 教師なし学習
## 半教師あり学習
## 強化学習
## トランスダクション（トランスダクティブ推論）
## マルチタスク学習
]
.right-column[
関連する複数の問題について同時に学習させ、主要な問題の予測精度を向上させる。
]

---
class: center, middle, inverse

# 2. Amazon Machine Lerningについて

---

# Amazon Machine Lerningとは？

--

### 簡単に予測アプリケーションを構築できる機械サービスです。

.right[
[よくある質問 - Amazon Machine Learning | AWS](https://aws.amazon.com/jp/machine-learning/faqs/)
]

---

# 特長

* ### 機械学習モデルを容易に作成
* ### 数秒でモデルから予測を実行
* ### スケーラブルで高パフォーマンスな予測生成サービス
* ### 低コストで効率的
* ### 実証済みのテクノロジーを活用

---

# ユースケース

* ### 不正検出
* ### コンテンツのパーソナライズ
* ### マーケティングキャンペーン向けの傾向モデリング
* ### ドキュメントの分類
* ### カスタマーサポートのソリューション推奨の自動化

---

# 使用可能アルゴリズムは？

* ### 教師あり学習
* ### 教師なし学習
* ### 半教師あり学習
* ### 強化学習
* ### トランスダクション（トランスダクティブ推論）
* ### マルチタスク学習

---

# 使用可能アルゴリズムは？

* ### 教師あり学習

---
layout: false

# 教師あり学習

.left-column[
## 二項分類
]
.right-column[
あるデータを２つのグループのどちらかに分類
  - このメールはスパムメールか否か
  - この服は男性用か女性用か
  - この顧客はこの商品を買うか否か
]

---

# 教師あり学習

.left-column[
## 二項分類
## 多項分類
]
.right-column[
あるデータを３つ以上のグループのどれかに分類
- この料理は和食か中華かイタリアンかフレンチか
- この曲はロックかテクノかジャズかクラシックか
- このブログエントリのジャンルは生活か技術かネタかエンタメか
]

---

# 教師あり学習

.left-column[
## 二項分類
## 多項分類
## 回帰
]
.right-column[
値の予測
- 明日の日経平均株価はいくらか
- この製品の売上はいくらになるか
- 明日の気温は何度になるか
]

---

# 予測の種類

* ## バッチ
大量の入力データレコードに対する予測をリクエストする

* ## リアルタイム
個々の入力データレコードに対する予測をリクエストする


---
class: center, middle, inverse

# 3. Amazon Machine Lerning
# チュートリアルを試す
---

# 具体的に何をするの？

## AWSがサンプルとして用意している銀行の取引データ（学習用と検証用）を使う。学習用データからモデルを作成し、検証用データに列挙された取引データの取引中止者を予測する

---

# 流れ

## 1. データソースの用意
## 2. モデルの作成
## 3. モデルの精度評価
## 4. 予測

---

# 1. データソースの用意

* ### データソースとは学習や検証に用いるデータの置き場所
* ### Amazon MLではデータソースの取得元としてS3, Redshiftが指定可能
* ### マネジメントコンソールではなくAWS APIを使用すればRDSも指定できる
* ### Amazon MLで使用可能なデータとして整形してやる必要がある

???
Amazon Redshift は高速で管理も万全な、ペタバイト規模のデータウェアハウスサービス

---

# 1. データソースの用意

## 1) データのインポート
## 2) 各カラムのデータ形式を指定
## 3) 評価ターゲットの指定

---

# 1. データソースの用意
.left-column-ml[
### 1) データのインポート
]
.right-column-ml[
AWSの用意しているCSVファイルを用意

下記の学習用データではカラム`y`が取引成立の成否を表している

![](assets/201603_amazon_ml/img/00.uploaded-csv.png)
]

---

# 1. データソースの用意
.left-column-ml[
### 1) データのインポート
]
.right-column-ml[
サンプルデータファイルをS3のバケットにアップロード

* `banking.csv`は学習用データ
* `banking-batch.csv`は検証対象データ

![](assets/201603_amazon_ml/img/01.upload-csv-to-s3.png)
]

---

# 1. データソースの用意
.left-column-ml[
### 1) データのインポート
]
.right-column-ml[
先ほどアップロードしたCSVのうち学習用データを選択

![](assets/201603_amazon_ml/img/02.select-datasource-store.png)
]

---

# 1. データソースの用意
.left-column-ml[
### 1) データのインポート
]
.right-column-ml[
先ほどアップロードしたCSVのうち学習用データを選択

![](assets/201603_amazon_ml/img/03.select-datasource-store-verified.png)
]

---

# 1. データソースの用意
.left-column-ml[
### 1) データのインポート
]
.right-column-ml[
無事に読み込まれました

![](assets/201603_amazon_ml/img/04.datasouce-creation.png)
]

---

# 1. データソースの用意
.left-column-ml[
### 1) データのインポート
### 2) 各カラムのデータ形式を指定
]
.right-column-ml[
各カラムのデータ形式を指定します

![](assets/201603_amazon_ml/img/04.datasouce-creation.2.png)
]

---

# 1. データソースの用意
.left-column-ml[
### 1) データのインポート
### 2) 各カラムのデータ形式を指定
### 3) 評価ターゲットの指定
]
.right-column-ml[
評価ターゲットの指定
![](assets/201603_amazon_ml/img/05.datasouce-creation-target.png)
]

---

# 1. データソースの用意
.left-column-ml[
### 1) データのインポート
### 2) 各カラムのデータ形式を指定
### 3) 評価ターゲットの指定
### 4) 完了
]
.right-column-ml[
完了です

![](assets/201603_amazon_ml/img/08.datasouce-creation-done.png)
]

---

# 2. モデル構築

## 1) データソースの指定
## 2) 学習設定の方針選択

---

# 2. モデル構築
.left-column-ml[
## 1) データソースの指定
]
.right-column-ml[
データソースの指定
![](assets/201603_amazon_ml/img/09.model-input-data.png)
]

---

# 2. モデル構築
.left-column-ml[
## 1) データソースの指定
]
.right-column-ml[
データソースの指定
![](assets/201603_amazon_ml/img/10.model-input-data-chosen.png)
]

---

# 2. モデル構築
.left-column-ml[
## 1) データソースの指定
## 2) 学習設定の方針選択
]
.right-column-ml[
推奨設定を選択

![](assets/201603_amazon_ml/img/11.model-input-data-to-be-reviewed.png)
]

---

# 2. モデル構築
.left-column-ml[
## 1) データソースの指定
## 2) 学習設定の方針選択
]
.right-column-ml[
### 推奨設定

* 前処理はデータソースの統計情報から自動的に設定される
* 学習用データは分割され、7割を学習用、3割を学習モデルの評価用として利用する
* 学習パラメータはデフォルト値のままで設定する
]

---

# 2. モデル構築
.left-column-ml[
## 1) データソースの指定
## 2) 学習設定の方針選択
]
.right-column-ml[
### カスタム設定
1. 前処理の指定
    * グループ化
    * 中間変数の作成
    * アウトプット形式の指定
2. 学習パラメータの設定
    * 最大モデルサイズ
    * 最大データパス
    * 正則化のタイプ
    * 正則化の強さ
]

???
* グループ化
  複数のカラムをひとまとめのグループにできる（address1, address2 を addressにできる、て感じかな？）
* 中間変数の作成
  emailをすべて小文字に変換して lower_email というパラメータを作る

---

# 3. モデルの評価

AUCが0.94で精度が高いと評価されています

![](assets/201603_amazon_ml/img/14.performance-tuning-01.png)

---

# 3. モデルの評価

精度に手を加えたい際には閾値を変更することができます

![](assets/201603_amazon_ml/img/15.performance-tuning-02.png)

---

# 3. モデルの評価

* False Positive
* False Negative

![](assets/201603_amazon_ml/img/16.performance-tuning-03.png)

???
* False Positive もしかしたらNegativeかもしれない値
* False Negative もしかしたらPositiveかもしれない値

たとえばスパムメール検出なら大事なメールを見逃さないようにFalse PositiveをNegativeに寄せるように閾値を上げる
たとえば疾病検出なら多少怪しいものも見逃さないようにFalse PositiveをPositiveに寄せるように閾値を下げる

---

# 4. 予測結果の作成

今回はバッチ予測をおこないます


![](assets/201603_amazon_ml/img/17.batch-prediction-select-model.png)

---

# 4. 予測結果の作成

検証対象データがS3に置いてあるので選択します

![](assets/201603_amazon_ml/img/18.batch-prediction-create-datasoure.png)

---

# 4. 予測結果の作成

予測対象データが1000件につき0.10USドル必要だそうです

![](assets/201603_amazon_ml/img/20.batch-prediction-stored-setting.png)

???
今回はとくに見積もりができるようにしていませんが、ちゃんと設定したらおよその見積額が出るようです。
なお、今回の検証用データは4000件強なので50円くらいですかね。
---

# 4. 予測結果の作成

使用モデル、検証対象データおよび結果保存場所などが設定できました

![](assets/201603_amazon_ml/img/21.batch-prediction-review.png)

---

# 4. 予測結果の作成

しばらくするとステータスが`Completed`になりました

![](assets/201603_amazon_ml/img/22.batch-prediction-done.png)

---

# 4. 予測結果の作成

さっそく保存された結果のファイルを見てみます

![](assets/201603_amazon_ml/img/23.batch-prediction-result.png)

---

# 4. 予測結果の作成

さっそく保存された結果のファイルを見てみます


![](assets/201603_amazon_ml/img/24.batch-prediction-result-csv.png)

---
# 最後に

* ## 掘れば掘るほど深い
* ## 専門用語難しい
* ## これがしたい！というのが無いといまいち面白くない

