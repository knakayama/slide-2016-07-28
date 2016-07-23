layout: true
class: center, middle

---
# オートスケーリンググループはともだち、こわくないよ
## knakayama

---
# 自己紹介

---
# knakayama(中山 幸治)&nbsp;![knakayama](https://avatars2.githubusercontent.com/u/1545919?v=3&s=400)
### [https://knakayama.github.io](https://knakayama.github.io)
### ![PSA](images/PSA.png)

---
# クラスメソッド![classmethod](https://pbs.twimg.com/profile_images/344513261567475947/516b99bf0b40c0354dfad345ef14051a_400x400.png)<br/>AWSコンサルティング部<br/>所属

---
background-image: url(http://cdn.dev.classmethod.jp/wp-content/uploads/2016/06/new_osaka_office_front_800-e1465205568251.jpg)

---
background-image: url(http://cdn.dev.classmethod.jp/wp-content/uploads/2016/06/new_osaka_office_front_800-e1465205568251.jpg)
**クラスメソッド<br/>大阪オフィス<br/>爆誕**

---
background-image: url(http://cdn.dev.classmethod.jp/wp-content/uploads/2016/06/new_office_naka-e1465280928774.jpg)

---
background-image: url(http://cdn.dev.classmethod.jp/wp-content/uploads/2016/06/new_office_naka-e1465280928774.jpg)
**オサレ系<br/>オフィス**

---
background-image: url(http://cdn.dev.classmethod.jp/wp-content/uploads/2016/06/new_office_naka-e1465280928774.jpg)

---
background-image: url(images/osaka-office-osare.jpg)

---
background-image: url(http://cdn.dev.classmethod.jp/wp-content/uploads/2016/06/new_office_naka-e1465280928774.jpg)

---
background-image: url(http://cdn.dev.classmethod.jp/wp-content/uploads/2016/06/new_office_naka-e1465280928774.jpg)
**オサレ系<br/>オフィス**

---
background-image: url(images/osaka-members.png)

---
background-image: url(images/osaka-members.png)
**メンバーは<br/>まだ3人だけ<br/>(2016年7月)**

---
**絶賛人材<br/>募集中**

---
**まだ間に合う**

---
**こんな話聞いてる場合じゃない**

---
**絶賛人材<br/>募集中**

---
background-image: url(http://cdn.dev.classmethod.jp/wp-content/uploads/2016/07/mesoko_01.png)
## http://classmethod.jp/recruit/jobs/

---
background-image: url(http://cdn.dev.classmethod.jp/wp-content/uploads/2016/07/mesoko_01.png)
**まだ間に合う**
## http://classmethod.jp/recruit/jobs/

---
background-image: url(http://cdn.dev.classmethod.jp/wp-content/uploads/2016/07/mesoko_01.png)
**絶賛人材<br/>募集中**
## http://classmethod.jp/recruit/jobs/

---
# 今日の資料↓に置いときました
### [https://knakayama.github.io/slide-2016-07-28](https://knakayama.github.io/slide-2016-07-28)
### 「knakayama」とかでググれば出てくると思います

---
layout: true
class: center, middle

---
# アジェンダ

---
layout: true
class: middle

---
## 1. オートスケーリンググループの基本
## 2. オートスケーリンググループの詳細
## 3. オートスケーリンググループの注意点
## 4. もっと知りたい方へのおすすめリンク

---
layout: true
class: center, middle

---
# 1. オートスケーリンググループの基本

---
# 唐突ですが<br/>こんな経験無いですか?

---
# アクセス増加でサーバが<br/>落ちた

---
### 通常のアクセス数の場合<br/><br/>![access-normal](images/access-normal.png)

---
### アクセスが急増した場合<br/><br/>![access-high](images/access-high.png)

---
# オートスケーリンググループでそれ解決できます
### # 一部を除く

---
# 改めてオートスケーリンググループとは?

---
# オートスケーリンググループ<br/> == <br/>「オートスケール」するインスタンスの集まり(グループ)

---
# オートスケール?

---
# *オートスケールは、クラウドコンピューティングで利用しているサーバーなどの台数を自動的に増減する技術、あるいはサービス。*
### http://www.nttpc.co.jp/yougo/オートスケール.html

---
# オートスケーリンググループ<br/> == <br/>オートスケール(自動で増減)<br/>するインスタンスの集まり(グループ)

---
layout: true
class: middle

---
## - サーバを増加させる == スケールアウト
## - サーバを減少させる == スケールイン

---
layout: true
class: center, middle

---
# 2. オートスケーリンググループの詳細

---
# ちなみに<br/>オートスケーリンググループ<br/> == <br/>Auto Scaling Group<br/> == <br/>ASG

---
layout: true
class: middle

---
## 2-1. 起動設定(ローンチコンフィギュレーション)
## 2-2. スケーリングポリシー
## 2-3. インスタンスの起動数

---
layout: true
class: center, middle

---
# 2-1. 起動設定

---
layout: true
class: middle

---
### - ASGで起動させるインスタンスの設定
### - どういったインスタンスで起動させるかを指定する
### - 例: メモリは1GB、ストレージは8GB、etc...
### - 1つのASGには必ず1つの起動設定を指定する
### - ASGの作成時やスケールアウトする時にこの起動設定に基づいたインスタンスが起動する

---
layout: true
class: center, middle

---
# 2-2. スケーリングポリシー

---
# その前にCloudWatchの解説

---
layout: true
class: middle

---
### - AWSの「監視」サービス
### - AWSのさまざまなメトリクスを収集(CloudWatch Metrics)
### - 集めたメトリクスのアラート設定が可能(CloudWatch Alarm)
### - アラート検知時に特定のアクションを実行可能

---
layout: true
class: center, middle

---
### CloudWatch Metricsのイメージ<br/><br/>
![cloudwatch-metrics](images/cloudwatch-metrics.png)

---
### CloudWatch Alarmのイメージ<br/><br/>
![cloudwatch-alarms](images/cloudwatch-alarms.png)

---
# 改めてスケーリングポリシーについて

---
layout: true
class: middle

---
### - どういった条件でオートスケールさせるかという設定
### - CloudWatchとひも付けることができる
### - メトリクスの閾値を超過した場合にオートスケールさせることが可能
### - 例: アクセスが増加したのでスケールアウト
### - 例: CPU使用率下がったのでスケールイン

---
layout: true
class: center, middle

---
### CloudWatchとASGの連携<br/><br/>
![cloudwatch-asg](images/cloudwatch-asg.png)

---
# 2-3. インスタンスの起動数

---
# オートスケーリンググループはどれくらいインスタンスを起動したいかを指定できる

---
layout: true
class: middle

---
### - max(最大起動数) -> 最大でもこの数しか起動しない
### - min(最低起動数) -> 最低でもこの数は起動させる
### - desired(希望起動数) -> 常にこの数を起動させようとする

---
### - maxが3 -> スケールアウトしてもインスタンス数を3つ以上には増加させない
### - minが1 -> スケールインしてもインスタンス数を最低1つ維持しようとする
### - desiredが2 -> インスタンスの数を常に2つに維持しようとする

---
layout: true
class: center, middle

---
# max/min/desiredの数を変更すれば手動でスケールさせることも可能

---
# 実はオートスケーリンググループだからといってスケーリングポリシーを設定しないといけないわけではない

---
layout: true
class: middle

---
### - オートスケーリングさせずに常に1台は起動させたい場合はある
### - 踏み台用サーバなど
### - max/min/desiredを全て1にするとインスタンスが死んでも自動で新しく作り変えてくれる
### - オートヒーリングパターン
#### http://www.slideshare.net/kazukiueki76/20130823-cloudpacknight-lt

---
layout: true
class: center, middle

---
# 3. オートスケーリンググループの注意点

---
layout: true
class: middle

---
### - 急激なアクセス増加の場合スケールアウトが間に合わない場合がある
### - インスタンスが起動するだけでサービスインできる仕組みを整えておく必要がある(デプロイ)
### - スケールインしてインスタンスが消去されても問題ない構成にしておく必要がある(ステートレス)

---
layout: true
class: center, middle

---
# 4. もっと知りたい方へのおすすめリンク

---
layout: true
class: middle

---
### - AWS Black Belt Techシリーズ Amazon CloudWatch & Auto Scaling
#### http://www.slideshare.net/AmazonWebServicesJapan/aws-black-belt-tech-amazon-cloudwatch-auto-scaling
### - Amazon CloudWatch の名前空間、ディメンション、メトリックスのリファレンス
#### https://docs.aws.amazon.com/ja_jp/AmazonCloudWatch/latest/DeveloperGuide/CW_Support_For_AWS.html
### - AWSのオートスケールとなかよく付き合う
#### https://speakerdeck.com/fujiwara3/awsfalseotosukerutonakayokufu-kihe-u
### - Developers.IO
#### http://dev.classmethod.jp/

---
layout: true
class: center, middle

---
# 注意点もあるけど

---
# それでも

---
# オートスケーリンググループはともだち、こわくないよ

---
# おわり
