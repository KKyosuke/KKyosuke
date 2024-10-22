# Code Review Perspectives
## PR
ure that the title and content are described with the following points of view.

### Title
* Is it possible to tell what the change was based on by the title alone?
  * Is the identifier of the corresponding ticket number or function listed?
  * Are the correspondence details described in text as well as identifiers?

### Contents
* Contents of changes
  * What kinds of changes did you make?
  * Why did you make those changes?
  * etc..
* Changed codes
  * What codes where changed in detail?
  * How did you think and decide to change in that way?
  * etc..
* Additional information needed to check the PR
  * If you have added a package, a link that shows what you have added
  * Include information that cannot be confirmed unless you know
* Test point of view
  * Describe what kind of test you did
  * Paste evidence
* Related Pages
  * Describe the page you referred to, PR, etc.

## Regarding comments
I would like to add a prefix to the beginning of the comment as follows, so please respond accordingly

* must:
  * 「must」 = Must be supported
* want:
  * 「want」 = Feelings to be addressed if possible.
* nits:
  * 「nitpick」 = It's a minor point (meaning “poking in the corner of a heavy box”), so I don't care whether it's handled or not.
* Q:
  * 「Question」= Question for an answer (I'd like to know the thoughts that led to that output)

## コード
Check the following aspects

* [Confirmation of IN and OUT](./review.md#in%E3%81%A8out%E3%81%AE%E7%A2%BA%E8%AA%8D)
* [Logic Confirmation](./review.md#%E3%83%AD%E3%82%B8%E3%83%83%E3%82%AF%E3%81%AE%E7%A2%BA%E8%AA%8D)
* [Test comprehensiveness](./review.md#%E3%83%86%E3%82%B9%E3%83%88%E3%81%AE%E7%B6%B2%E7%BE%85%E6%80%A7%E3%81%AB%E9%96%A2%E3%81%97%E3%81%A6)
* [Confirmation of description method](./review.md#%E8%A8%98%E8%BC%89%E6%96%B9%E6%B3%95%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6%E3%81%AE%E7%A2%BA%E8%AA%8D)
* [Naming](./review.md#%E5%91%BD%E5%90%8D%E3%81%AB%E9%96%A2%E3%81%97%E3%81%A6)
* [Granularity of class/function partitioning](./review.md#%E3%82%AF%E3%83%A9%E3%82%B9%E9%96%A2%E6%95%B0%E3%81%AE%E5%88%86%E5%89%B2%E7%B2%92%E5%BA%A6%E3%81%AB%E9%96%A2%E3%81%97%E3%81%A6)
* [Comment volume](./review.md#%E3%82%B3%E3%83%A1%E3%83%B3%E3%83%88%E9%87%8F%E3%81%AB%E9%96%A2%E3%81%97%E3%81%A6)

### Confirmation of IN and OUT
必須対応になる
実装したコードのインプットとアウトプットがI/Fなどの理想としているものと同じであることを確認する。
* 画面の時
  * 呼び出しパラメータの妥当性の確認。
* APIの時
  * リクエストとリスポンスの妥当性の確認

### Logic Confirmation
実装が合っているかを以下の様な観点から確認する。
以下のようなポイントで確認する
* 取得SQLの条件設定が合っているのか？
* 追加、更新、削除のパラメータがあっているのか？
* 処理内の条件分岐に問題がないのか？
* エラーハンドリングがちゃんとできているのか？

### Test comprehensiveness
テストの網羅性について以下のような観点から確認する。
* テストコードがある場合には
  * 書き方があっているのか？
  * パターン分網羅できているのか？
  * テストの実行速度に悪影響を与えてないのか？
* テストコードがない場合には
  * 代わりにどのようなテストを行ったか記載があるのか？
  * 実行した結果が気さされているのか？
  * 十分なパターンをもうらしているのか？

### Confirmation of description method
プロジェクト全体の平仄に従ってるか、以下の観点から確認する。
* 全体の実装フローは同じ様になっているか？
  * example) controller→transaction→service→repositoryとなっている構造の場合にそれに従っているか 
* 命名規則に統一感があるのか？ 
* ファイルの分割粒度に統一感はあるのか？

### Naming
わかりやすい命名になのか、以下の観点から確認する。
* 実体系（クラス・フィールドなど）
  * 何の実体かわかる命名になっているのか？
  * 何の値がフィールドに格納されているかわかる様になっているのか？
* 動作系（関数など）
  * 動詞から始まっているのか？
  * 関数内部の処理を簡潔に表せているのか？
  * 何を返却するのか名前からわかる様になっているのか？  

### Granularity of class/function partitioning
関数の中の処理は極力シンプルになるように心がける。  
こちらができてないと可読性の低下や関数を作ってない人が使用した時の認識齟齬を生みバグの原因となることがある。  
関数名と処理がどうしても一致しない場合には粒度に問題がある可能性もあるのでファイル分割を勧める。  

### Comment volume
基本的には命名で大まかなフローは掴める様にしたいが、複雑な処理や特別な処理の場合にはコメントを残した方が可読性が上がる。  
複雑な仕様（ロジック）が組み込まれる場合にはコメントを追記することを推奨する。  
※ コメントの言語はそのプロジェクトの方針に合わせる  

