# 課題　じゃんけんアプリ「JANKENTALE」

<img src ="https://user-images.githubusercontent.com/113824527/198418258-d7ac987c-3831-4d0f-9f65-95437b3e8a50.png" width="600px">

## ①課題内容（どんな作品か）
- 大好きなゲーム「[UNDERTALE](https://store.steampowered.com/app/391540/Undertale/?l=japanese)」のパロディで、敵(イノウエ)と戦う「JANKENTALE」を作りました。
- プレイヤーは「さそう」「チーズ(をたべる)」「みのがす」という行動をとれます。
- プレイヤーの選択によってヒットポイント(HP)が増減し、3種類のエンディングに分岐します。
  - 「ハッピーエンド」「ノーマルエンド」「XXXエンド」があります。ぜんぶ見られるかな…！？
### 「さそう」について
- じゃんけんの機能にあたるコマンドです。
- プレイヤーの選択と、イノウエの選択の結果によって勝敗が決まり、100〜200HP増減します。
- プレイヤーは「のみかい」「すいみん」「ジーズのかだい」の3種類を選べます。
- 「ジーズのかだい」は「のみかい」に勝利するが「すいみん」には負ける…というように、三すくみになっています。
### 「チーズ」について
  - 回復コマンドです。ランダムで50〜150HP回復します。
  - 初期値は2個であり、増えることはありません。
### 「みのがす」について
  - ある条件を満たすと使えるようになるコマンドです。最初は選択することができません。

## ②工夫した点・こだわった点
- 共通の処理は関数にまとめた
  - じゃんけん(さそうコマンド)の勝敗結果は9種類用意したかったので、win(), lose(), tie()という関数を用意し、「HPの増減」「画像の表示」といった共通の操作をまとめることで、コードが少しスッキリしました。
  - プレイヤーの選択を数字に変換する方法を何パターンか調べましたが、attrメソッドで属性を取得する方法がきれいだと思ったので使ってみました。

- エンディング分岐
  - 最初にエンディングの条件達成のフラグを変数でもたせ、プレイヤーの選択によってonにすることで、エンディング分岐の場合分けを作りました。
  - いちど特定のエンディングになると、画面をリフレッシュしない限り、どう操作してもほかのエンディングに行けないようにすることに地味にこだわりました。

## ③難しかった点・次回トライしたいこと(又は機能)
### しくじりコード 〜オレみたいになるな！〜
- 関数内で定義した変数を関数の外で使ってエラー！
- idを複数指定していてエラー！
- カウントするための変数にconstを使い、再代入ができなくてエラー！

### 次回トライしたい機能
- プレイn週目で結果が変わるというのをやってみたかった。
- Github pagesで公開した後、寝る前にスマホでプレイしようとしたら、全然ボタンが押せなくてすごく萎えたので、レスポンシブ対応まではいかなくても普通になんとかしたいと思った。

## ④質問・疑問・感想、シェアしたいこと等なんでも
### 質問・疑問 
- まだじゃんけんなのでなんとかなっているが、もっと複雑な場合分け等が必要な場合は、どう整理するのが良いでしょうか。

###  参考記事
- JavaScript / jQuery
  - [【怖くないJavaScript + jQuery】if文のいつもと違った使い方](https://blog.8bit.co.jp/?p=13883)
  - [【JavaScript】var / let / const を本気で使い分けてみた](https://qiita.com/cheez921/items/7b57835cb76e70dd0fc4)
  - [【JavaScript入門】setTimeoutの使い方とサンプル事例まとめ！](https://www.sejuku.net/blog/24540)
  - [JavaScriptでif文の中で関数を定義する](https://kimizuka.hatenablog.com/entry/2015/05/05/000000)
  - [JavaScript: if else if文で何もしない場合の書き方](https://step-learn.com/article/javascript/168-if-nothing.html)
  - [jQueryでシンプルなポップモーダルアップを実装する](https://mgmgblog.com/?p=641)
  - [「OK/キャンセル」ダイアログを表示して確認・分岐する方法](https://www.nishishi.com/javascript-tips/confirm-dialog.html)

- HTML / CSS
  - [HTMLコーダー必見のdl dt ddタグの基礎から応用まで！](https://ferret-plus.com/5063?page=2)
  - [CSSで要素を上下や左右から中央寄せする7つの方法](https://www.granfairs.com/blog/staff/centering-by-css)
  - [グローバルナビゲーション-ドロップダウンメニュー（上）-](https://coco-factory.jp/ugokuweb/move01/5-1-1/)
  - [CSSで背景を画面サイズいっぱいに広げる！フルスクリーンの作り方](https://jajaaan.co.jp/css/css-full-screen/)
  
- そのほか
  - [Visual Studio CodeでMarkdownをプレビューする](https://qiita.com/k_maki/items/d2ed604ac967e029c9a9)
  - [OGPの正しい設定方法を解説！Facebook・Twitter対応](https://mirai-creators.com/2199/)
