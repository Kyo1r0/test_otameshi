# Markdown Basic

これは buffet-seminar の Markdown 基礎編です．
これから Markdown の基本的な書き方を学んでいきます．

## Markdown とは

Markdown は，テキストベースの軽量マークアップ言語です．
Markdown を使うことで文章を記述する際の書式を簡単にすることができます．

早速 Markdown を使ってみましょう．以下に Markdown の書き方の例を示します．ここでは使う頻度の高いもののみを紹介します．詳しく知りたい方は [Markdown 記法 チートシート](https://qiita.com/Qiita/items/c686397e4a0f4f11683d) や [Markdown 記法 サンプル集](https://qiita.com/tbpgr/items/989c6badefff69377da7) などを参照してください．また，他にもウェブサイト特有の書き方がある場合があります．Qiita や Zenn などにも書き方の例がありますので，そちらも参考にしてください．今回の内容も [Markdown 記法 サンプル集](https://qiita.com/tbpgr/items/989c6badefff69377da7) とほぼ同じです．

# 見出し

1 個から 6 個シャープで見出しを記述する．
※シャープと見出し文字の間には半角スペースを 1 つ入れること．

記述例

```markdown
# 見出し 1

## 見出し 2

### 見出し 3

#### 見出し 4

##### 見出し 5

###### 見出し 6
```

表示例

# 見出し 1

## 見出し 2

### 見出し 3

#### 見出し 4

##### 見出し 5

###### 見出し 6

# 箇条書きリスト

ハイフン、プラス、アスタリスクのいずれかで箇条書きリストを記述可能。
※ハイフン、プラス、アスタリスクと箇条書きの項目の間には半角スペースを 1 つ入れること

記述例

```markdown
-   リスト 1
    -   ネスト リスト 1_1
        -   ネスト リスト 1_1_1
        -   ネスト リスト 1_1_2
    -   ネスト リスト 1_2
-   リスト 2
-   リスト 3
```

表示例

-   リスト 1
    -   ネスト リスト 1_1
        -   ネスト リスト 1_1_1
        -   ネスト リスト 1_1_2
    -   ネスト リスト 1_2
-   リスト 2
-   リスト 3

# 番号付きリスト

数値+半角ドットで番号付きリストを記述可能。
番号の内容は何でもいい。実際に表示される際に適切な番号で表示される。
そのため、一般的にはすべて 1. 内容 で記載すると変更に強く楽です。
※数値+半角ドットと箇条書きの項目の間には半角スペースを 1 つ入れること

記述例

```markdown
1. 番号付きリスト 1
    1. 番号付きリスト 1_1
    1. 番号付きリスト 1_2
1. 番号付きリスト 2
1. 番号付きリスト 3
```

表示例

1. 番号付きリスト 1
    1. 番号付きリスト 1_1
    1. 番号付きリスト 1_2
1. 番号付きリスト 2
1. 番号付きリスト 3

# 引用

記述例

```markdown
> お世話になります。xxx です。
>
> ご連絡いただいた、バグの件ですが、仕様です。
```

表示例

> お世話になります。xxx です。
>
> ご連絡いただいた、バグの件ですが、仕様です。

# 水平線

アスタリスク、ハイフン、アンダースコアを 3 つ以上並べると水平線を表示できます。

記述例

```markdown
---
```

表示例

---

# pre 記法

半角スペース 4 つもしくはタブでコードブロックを pre 表示できます．

記述例

```markdown
    # Tab
    class Hoge
        def hoge
            print 'hoge'
        end
    end

---

    # Space
    class Hoge
      def hoge
        print 'hoge'
      end
    end
```

表示例

    # Tab
    class Hoge
        def hoge
            print 'hoge'
        end
    end

---

    # Space
    class Hoge
    def hoge
        print 'hoge'
    end
    end

# コード記法

バッククォートでコードを囲むとインライン表示できます．

記述例

```markdown
インストールコマンドは `gem install hoge` です
```

表示例

インストールコマンドは `gem install hoge` です

# コードブロック記法

バッククォートを 3 つで囲むとコードブロックを表示できます．

記述例

    ```ruby
    class Hoge
        def hoge
            print 'hoge'
          end
    end
    ```

表示例

```ruby
class Hoge
    def hoge
        print 'hoge'
    end
end
```

# リンク

`[表示文字](URL)` でリンクを表示できます．

記述例

```markdown
[Google](https://www.google.co.jp/)
```

表示例

[Google](https://www.google.co.jp/)

# 画像

`![表示文字](画像URL)` で画像を表示できます．

記述例

```markdown
![画像](https://www.google.co.jp/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png)
```

表示例

![画像](https://www.google.co.jp/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png)
