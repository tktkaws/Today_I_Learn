# マークアップ

アクセシビリティ
マシンリーダブル
セマンティック　意味に基づいたマークアップ

# タグ

h タグ
heading
数字順に使用
ｐ　タグ　 paragraph 　段落（ひとかたまりの文章
br 　 break

ol 　順列リスト　 orderd リスト　 li を囲む

dl 　 descriptionlist 　項目名とその説明がセット
dt 　定義
dd 　項目の説明

a 　 anchor

nu html checker html の文法チェックツール

img alt 代替テキスト 音声ブラウザで読み上げられる 意味を持たない画像には空白

テキストにニュアンスを与えるタグ
em 　 emphasis 文章に強調のニュアンスを与えう r
strong 　非常に強い重要性をあらわす
mark 　検索結果の文章内で関連性がある箇所
i 　心の中の声など　周りの文章とは質が違うこと
b 　記事のリード文　意味的な重要性はないが注目させたいテキスト

table
tr th th th tr thead
tr td td td tr tbody
tr td td td tr tbody

address 連絡先

header
nav
main ページの主題になる箇所に一回だけ使用
article 自己完結している　ブログ記事　見出しとセット h1〜h6
完結している＝取り出しても意味が通じる　 twitter の投稿など
aside 　補足情報のエリア　省略してもメインコンテンツの意味がわかる
footer
section 見出しとその後に続く段落　アウトラインが明確になる
section 　 article aside nav はアウトラインを生成
article aside nav が使えるならそちらを使用

h1 を section に内包するとアウトラインがずれる

その他の新しいタグ
time 　日時が重要な意味を保つ場合に使用
datetime とセット

figure 自己完結している必要あり
figurecaption 　補足説明を記述できる　必須ではない
figure に該当している
・本文内では画像について言及していない
・本文に関係のある画像
figure に該当していない
・本文で下の画像のように　と言及している
・本文に直接関係のないイメージ画像
small 　著作権や免責事項など　習慣的に小さくする箇所

# 画像の種類

svg 拡大縮小をしてもボケない　複雑ではない図形やアイコンイラストに向いている　高解像度ディスプレイ対応
jpg 　写真　グラデーション　色数が多い画像に向いてる　圧縮率が高い　ファイルサイズが小さい　透過処理ができない　保存し直すたびに画質が劣化
png 　ベタ塗り中心線画のイラストに向いてる　 jpg より思い　透過処理ができる　保存し直しても劣化しない
webp 　 jpg よりも軽い　透過処理できる　保存し直しても画質が劣化しない　アニメーションも可能　 adobe が公式対応していない　普及はいつから？

CSS

# ボックスモデル

ブロックボックス
display: block;
.横いっぱいに広がり積み重なる
・width と height の指定ができる
・margin と padding を四方に指定できる

インラインボックス
display: inline;
・横に並ぶ
・width と height の指定ができない
（要素の中身によって変化する）
・margin と padding は左右のみ指定できる

.margin\_\_shorthand {
border: 3px solid #fffff;
solid double dotted dashed

/_ 上下　左右 _/
margin: 10px 20px;
/_ 上　左右 下 _/
margin: 10px 20px 5px;
// 上　右 下 左 時計回り
margin: 10px 20px 5px 3px;
}

.hoge {
/_ padding と border が width に含まれない _/
box-sizing: content-box;

// インライン要素の中央寄せ
text-align: center;
border-radius: 5px 5px 5px 5px;
}
