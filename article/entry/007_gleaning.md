# 007. 落穂拾い

## 下書きの管理はどうすればよいか？

Rijiでは追随ブランチ(デフォルトではmaster)にコミットした記事は否応なしに公開されます。では公開したくない下書きの管理はどうすれば良いのでしょうか？

書き上がるまではコミットしないで手元に保存しておく？それはあまりスマートではありません。せっかくgitを使っているのですから、下書き用のブランチ(例えばdraft)を作り、そちらにコミットしておけばよいのです。書き上がったら、そっちのブランチから追随ブランチへcheckoutしてくれば良いでしょう。

## コメント機能について

Rijiではコメント機能を用意しておりません。DisqusのようなAjaxベースのコメント機能を利用するのが良いでしょう。

## 検索窓に関して

Googleのサイト内検索を使えば良いと思います

## 動的配信について

静的配信はめんどくさいから動的配信したいという人もいるかと思います。その場合は、自分のサーバーにリポジトリをpullして、`riji server`を直接動かしても良いでしょう。実は`riji server`は`plackup`と同じ引数を受け取ることができるので、`riji server -s Starman -p 9999`などと指定することも可能になっています。

注意点としては、コンテンツを追加しても、プロセスの再起動をしないと変更が反映されない部分があるということです。

コミットフック等を利用してサーバーがgraceful restartできるようになっていたりすると美しいですね。その辺り、うまい運用のやり方を編み出して作者に教えてもらえると嬉しいです。

## トラックバックに関して

残念ながらトラックバックはオワコンになりました。概念としては個人的に好きだったのですが、多くの人に誤った理解をされ誤った使い方をされた挙句廃れてしまったのは非常に残念に思っています。Rijiにはトラックバック機能はありません。

## その他機能追加要望に関して

使っているうちにXslateに関数を追加したい、プラグイン機構を入れたい、等色々要望は出てくるかと思います。

開発は以下で行なっているので随時pull requestやissueを投げていただけると非常に嬉しいです。

<https://github.com/Songmu/p5-Riji>

## 終わりに

もし、ここまで読んでいただけた方がいると大変嬉しいです。ぜひRijiを使ってみてください。フィードバックをいただけると作者は泣いて喜びます。