# LT木曜特選市
##### Ryo Uchino (<a href="https://github.com/rinfield" target="_blank">@rinfield</a>)
---
# 今日ご紹介するのは
---
# 今話題のプログラミング言語！
---
# Scala
---
# こんなことにお困りでは？
---
- ムダにコード量が多い |
- パフォーマンスが出ない |
- 一生懸命エラーの原因探していたら一文字のTypo |
- いろんな言語を覚えるのはもうたくさん |
---
# もう大丈夫です！
---
# コード量が増えてお困りの方
---
#### JavaのFizzBuzz

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
#### ScalaのFizzBuzz

```scala
object FizzBuzz extends App {
  (1 to 30).map { i =>
    (i % 3 == 0, i % 5 == 0) match {
      case (true,  false) => "Fizz"
      case (false, true)  => "Buzz"
      case (true,  true)  => "FizzBuzz"
      case _              => i.toString
    }
  }.foreach(println)
}
```
---
# 見て下さい！このボデー!!
---
# ✨キレイなコードを保つことができます！
---
# 🚀パフォーマンスはJavaと同等
### スクリプト言語には負けません！
---
# Typoなどの間違いもすぐに検出
---
# なんとこんなところで使われています！
---
- NASA
- Twitter
- Netflix
- その他有名企業も！
---
# Javaをお使いのあなた！
---
# なんとJava資産をそのままご利用いただけます！
---
# それだけじゃないんです！
---
# ​今回はなんと…
---
# ​ScalaをJavaScriptにできるツールもお付けしちゃいます
---

