# Python基礎講習　分かち書き(形態素解析)
## 0.準備　Mecabのインストール　
https://qiita.com/yosemite2307/items/b73c24caa29fca415bba
このサイトを見て導入してわからなければ自分で調べるのもいいですし気軽に聞いて下さい。
## 1.分かち書き(形態素解析)とは
分かち書き（形態素解析）とは、英語のようにことばのくぎりに空白をいれる書きかたである。
例　お酒を飲み過ぎて気持ち悪い→お　酒　を　飲み　過ぎて　気持ち　悪い
## 2.Mecab
今回の形態素解析ソフトはMecabというソフトを使う。
MeCabは 京都大学情報学研究科−日本電信電話株式会社コミュニケーション科学基礎研究所 共同研究ユニットプロジェクトを通じて開発されたオープンソース 形態素解析エンジンです。
使い方
```python
import MeCab
mecab = MeCab.Tagger ("-Ochasen")
text = mecab.parse ("お酒を飲み過ぎて気持ち悪い")
print(text)
→
お	オ	お	接頭詞-名詞接続		
酒	サケ	酒	名詞-一般		
を	ヲ	を	助詞-格助詞-一般		
飲み	ノミ	飲む	動詞-自立	五段・マ行	連用形
過ぎ	スギ	過ぎる	動詞-非自立	一段	連用形
て	テ	て	助詞-接続助詞		
気持ち	キモチ	気持ち	名詞-一般		
悪い	ワルイ	悪い	形容詞-自立	形容詞・アウオ段	基本形
```
## 課題
課題１．Mecabを導入し好きな文章を入力し表示せよ。
課題２．下記のように分かち書きした単語を全て表示せよ。難しいが調べてチャレンジしてみよう。
表層系:お 表層系の読み:オ  原型:お 品詞:名詞接続
どうしてもわからない場合はヒントをあげますので気軽にお聞きください。