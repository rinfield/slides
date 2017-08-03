# LT木曜特選市
##### Ryo Uchino (<a href="https://github.com/rinfield" target="_blank">@rinfield</a>)
---
# こんばんは❗️
---
# 今日ご紹介するのは‼️
---
# 今話題のプログラミング言語⌨️
---
# ![Scala](http://www.lyh.me/slides/images/scala-logo.png)
---
# こんなことにお困りでは❓
---
- 🤔ムダにコード量が多い
- 😱アプリのパフォーマンスが出ない |
- 😡一生懸命エラーの原因探していたら一文字のTypo |
- 😵いろんな言語を覚えるのはもうたくさん |
---
# もう大丈夫です💡
---
# コード量が増えてお困りの方✋
---
#### JavaのFizzBuzz🤔

```java
public class FizzBuzz {
  public static void main(String[] args) {
    for(int i = 1; i <= 30; i++) {
      boolean isDividableWith3 = i % 3 == 0;
      boolean isDividableWith5 = i % 5 == 0;
      String result;
      if(isDividableWith3 && isDividableWith5) {
        result = "FizzBuzz";
      } else if(isDividableWith3) {
        result = "Fizz";
      } else if(isDividableWith5) {
        result = "Buzz";
      } else {
        result = Integer.toString(i);
      }
      System.out.println(result);
    }
  }
}
```
---
#### ScalaのFizzBuzz😍

```scala
object FizzBuzz extends App {
  (1 to 30).map(i => (i % 3 == 0, i % 5 == 0) match {
    case (true,  false) => "Fizz"
    case (false, true)  => "Buzz"
    case (true,  true)  => "FizzBuzz"
    case _              => i.toString
  }).foreach(println)
}
```
---
# 見て下さい❗️このボデー‼️⤴️⤴️
---
# キレイなコードを保つことができます✨
#### 柔軟な構文＆型推論
---
# 🚀パフォーマンスはJavaと同等
#### JVMで動作、スクリプト言語には負けません
---
# 🔍Typoなどの間違いもすぐに検出
---
# ✅既にこんなところで使われています
---
<img src="https://www.nasa.gov/sites/default/files/images/nasaLogo-570x450.png" width="40%" height="40%" class="fragment">
<img src="https://g.twimg.com/dev/img/marketing/twitter-for-websites/header-logo.png" width="40%" height="40%" class="fragment">
<img src="https://p13.zdassets.com/hc/settings_assets/830444/200181708/3kZZmx88qLvtPxQcrCE1og-netflix-logo-small.png" width="40%" height="40%" class="fragment">

- その他有名企業も！ |
---
# 👀今Javaをお使いのあなた❗️
---
# なんとJava資産をそのままご利用いただけます‼️
---
# それだけじゃないんです❗️
---
# 今回はなんと…😮
---
# JSに出力できるScala.jsもお付けしちゃいます🎁
---
# サーバーサイドとフロントのコードを共有できるんです❗️
---
# 今流行りのReactにも対応💮
---
# JSの😫なところに悩む必要はありません❗️
---
# ちょっと待ってください✋
---
# 今回は今年3月に発表された新製品🆕
---
# Scala Nativeもお付けしちゃいます❗️🎁
---
# なんとScalaでネイティブアプリが作れちゃう❗️
---
## JVMが苦手な分野で活躍すること間違い無し❗️

- メモリ制約が多い
- 立ち上がりが早くないといけない
- ネイティブライブラリを使う
---
# Scalaさえあれば💡
---
- Web開発(Play!)
- マイクロサービス(Lagom) |
- スクリプティング |
- ビッグデータ(Spark) |
- フロントエンド開発 |
- 機械学習 |
---
- Androidアプリ
- Nativeアプリ |
- IoT |
- ゲーム |
- コマンドラインツール |
---
# 全部おまかせ❗️
---
# いかがでしょう⁉️
---
# Scala 3点セット
- Scala (JVM)
- Scala.js
- Scala Native
---
# 🤔「お高いんでしょう」とお思いでしょう❗️
---
# ガンバらせて頂きました
---
# 何と5000兆円引きの
---
# 0円！
---
# 金利手数料は負担いたします
---
# おアクセスお待ちしております
## http://www.scala-lang.org/
---
# 謝罪🙇
---
# Javaのコード意図的に冗長にしてました🙇
---
#### Before

```java
public class FizzBuzz {
  public static void main(String[] args) {
    for(int i = 1; i <= 30; i++) {
      boolean isDividableWith3 = i % 3 == 0;
      boolean isDividableWith5 = i % 5 == 0;
      String result;
      if(isDividableWith3 && isDividableWith5) {
        result = "FizzBuzz";
      } else if(isDividableWith3) {
        result = "Fizz";
      } else if(isDividableWith5) {
        result = "Buzz";
      } else {
        result = Integer.toString(i);
      }
      System.out.println(result);
    }
  }
}
```
---
#### After

```java
public class FizzBuzz {
  public static void main(String... args) {
    Stream.iterate(1, i -> i + 1).limit(30).map(i -> {
      String result = Integer.toString(i);
      result = (i % 3  == 0) ? "Fizz"     : result;
      result = (i % 5  == 0) ? "Buzz"     : result;
      result = (i % 15 == 0) ? "FizzBuzz" : result;
      return result;
    }).forEach(System.out::println);
  }
}
```
---
# Javaもガンバレばこんくらいにはなりますね😔
---
## Javaのイマイチポイント
- 🤔Tupleがないので割り切れるかどうか3回評価してる
- 🤔パターンマッチがないので三項演算子を代用してる
  - 短く書くために`result`が`final`じゃないし
  - 同じこと何回もかいててギチギチしてる
- 🤔セミコロン！
