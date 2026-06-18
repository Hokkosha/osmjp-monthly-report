# こんにちは。OSMでインドアマッピングができないか検討しています。

## 2026-05-02 23:37
kzmi

おかげさまでインドアマッピング1投目を遂げることができました ❤️🙏


# こんにちは。OSMでインドアマッピングができないか検討しています。

## 2026-05-02 23:42
kzmi

JOSMでの編集も初めて試しました。懸念だったフロアごとの編集も、一度編集開始してみるとここにフィルタが出まして、さほど苦労することなく編集できましたのでメモしておきます 🗒️


# こんにちは。OSMでインドアマッピングができないか検討しています。

## 2026-05-03 19:24
alt9800

素晴らしすぎる〜！


# こんにちは。OSMでインドアマッピングができないか検討しています。

## 2026-05-09 01:28
alt9800

OSMの本サーバーにマージする前に、indoorのプレビューが適宜できるといいかもな〜と思いつつ、イベント用の誘導ツールを作ってみました。



---

# （NSI追加提案）提案されないチェーン店をまとめる

## 2026-05-09 12:54
tom_konda

スプレッドシート更新しました。


# （NSI追加提案）提案されないチェーン店をまとめる

## 2026-05-16 19:31
yuzishenniyaoha

スプレッドシートの様子を見たので、登録済み専用ページへの転記を行いました
自動的な方法があっても良さそうだけど開発する気なし…


# （NSI追加提案）提案されないチェーン店をまとめる

## 2026-05-16 19:35
yuzishenniyaoha

地図そのものは基本的に時間が経つと実際の状況も変わるけど、ブランドデータは網羅したらそれほど増えなくなる（新しいブランド自体は頻繁に生まれるものの、登録目安の30～50件まで増えるものは頻繁に無いので）



---


---


---

# ファストフードとレストランの境界

## 2026-05-09 23:16
okadatsuneo

taginfoで見たら90件登録されているので、使ったら良いと思いますよ。
ただレストランは「テーブル席でサービスを受けて飲食をする」のが定義のようなので、高級仕出しでもfast_foodでしょうね。
https://taginfo.openstreetmap.org/tags/cuisine=bento



---

# 道路幅が狭い都道府県道・国道について

## 2026-05-28 07:23
naminami_t

なお、希望は残らない



---


---

# RapiD_Plateau

## 2026-05-09 17:16
nyampire3568

@okadatsuneo @Ryo-a 追加しました！（世田谷区・渋谷区・新宿区・中野区・豊島区）


# RapiD_Plateau

## 2026-05-09 22:02
okadatsuneo

ありがとうございましたー。


# RapiD_Plateau

## 2026-05-11 11:09
nyampire3568

ついでに、作業済の地域をサーバのDBから削除する機能をつけました。
これで、新しいものも追加しやすくできそうです。


# RapiD_Plateau

## 2026-05-11 20:19
nyampire3568

Plateauデータがどこにあるのかわかりづらいな、と思ったので、Zoom5-14ではオレンジのポリゴンを表示するようにしました。
これで、対象の場所に行きやすくなったはず。


# RapiD_Plateau

## 2026-05-11 21:46
samrobot

高知市を追加できますか？


# RapiD_Plateau

## 2026-05-11 22:11
nyampire3568

@kuroshiokun 追加しました。
ただ、もしかしたら、データの対象区域が、都市計画地域だけかもしれません。
郊外の地域のデータが無さそう。みてみてください！

https://rapid.nyampire.info/#map=18.84/33.57626/133.55135&background=MAPNIK


# RapiD_Plateau

## 2026-05-11 22:21
samrobot

ありがとうございます


# RapiD_Plateau

## 2026-05-11 22:39
nyampire3568

ところどころ、こういうかんじの、ノードが欠落しているデータがあるので、ご注意ください。
適度に形状修正していただくかんじで。
なにが原因なのかは、別途調べようかな、と思います（他のところでも見かけたので）

あと、Bingなどの画像が荒いので、航空写真が使いたいところ。
Plateauの航空写真は無いですが、公共測量で毎年（！）撮影しているようなので、OSMFJとして使用申請はできます。

最新ではないですが、令5四公第10号　が、山間部もカバーされていてよさそう。


# RapiD_Plateau

## 2026-05-12 11:59
nyampire3568

調べたら、バグっぽい。予定つけて直します。


# RapiD_Plateau

## 2026-05-12 14:13
okadatsuneo

citygml変換後のファイルでtype=buildingのリレーションになっている建物もおかしくなっているような気がしたので、見てみて下さい。


# RapiD_Plateau

## 2026-05-14 20:50
nyampire3568

relationを追加する機能がRapidにそもそも無かったようなので、それを含めて開発中です。
わりと多くの建物（ざっと10-20%くらい）が抜けてるみたいです。
もうちょっとで開発終わる、はず。


# RapiD_Plateau

## 2026-05-14 20:51
nyampire3568

三角形など、頂点が抜けていたバグについては、修正しました。まだ全国分の入れ替えはできてないのですが、Relationの機能改修とあわせて適用予定です。


# RapiD_Plateau

## 2026-05-15 21:41
nyampire3568

ひとまず、
* 頂点ノードが削除されてしまうバグ
* relation (type=building) の追加ができない

という点を修正しました。
データの更新が必要で、まだ高知市しか対応できていないですが、いったんMilestoneかな、と思います。

このあたりにいっぱい、Multipolygonがあります。
https://rapid.nyampire.info/#map=20.00/33.57267/133.51761&background=MAPNIK


# RapiD_Plateau

## 2026-05-16 21:05
okadatsuneo

上記のリンクのあたりを見てみましたが、マルチポリゴンのオブジェクトを選択すると、それを適用する時に出てくる「+ Add This Feature」のボタンが「+ Missing zh translation: ～～」というボタンに変わるのですが、何なのでしょうか？


# RapiD_Plateau

## 2026-05-16 21:10
nyampire3568

翻訳テキストの不足、というやつで、バグのひとつなので、ローカルでは直してます。
近日中には修正をデプロイします！


# RapiD_Plateau

## 2026-05-21 20:10
nyampire3568

壊れていたジオメトリの入れ替えと、relation対応をしています。
たぶん明日くらいまで、データ入れ替えかかります


# RapiD_Plateau

## 2026-05-23 14:24
nyampire3568

作業完了しました。
マルチポリゴン建物の取り込みができるようになったのと、頂点が削れていた建物の修正ができています。


# RapiD_Plateau

## 2026-05-23 14:25
nyampire3568

また、サーバの容量を増強しました。
他にも対象の都市を増やせると思いますので、リクエストあればぜひ。


# RapiD_Plateau

## 2026-05-24 21:58
okadatsuneo

@nyampire マルチポリゴンの追加動作でAdd Entire Featureのボタンの上にマウスカーソルを持っていった時のポップアップ表示の説明の中でショートカットが「Shift+A」となっていますが、これは「A」ですよね？(実際の動作を見たところ..)


# RapiD_Plateau

## 2026-05-24 23:02
nyampire3568

はい、aです。
さすがに誰も気づかんだろう、と思ったら、早かった！
明日には直るとおもいます。


# RapiD_Plateau

## 2026-05-26 09:58
nyampire3568

直しました！


# RapiD_Plateau

## 2026-05-30 16:58
nyampire3568

作業進捗ダッシュボードを作ってみました。
各市町村の作業状況を一覧化できます。

なお、進捗はPlateauのオブジェクトを100、として割合を計算していますが、必ずしもPlateauが正しいわけではないので、インポート完了していても割合は100にはなりません。（だいたい90％以上くらいになる）

https://rapid.nyampire.info/dashboard/


# RapiD_Plateau

## 2026-05-30 16:59
nyampire3568

あと、Rapidの上のツールバーに、ダッシュボードとかのリンクを配置してみましたが、 missing translationのエラーがでます。
そのうち直すので、今日のところはこれでご容赦ください（）


# RapiD_Plateau

## 2026-05-30 17:00
nyampire3568

これね。


# RapiD_Plateau

## 2026-05-30 20:42
nyampire3568

シークレットウィンドウだとちゃんとでたので、キャッシュの問題だとは思います。そのうち直るはず。


# RapiD_Plateau

## 2026-05-31 20:29
okadatsuneo

@nyampire githubのissueに2件登録したので、またご確認のほどよろしくお願いします。



---

# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-12 23:55
canunen_tomtom

TomTomは、日本の国土交通省（MLIT）が公開するProject PLATEAUのオープン3D都市モデルデータセット（CC BY 4.0 / ODbL互換ライセンス）を活用し、OpenStreetMapの建物に不足している高さ情報を自動的に追加するプロセスに取り組んでいます。

**概要**

このプロセスでは、幾何学的コンフレーション（空間照合）を使用して、PLATEAUの建物フットプリントを既存のOSM建物と空間的にマッチングします。オーバーラップ率、面積比較、ジオメトリの妥当性チェックなど、複数の検証を行います。マッチした建物のうち、height=* タグがまだ付与されていないものだけが更新対象となります。 既存のタグが上書きされることはなく、建物のジオメトリが変更されたり、新しい建物が作成されることもありません。

**パイロット計画**

今週、TTmechanicalupdates OSMアカウントを使用して、大阪で小規模なテストを実施する予定です。問題が見つかった場合は、チェンジセットをリバートします。パイロットが成功した場合、大阪全域に対してプロセスを拡大する予定です。

**今後のステップ**

コミュニティへの相談 — フィードバック、ご質問、ご提案を歓迎します。このプロセスがコミュニティの期待に沿うものであることを確認したいと考えています。
OSM Wikiドキュメント — 詳細なプロセスドキュメントは、OSM Wiki上のTomTomの組織的編集ページに公開予定です。

皆さまのご意見をお待ちしております。

よろしくお願いいたします。



TomTom is working on an automated process to add missing building heights to OpenStreetMap using Japan's Project PLATEAU open 3D city model datasets (published by MLIT under CC BY 4.0 / ODbL-compatible terms).

**What we are doing**

Our process uses geometric conflation to spatially match PLATEAU building footprints against existing OSM buildings, using several validation checks including overlap percentage, area ratio comparison, and geometry validity. Only buildings that match and do not already have a height=* tag will be updated. No existing tags will be overwritten, no building geometries will be modified, and no new buildings will be created.

**Pilot plan**

We are planning to run a small-scale test in Osaka this week using the TTmechanicalupdates OSM account. If any issues are found, we will revert the changesets. If the pilot is successful, we plan to expand the process to cover the entire Osaka area.

**Next steps**

Community consultation — All feedback, questions, and suggestions are very welcome. We want to make sure this process aligns with community expectations.
OSM Wiki documentation — Full process documentation will be published under TomTom's organised editing page on the OSM Wiki.

We look forward to hearing your thoughts.

Best regards,

Can Ünen


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-13 10:36
nyampire3568

ありがとうございます。
いつかやりたいな、と思っていた作業なので、個人的には実施を歓迎します。
大阪市は既にPlateauのインポートも完了しており、既存の建物も多くが既に書かれています。

3つほど、懸念を示させてください。

* 実施対象の都市
大阪はPlateauのインポートが完了していますが、もともと、非常に入り組んだ大都市であり、作業自体の難易度が高いのではないかと推測されます。
他の、もう少し小規模な都市を対象にすることは選択肢としてありえるのでしょうか。

* ドキュメンテーション
なんとなく作業のイメージはつきますが、より詳しい内容について、まず実施前にOSM wikiへのドキュメンテーションをお願いできるでしょうか。
試行とはいえ、実データを対象とする編集ですので、Import guidelineおよび組織的編集のガイドラインに沿って、大枠としてでも作業内容を透明化しておきたいです。

* アナウンスメント
このDiscordは最近いちばん活発なJapanコミュニティスペースです。
ただ、古くから参加しているひとは特に、Talk-ja MLでの告知を重視する傾向があります。

そちらにも、アナウンスをお願いできるでしょうか。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-13 17:37
canunen_tomtom

Thank you for your great feedback. I agree with the mentioned complexity, and that is why we want to first run a controlled test edit on a very small number of buildings to see whether it works well or not before moving forward. 

We already have a draft for the OSM Wiki documentation, and I will publish it today for your review. I will also repeat this message, including the Wiki link to Talk-ja ML so the wider community is informed. 

Until the above mentioned tasks are done, we won't go forward with the test edit. 

I would then share the outcome of the small-scale test edit with you, before importing all Osaka. 

==========

フィードバックをいただきありがとうございます。ご指摘の複雑さについては同意しており、だからこそまず非常に少数の建物を対象に、制御されたテスト編集を実施し、うまく機能するかどうかを確認したうえで次のステップに進みたいと考えています。

OSM Wikiドキュメントのドラフトはすでに準備しており、本日中にレビュー用として公開いたします。また、Wikiリンクを含めたこのメッセージをTalk-ja MLにも投稿し、より広いコミュニティにも情報が届くようにいたします。

上記の作業が完了するまで、テスト編集には着手しません。

その後、大阪全域のインポートに進む前に、小規模テスト編集の結果を皆さまと共有させていただきます。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-13 21:08
canunen_tomtom

Please see the corresponding Wiki Page for the work: 

https://wiki.openstreetmap.org/wiki/Organised_Editing/Activities/TomTom/Global_-_Building_Height_Imports/Japan_-_PLATEAU_Building_Height_Enrichment

Thank you


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-14 08:45
okadatsuneo

プロジェクト活動について、OSMデータの充実につながるので賛成します。
Wikiを確認しました。タグ付けは良いと思います。
1点質問ですが、作業単位はどうなりますか？Project Plateauのタイルあるいはそれより小さな面積のエリアごとに実施するのか、MapRouletteやRapidのように個々の建物単位での作業が可能なのか？です。

====

I agree with this project activities as they will contribute to enriching the OSM data.
I checked the Wiki. Tagging seems fine.
I have one question: What will the work unit be? Will it be done on a tile-by-tile basis in Project Plateau or smaller area, or is it possible to work on individual buildings like in MapRoulette or Rapid?


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-14 12:09
hiroshimiura.

Talk-jaへの投稿がフィルターにひっかかっていましたので、承認しました。配信されたはずです。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-14 20:53
k.sakanoshita

@Can (チャソ) - TomTom 日本語で申し訳ありませんが、「Full Osaka import following community agreement」は明確に反対します。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-14 20:55
k.sakanoshita

まず、大阪をインポートしたい理由がわかりません。次に大阪は他の地域よりマッピングが進んでおり、PLATEAUより精度が高い場所や、PLATEAUと異なる書き方をしている箇所（特にマイクロマッピング）が大量にあります。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-14 20:57
k.sakanoshita

その上で、TomTom側の理由でどうしてもインポートしたいと言うなら、「日本のコミュニティからの意見は無視して進める」とWikiに明記してください。
そして、あなたがインポートした後、何年か掛けて、また少しずつ書き直していきます。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-14 20:59
k.sakanoshita

ちなみに「大阪」の定義は「大阪市」か「大阪府」かも分かりません。大阪府であれば、マッピングの弱い市町村もありますが、それでも東京に比べても急速に改善が進んでいる箇所です。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-14 21:01
k.sakanoshita

また、日本コミュニティが有志で実行しているPLATEAUデータを使ったマッピングとの競合しているのに、その活動との住み分けについてWikiには何も記載されていません。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-14 21:10
k.sakanoshita

すみません。いくつか読み飛ばししていました。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-14 21:11
k.sakanoshita

上記のコメントは残しておきますが、私の勘違いがあるので、読み直した上で再度コメントさせてください。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-14 21:14
k.sakanoshita

まず、私の大きな読み落としとして「建物の高さタグ」の件でした。この点だけであれば、むしろ賛成です。ご提案感謝します。

上に書いた私のコメントは正直削除したい気持ちですが、逆に何か勘違いされると良くないので、あえて残しておきます。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-14 21:22
k.sakanoshita

ただ、以下の点についてはWikiに明記していただきたく思います。

・大阪府と大阪市のどちらか？（範囲の明記）
・フットプリントが不足しているエリアについての対応はどうするか？
　→例えば、イベントを開いてフットプリントを充実させる
　→例えば、地域を決めた上でPLATEAUからインポートする
・スケジュールの共有とディスカッションの方法

スケジュールについては、対象範囲とフットプリントの充実度に合わせて変化すると思います。

また、必要であれば大阪でイベントを開催するなどで協力することも可能です。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-15 15:28
ashashash5025

Feedbackをいただき、誠にありがとうございます。日本語でのコメント内容について、私の方からもフォローをするようにいたします🙇


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-18 22:34
sbaidoun

Hello everyone,

My name is Salim, and I am writing on behalf of my colleague Can, who is on vacation for two weeks. I am taking over the follow-up on the PLATEAU building height enrichment for Osaka while he is away.
First of all, thank you very much for the careful and constructive feedback you have shared with us so far. We have read every comment and taken them all on board.

**Wiki page updated**
Based on your feedback, I have updated the Wiki page with the following:
- Scope is clearly **Osaka City** (not Osaka Prefecture).
- The first test will cover **20 buildings only**, to validate the end-to-end process at small scale before doing anything wider.
- The Wiki now shows the test scope visually: a map with the 20 building footprints, plus a sortable table listing the centroid coordinates of each building. Every row links to the OSM object so anyone can review the buildings directly.

**You can see the Test Scope section here:**
https://wiki.openstreetmap.org/wiki/Organised_Editing/Activities/TomTom/Global_-_Building_Height_Imports/Japan_-_PLATEAU_Building_Height_Enrichment#Test_Scope


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-18 22:34
sbaidoun

**What we will and will not change**
To keep this transparent and to minimise any risk to the data:

- We will only add height=* where it is missing from the OSM building.
- We will not modify any existing tag, including any height value that is already present.
- We will not create any new buildings.
- We will not modify any building geometry.
- If any issue is found, we will revert the changeset.

**Next steps**

- Before we run the test, we would very much appreciate your feedback on the 20-building test scope. Please take a look at the Wiki section (https://wiki.openstreetmap.org/wiki/Organised_Editing/Activities/TomTom/Global_-_Building_Height_Imports/Japan_-_PLATEAU_Building_Height_Enrichment#Test_Scope) above and let us know if anything looks wrong.
- Once the 20-building test is reviewed and accepted, we will scale gradually within Osaka City only.
- We will share the result of the small test with the community before moving to anything wider.

**On the offer to help with community events**
Special thanks to K.Sakanoshita for the kind offer to help organise events in Osaka to support footprint mapping. We really appreciate it. My colleagues will be in touch with you to discuss how we can best work on this together.
Thank you again for taking the time to guide us. We are committed to doing this carefully and openly, and your input is making the process stronger.

Best regards,
Salim


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-18 22:35
sbaidoun

お世話になっております。
TomTomのSalim（サリム）と申します。
このたび、2週間の休暇中の同僚Canに代わり、大阪のPLATEAU建物高さ情報追加プロジェクトのフォローアップを担当させていただきます。
まずはじめに、これまで丁寧かつ建設的なフィードバックをお寄せいただき、誠にありがとうございます。皆様からのコメントは一つひとつ拝読し、真摯に受け止めております。
Wikiページの更新について
皆様からのご指摘を反映し、Wikiページを以下のとおり更新いたしました。

対象範囲は 大阪市 であることを明記いたしました（大阪府ではありません）。
最初のテストは 20棟のみ を対象とし、より広い範囲に進む前に、エンドツーエンドのプロセスを小規模に検証することを目的としています。
Wikiには、テスト対象を視覚的にご確認いただけるよう、20棟のフットプリントを示す地図と、各建物のセントロイド座標を一覧化したソート可能な表を掲載いたしました。各行はOSMオブジェクトへのリンク付きとなっており、どなたでも建物を直接ご確認いただけます。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-18 22:35
sbaidoun

テストスコープのセクションはこちらをご覧ください：
https://wiki.openstreetmap.org/wiki/Organised_Editing/Activities/TomTom/Global_-_Building_Height_Imports/Japan_-_PLATEAU_Building_Height_Enrichment#Test_Scope
変更する内容と変更しない内容
透明性を確保し、データへのリスクを最小限に抑えるため、以下のとおり対応いたします。

height=* タグがまだ付与されていない建物にのみ、高さ情報を追加します。
既存のタグ（既に登録されている height の値を含む）は一切変更いたしません。
新たな建物の作成は行いません。
建物のジオメトリの変更は行いません。
万一問題が発見された場合、ChangesetをRevertいたします。

今後の進め方

テストを実行する前に、20棟のテストスコープについて皆様のご意見をいただけますと幸いです。上記のWikiセクション（https://wiki.openstreetmap.org/wiki/Organised_Editing/Activities/TomTom/Global_-_Building_Height_Imports/Japan_-_PLATEAU_Building_Height_Enrichment#Test_Scope）をご覧いただき、お気づきの点がございましたらお知らせください。
20棟のテストをご確認いただき、ご了承いただけましたら、大阪市内に限定して 段階的に範囲を広げてまいります。
小規模テストの結果は、それ以降の作業に進む前に、必ずコミュニティと共有いたします。


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-18 22:35
sbaidoun

コミュニティイベントへのご協力のお申し出について
K.Sakanoshita様より、フットプリント整備を支援するための大阪でのイベント開催にご協力いただけるとのお申し出をいただき、誠にありがとうございます。心より感謝申し上げます。今後の進め方について、社内の担当者より別途ご連絡させていただきます。
ご多忙のところ、丁寧にご指導いただき、重ねて御礼申し上げます。
本プロジェクトを慎重かつオープンに進めてまいります。皆様からのご意見によって、プロセスがより良いものになっております。
引き続き、どうぞよろしくお願いいたします。
Salim（サリム）


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-21 04:52
sbaidoun

皆様
 
お世話になっております。Salim（サリム）です。
 
簡単な訂正と計画変更のご報告です。
 
本日先ほど、14棟の建物のインポートを実施いたしました。2日前にご案内した20棟とは別のセットでございます。
 
本日（2026年5月20日）実施した内容：
 
* Changeset: https://www.openstreetmap.org/changeset/182920833
* 14棟にPLATEAUのデータから高さ情報を付与
* 各建物に source:height = MLIT_PLATEAU タグを追加（出典の明示）
* 既存タグの上書きなし
* ジオメトリの変更なし
* 新規建物の作成なし
* アカウント：TTmechanicalupdates
* エリア：大阪市住之江区 南港南
 
Wikiページもあわせて更新済みでございます：
https://wiki.openstreetmap.org/wiki/Organised_Editing/Activities/TomTom/Global_-_Building_Height_Imports/Japan_-_PLATEAU_Building_Height_Enrichment
 
現状をご確認いただけるかと存じます。お気づきの点やご意見がございましたら、ぜひお寄せいただけますと幸いです。計画に小さな変更が生じましたことをお詫び申し上げます。問題なく機能していることを確認したうえで次のステップに進むため、あえて非常に小規模なところから開始しております。
 
ご確認・ご対応のほど、誠にありがとうございます。
 
引き続きどうぞよろしくお願いいたします。
 
Salim（サリム）

Hello everyone,
 
A short correction and change of plans.
 
Earlier today we had the opportunity to import 14 buildings. This is a different set from the 20 buildings I communicated two days ago.
 
What was done today (20 May 2026):
 
* Changeset: https://www.openstreetmap.org/changeset/182920833
* 14 buildings tagged with height values from PLATEAU
* source:height = MLIT_PLATEAU added to each building for provenance
* No existing tag was overwritten
* No geometry was modified
* No new building was created
* Account: TTmechanicalupdates
* Area: Nanko-Minami, Suminoe-ku, Osaka City
 
I have already updated the Wiki page accordingly:
https://wiki.openstreetmap.org/wiki/Organised_Editing/Activities/TomTom/Global_-_Building_Height_Imports/Japan_-_PLATEAU_Building_Height_Enrichment
 
I hope that gives a clear picture of where we stand, and we would really value any feedback you may have. Please excuse this small change in the plan. We are intentionally starting at very small scale so that we can confirm everything is working cleanly before going further.
 
Thank you for your patience.
 
Best regards,
Salim


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-23 00:02
sbaidoun

皆様

簡単なアップデートです：

昨日（2026年5月21日）、本プロジェクトの第2回テストを完了いたしました。先にご案内した20棟のスコープを、4件のChangesetに分けてインポートいたしました。Test 1と同じルール（heightタグが未付与の建物にのみ追加、各建物に source:height = MLIT_PLATEAU を付与、既存タグの上書きなし、ジオメトリの変更なし、新規建物の作成なし）に従って実施しております。

実施したChangeset：
- https://www.openstreetmap.org/changeset/182980920
- https://www.openstreetmap.org/changeset/182980922
- https://www.openstreetmap.org/changeset/182980925
- https://www.openstreetmap.org/changeset/182980928

合計：20棟（各Changesetに5棟ずつ）。高さの範囲：3.4 m〜49.7 m、平均19.5 m。4件すべてアカウント TTmechanicalupdates で、同じエディタ（osm-bulk-upload/upload.py v.2）を使用しております。

Wikiページを更新し、対象となった20棟すべての一覧を掲載いたしました。各建物はOSMオブジェクトへのリンク付きで、タグ付けを直接ご確認いただけます：
https://wiki.openstreetmap.org/wiki/Organised_Editing/Activities/TomTom/Global_-_Building_Height_Imports/Japan_-_PLATEAU_Building_Height_Enrichment

お時間のある際にご確認いただき、お気づきの点がございましたらお知らせください。問題が見つかった場合はChangesetをrevertいたします。

次のステップとして、大阪市全域での建物高さ情報追加作業を本格的に展開するための全体計画を準備しております。より大きな規模の作業に着手する前に、皆様に内容をご確認いただきフィードバックを頂戴できるよう、近日中に共有させていただきます。

ご確認・ご対応のほど、誠にありがとうございます。

引き続きどうぞよろしくお願いいたします。

Salim（サリム）


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-23 00:02
sbaidoun

Hi everyone,

A quick update 

Yesterday (21 May 2026) we completed the second test of this project. The 20-building scope I announced earlier was imported across four changesets. Same rules as Test 1: height added only where missing, source:height = MLIT_PLATEAU on each modified building, no existing tags overwritten, no geometry changes, no new buildings created.

Changesets:
- https://www.openstreetmap.org/changeset/182980920
- https://www.openstreetmap.org/changeset/182980922
- https://www.openstreetmap.org/changeset/182980925
- https://www.openstreetmap.org/changeset/182980928

Totals: 20 buildings (5 per changeset). Height range 3.4 m to 49.7 m, average 19.5 m. All four done by account TTmechanicalupdates using the same editor (osm-bulk-upload/upload.py v.2).

The Wiki page has been updated with the full list of all 20 buildings, each one linking to OSM so you can verify the tagging directly:
https://wiki.openstreetmap.org/wiki/Organised_Editing/Activities/TomTom/Global_-_Building_Height_Imports/Japan_-_PLATEAU_Building_Height_Enrichment

Please take a look when you have a moment. If anything looks off, let us know and we will revert.

Next: we are putting together a full plan to scale building height enrichment across the whole of Osaka City. We will share it with the community very shortly so you can review the approach and give us your feedback before any larger-scale work begins.

Thank you again for your patience and continued feedback. Please note that I used auto-translate for Japanese, so I would request you to excuse me if there are any mistakes.

Best,
Salim


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-23 12:47
k.sakanoshita

テストお疲れ様でした。テストの段階では既存のOSMとPLATEAUの建物は一対一の関係を保てたかと思います。
今後、範囲を増やすに当たって、事前テストとして合致率を出すことは可能でしょうか？
大阪市の各区ごとの建物が
OSMとPLATEAUで合致していない所が多い場合、何か対応できないか検討したいと考えます（別にPLATEAUの方が最新とは限らないので、出来ることは限定的ではあると想いますが、そういった地域を把握できると、今後のマッピング計画にも入れやすくなります）


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-26 23:46
sbaidoun

ご丁寧なご返信、ありがとうございます。テストにご関心をお寄せいただき、感謝いたします。

合致率の算出方法とパラメータにつきましては、Wiki ページの以下のセクションに記載しております:

https://wiki.openstreetmap.org/wiki/Organised_Editing/Activities/TomTom/Global_-_Building_Height_Imports/Japan_-_PLATEAU_Building_Height_Enrichment#Conflation_and_Acceptance

PLATEAU の更新タイミングに関するご指摘、誠にありがとうございます。これは重要なポイントとして、社内のチームでも共有させていただき、皆で認識しておきたいと思います。

その上で、もし大阪市内で特に注意すべき点や、確認しておいた方が良い事例などがございましたら、ご教示いただけますと幸いです。皆様の現地でのご経験に基づくご助言は、大変参考になります。

お時間をいただき、誠にありがとうございました。

引き続き、どうぞよろしくお願いいたします。

Salim (TomTom)

 - - - - - - - - - - - - - - - - - - - - - - - - 
Thank you for your thoughtful reply, and for taking an interest in the test.

The methodology and parameters we use for matching are documented on the wiki page in the following section:

https://wiki.openstreetmap.org/wiki/Organised_Editing/Activities/TomTom/Global_-_Building_Height_Imports/Japan_-_PLATEAU_Building_Height_Enrichment#Conflation_and_Acceptance

Thank you very much for the point about PLATEAU update timing. This is valuable input that I will share with my team internally so we all keep it in mind as we proceed.

With that in mind, if there are any particular points we should pay attention to in Osaka, or specific examples you think we should check, we would be very grateful for your guidance. Your advice based on local experience would be very helpful to us.

Thank you very much for your time.

Best regards,
Salim (TomTom)


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-26 23:50
k.sakanoshita

すみません。意図が伝わっていないようで申し訳ありません。
Wikiには実際の合致率は書いていないかと思います。
大阪市の各区ごとに合致率が分かれば、インポート前にフットプリントの見直し（PLATEAUが正しいのであれは、ですが）が出来ること思いますが、それは可能でしょうか？


# TomTom Automated Edit Pilot: Building Height Enrichment from PLATEAU Data (Osaka)

## 2026-05-26 23:53
k.sakanoshita

まぁ、インポート後にbuildingからheightが無い建物を抽出すれば、外れ率を算出することも出来ますが、インポート前に出来ればありがたく。

また、質問ですが、このインポートは何時までに実施する計画でしょうか。



---

# 組織的編集：鹿児島県_観光スポット

## 2026-05-14 20:26
qing_06282

だいぶ間が空いてしまいましたが、作業中止となってしまったことを残念に思っています。

リストにある施設名、タグ案、大まかな位置情報は、今後のマッピングにおいても貴重な情報だと思うため、もし元データの出典やライセンス上問題なければ、参考情報として利用させていただけないでしょうか。

なお、訪れたことのない・知らなかった箇所については、航空写真等で確認できる範囲で、個別に確認しながら追加したいと考えています。



---

# 遊具のある公園マップ

## 2026-05-16 10:13
k.sakanoshita

そろそろ「口コミ」機能を充実できないかなとフォームの見直しを行おうと思いますー。
こんな入力項目が欲しいなどありましたら教えてくださいー。



---

# 2026年05月定例会

## 2026-05-02 20:03
wish.f

先日 @K.Sakanoshita さんと話していたのですが、
毎週の #MappyJourJapan の時間で、OSMをより多くの場面で使われる地図に育てるため、
時々、集中編集テーマを設けることができないかと感じています。
テーマはみなさんからの提案で、地域にこだわらず進めることができればいいなと思います。
(例：サーベイ不要でも参加できる品質向上型の
建物が全く描かれていない地域での集中トレース、道路や森林等の修正など）
ご意見をいただけたらと思います。
(時間があれば今夜の定例会でお話しできたらと思います)

わざわざ見に行くの面倒ですし…


# 2026年05月定例会

## 2026-05-02 20:04
k.sakanoshita

・「編集合戦」の進捗報告
　→すみません。進捗なしです。GW中になんとかしたいと思います。


# 2026年05月定例会

## 2026-05-02 20:06
btm.smellman

OSC 2026 Sendaiに出展します。


# 2026年05月定例会

## 2026-05-02 20:08
k.sakanoshita

・イベント情報共有・出展を考える
　→地図カフェは進捗なし
　→OSC2026仙台出展(6/6)。OSM Fukushimaが中心で出したい。
　  OSC仙台自体かなり久しぶり。smellmanさん、Ikiyaさん参加予定
　→OSC名古屋は5/23。OSMJPブースはなし。
　→OSC北海道（6/27）締め切り5/15。ブースとセミナー予定 
　→OSC島根（7/11）はOSGeoで出展を計画中
　→OSC京都（8/1）smellman、nmaruichi、kussun、坂ノ下が申し込み担当
　→テックシーカーハッカソン2026
　   https://techseeker.jp/post-2077/
　→OSC広島は出展したい（nmaruichi）
　→毎月第1水曜日20時から「マッピングパーティお酒の会」
　  https://www.facebook.com/events/1449977673061417
　→State of the Map ASIA
　  GEO展の翌日（5月から）まで古橋先生は忙しいとのこと
　→State of the Map Taiwan（FJ三浦さんは参加予定）
　  https://diff.wikimedia.org/2026/04/29/wikidata-community-summit-2026-coscup-call-for-proposals/
　→シビックテックフォーラム2026（5/23 大阪）
　  https://civictechforum.jp/
　→KOF2026は11/13-14。


# 2026年05月定例会

## 2026-05-02 20:36
k.sakanoshita

・OSM.JP Webサイトの今後を考える
　→今のサイトはセキュリティ上非常に問題がある
　  過去データの移行は行う予定（データ抽出済み）
　  一旦新サイトへの移行を進めて頂く
　  CloudFlareのEmDashも検討
　  みんなで欲しいサービスを考えていこう


# 2026年05月定例会

## 2026-05-02 20:38
btm.smellman

https://blog.cloudflare.com/ja-jp/emdash-wordpress/


# 2026年05月定例会

## 2026-05-02 20:53
k.sakanoshita

・欲しいアプリやサービスを考える
　→タグ付け案をプリセットにして提供出来たらいいな
　→maripoさんのプラグインでプリセットを作れる
　→GitHubで共有＆開発していけたらいいな
　→ヴェスプッチなどプリセットの互換性があればいいな
　→音声案内のアプリをChatGPTで一瞬で作れた
　→Androidタブレットの電子ペーバにCoMapを表示させると紙っぽい印象で受けが良かった
　  今後もこういったネタを探していきたい（smellman）


# 2026年05月定例会

## 2026-05-02 20:56
btm.smellman

https://every-door.app/plugins/


# 2026年05月定例会

## 2026-05-02 20:56
k.sakanoshita

・やりたいイベントの企画を考える
　→KOF。SotMJPは春にマッピングパーティと重ねては？
　→酒蔵などのマッピングイベントとかも楽しいのでは？
　→開催地にちなんだイベントがいいな


# 2026年05月定例会

## 2026-05-02 21:11
ryoa8139

違う人に乗っ取られてる！


# 2026年05月定例会

## 2026-05-02 21:12
k.sakanoshita

あー。ごめん。戻ってきてくださいー。


# 2026年05月定例会

## 2026-05-02 21:12
ryoa8139

私がしゃべっていないのに別の音声が聞こえてきた


# 2026年05月定例会

## 2026-05-02 21:13
ryoa8139

承知しました


# 2026年05月定例会

## 2026-05-02 21:13
ryoa8139

マイク設定がうまくいかないので


# 2026年05月定例会

## 2026-05-02 21:13
ryoa8139

チャットします


# 2026年05月定例会

## 2026-05-02 21:14
ryoa8139

内容が難しく内容についていくのに精一杯でした


# 2026年05月定例会

## 2026-05-02 21:15
wish.f

私もわからないこといっぱいです......


# 2026年05月定例会

## 2026-05-02 21:17
k.sakanoshita

+Nyanpireさん


# 2026年05月定例会

## 2026-05-02 21:21
btm.smellman

https://www.kagolug.org/ ちなみに友達が鹿児島で勉強会やってます。


# 2026年05月定例会

## 2026-05-03 13:21
nmaruichi0129

車椅子利用向けのタグ付けで、縁石の書き方の件です。

まず画像を参照してください。
(ウェイの)横断歩道(`highway=footway` & `footway=crossing`)と道に沿った歩道(`highway=footway` & `footway=sidewalk`)の境界となる縁石部分の交点ノードへのタグ付けを吹き出しで説明しました。
`kerb=*` の値部分が車椅子での利用の可・負荷に相当するので、実際には斜字体(イタリック)の `wheelchair=*` のタグは、設定していません。
この交差点にはありませんが、横断歩道との境界の交点ノードには、完全な平坦 `kerb=flush` もありますが、こちらは視覚障害の方が横断歩道との境がわからない可能性が高く危険かもしれません。

境界の交点ノードのシンボルは、Wikiページのアイコンを貼り付けました。
マップのスタイルは、merkaartor で表示した個人的なマップスタイル設定です。
道路を細めに表示するマイクロマッピングに適したスタイルで、歩道でも横断歩道や点字ブロック付き歩道を別のラインスタイルで表現するようにしています。

詳細は、`JA:Key:kerb` ( https://wiki.openstreetmap.org/wiki/JA:Key:kerb ) に書かれています。(英語版や`JA:歩道/SidewalkMapping`( https://wiki.openstreetmap.org/wiki/JA:%E6%AD%A9%E9%81%93/SidewalkMapping )も見た方が良いかも……)

この図の場所は、ウェイの縁石(`barrier=kerb`)やエリアの歩道(`area:highway=footway`)も(マルチポリゴンを多用して)作成しているので同じように編集するのは難しい認識です。
お薦めはしません。

あとこの交差点で縁石あり(`kerb=yes` )がありますが、横断歩道の幅(約4m)のうち2/3位が(推測で15cm)高い縁石で1/3位が低い縁石になっていたので「よくわからない」と思って設定しましたが、あまり適切出ない様なので後で`kerb=low`に直そうと思います。

↓下のリンクが、その縁石が見える mapillary 画像。
https://www.mapillary.com/app/?lat=34.43064899999999&lng=132.29665699989005&z=18.603449320747238&pKey=218023277022208&focus=photo&x=0.7598914169491195&y=0.4234875164629945&zoom=0.192375


# 2026年05月定例会

## 2026-05-03 14:45
nmaruichi0129

張り付けたはずの画像が落ちていたので、添付します。


# 2026年05月定例会

## 2026-05-12 07:31
nmaruichi0129

「週刊OSM 824」の下記の記事が気になりました。
> 以下のタグ提案に対するコメントを募集中です。
> 
>     `name:<language>-Latn`：BCP47に従って、各国の文字をラテン文字に音訳します。int_nameとの使い分けも明確にします。
↓記事へのリンク
https://weeklyosm.eu/ja/archives/18565#wn824_%E3%83%9E%E3%83%83%E3%83%94%E3%83%B3%E3%82%B0

記事のキー名のところが、「タグの提案ページへのリンクになっていて下記ページへのリンクです。
https://wiki.openstreetmap.org/wiki/Proposal:*:language-Latn_for_name_keys_around_the_world
「int_name」に関する提案ではなく、違いのみに触れている様です。



---

# 2026年06月定例会

## 2026-05-12 21:16
k.sakanoshita

2026/06/06 20時開始。時間になれば以下のボイスチャンネルへ接続してください。
https://discord.com/events/1280891177020686347/1459529305447989444/1512773045452800000


# 2026年06月定例会

## 2026-05-12 21:18
k.sakanoshita

議題はこんな感じかな
・「編集合戦」の進捗報告
・イベント情報共有・出展を考える
　→OSCなどのイベント情報の共有
　→出展したいイベントの検討
・OSM.JP Webサイトの今後を考える
　→特に誰が運用を行うか（投稿や管理）
・欲しいアプリやサービスを考える
　→誰が作るとかは一旦考えない
・やりたいイベントの企画を考える
　→誰がやるとかは一旦考えない


# 2026年06月定例会

## 2026-05-31 00:48
k.sakanoshita

@hayashi さんの無限の刃さんとの件。遅くなって申し訳ありませんが、こんな内容を考えました。如何でしょうか。 @everyone



---


---


---


---


---


---

# 52_sotmjp2026_asia

## 2026-05-07 22:45
hiroshimiura.

8月8，9日に台北市で今年もCOSCUP2026ありますが、参加される方はありますか？
講演提案が5月9日までなのですが、SotM Asia 2026やFOSS4G Hiroshimaの宣伝を講演したらどうかとおもいます。


# 52_sotmjp2026_asia

## 2026-05-07 22:46
hiroshimiura.

トラックとしては、OSPN.JP ジャパントラックか、Wikidata＆OSMトラックかと。


# 52_sotmjp2026_asia

## 2026-05-07 23:08
hiroshimiura.

https://discordapp.com/channels/1280891177020686347/1280891177608024169/1501948680691912715


# 52_sotmjp2026_asia

## 2026-05-14 09:54
hokkosha

SOTM Asiaの日程等は9/5〜9/6、大阪で決定でしょうか？
できるだけ参加したいと思ってますが、仕事その他のスケジュール調整のため、現時点の確定事項を確認したいです。


# 52_sotmjp2026_asia

## 2026-05-18 23:03
k.sakanoshita

9/6-7みたいですね。
https://wiki.openstreetmap.org/wiki/State_of_the_Map_Asia_2026/Call_for_Venues/Japan


# 52_sotmjp2026_asia

## 2026-05-19 07:31
hokkosha

会場とされている中崎町ホール、収容人数140名とありますがSOTMには手狭に思えるのですが…🤔


# 52_sotmjp2026_asia

## 2026-05-20 13:07
alt9800

実際昨年のグローバルとか見た感じ140人がどれくらいの多さかは少し判断に迷うところもあります。
直前のFOSS4G からどれくらい流れてくるかっていうのも見積もりしがたかったりする要因ですよねきっと。


# 52_sotmjp2026_asia

## 2026-05-21 09:13
mapconcierge

SotM Asia 2026 Osaka は、2026年5月19日に開催された FOSS4G 2026 Hiroshima 運営会議において、FOSS4G 2026 Hiroshima の公式 Community Event として審議・採択されました。これにより、FOSS4G Hiroshima と SotM Asia Osaka の連携は単なる日程上の近接ではなく、公式な関連イベントとして位置づけられます。

次のステップとして、OpenStreetMap Japan コミュニティと OSMFJ に最終案を提示して最終的な了承をいただき、ようやく準備活動を公式にスタートしたいと考えております！ みなさまどうぞよろしくお願いいたします。


# 52_sotmjp2026_asia

## 2026-05-21 09:14
mapconcierge

FOSS4G Hiroshima との日程かぶりを考え、メインのカンファレンスは9/7 平日月曜日となりますので、それほど大人数にはならないと予想しております。


# 52_sotmjp2026_asia

## 2026-05-21 09:15
mapconcierge

大まかな見積もりですが、FOSS4G Hiroshima からは約50名程度流れてくると予想しております。


# 52_sotmjp2026_asia

## 2026-05-21 09:17
mapconcierge

ありがとうございます。
最終的に、FOSS4G Hiroshima の Community Sprint と Excursion 日程に重ならない調整を行い、9/6-7 と修正いたしました。


# 52_sotmjp2026_asia

## 2026-05-21 11:10
mapconcierge

SotM Asia 海外勢の運営ボランティア募集をかけ、 #53_sotmjp2026_asia_en チャンネルに誘導開始いたしました。


# 52_sotmjp2026_asia

## 2026-05-26 17:24
mapconcierge

SotM Asia の準備で、その歴史をまとめてもらいました。


# 52_sotmjp2026_asia

## 2026-05-26 17:24
mapconcierge

英語版も現在作成中です。


# 52_sotmjp2026_asia

## 2026-05-26 17:25
mapconcierge

これで、開催概要案今日中に完成できそうです。


# 52_sotmjp2026_asia

## 2026-05-26 17:42
k.sakanoshita

肝心のOpenStreetMap Japanがありませんがー。


# 52_sotmjp2026_asia

## 2026-05-26 18:16
mapconcierge

確かに！！ 修正させます！！！


# 52_sotmjp2026_asia

## 2026-05-26 18:16
mapconcierge

説明したんだけど、欠けとる


# 52_sotmjp2026_asia

## 2026-05-26 18:50
mapconcierge

一旦、古橋が手を入れた簡易修正版こちらです。学生には修正依頼完了。このあと英語版も作ってもらいます。


# 52_sotmjp2026_asia

## 2026-05-27 12:38
mapconcierge

学生が再度修正したバージョン。



---

# 53_sotmjp2026_asia_en

## 2026-05-21 09:11
mapconcierge

## Relationship with FOSS4G 2026 Hiroshima

SotM Asia 2026 Osaka has been reviewed and officially accepted as a Community Event of FOSS4G 2026 Hiroshima at the FOSS4G 2026 Hiroshima organizing meeting held on 19 May 2026.

This official recognition creates a strong linkage between FOSS4G 2026 Hiroshima and SotM Asia 2026 Osaka, allowing international participants to join both events during a single trip to Japan. It also strengthens collaboration between the FOSS4G, OSGeo, OpenStreetMap, humanitarian mapping, and open geospatial communities in Asia.

The proposed schedule places SotM Asia 2026 Osaka immediately after FOSS4G 2026 Hiroshima, enabling a smooth transition from Hiroshima to Osaka and encouraging broader participation from regional and international communities.


# 53_sotmjp2026_asia_en

## 2026-05-21 09:32
mapconcierge

Welcome to SotM Asia 2026 Osaka volunteer team!!

--
# Call for Volunteers: SotM Asia 2026 Osaka

We are starting to organize the international volunteer team for **State of the Map Asia 2026 Osaka**, planned to be held in **Nakazakicho, Osaka, Japan**, immediately after **FOSS4G 2026 Hiroshima**.

SotM Asia 2026 Osaka has been officially accepted as a **Community Event of FOSS4G 2026 Hiroshima** at the organizing meeting held on **19 May 2026**.

We are now looking for volunteers from across Asia and beyond to help with program planning, speaker coordination, sponsorship, scholarships, communications, translation, workshops, mapping activities, online/hybrid support, and on-site operations.

Remote volunteers are very welcome.

If you are interested, please join our volunteer coordination channel:

https://discord.com/channels/1280891177020686347/1493460424056901764

Please introduce yourself with your name, country/region, OSM username, languages, areas where you would like to help, and whether you can support remotely, on-site, or both.

Let’s build SotM Asia 2026 Osaka together as an open, inclusive, and community-driven event!


# 53_sotmjp2026_asia_en

## 2026-05-21 19:01
supaplextw

Hello everyone, I am Dennis Raylin Chen from Taiwan, user name is Supaplex
I can help with doing program committee remotely or on-site if needed


# 53_sotmjp2026_asia_en

## 2026-05-21 19:44
mapconcierge

Welcome Dennis-san!!! 🙂


# 53_sotmjp2026_asia_en

## 2026-05-27 16:11
sshariar1991

Hello Everyone 
This is Sawan from Bangladesh


# 53_sotmjp2026_asia_en

## 2026-05-28 14:04
rajnandinikadam

Hello everyone! 
My name is Rajnandini Kadam from India. I am an M.Sc. Geoinformatics student passionate about GIS, mapping, and open-source geospatial communities. OSM Username: Rajnandini Kadam I would love to help with mapping support, community coordination, and event activities. 
I can support both remotely and on-site. Excited to contribute to SotM Asia 2026 Osaka and connect with the OSM Asia community!


# 53_sotmjp2026_asia_en

## 2026-05-28 18:56
riyankabanerjee.

Hello everyone. I am Riyanka Banerjee. I am from India. My osm username is Riyanka Banerjee. I am a Geoinformatics student. I would like to volunteer for the event by on-site visiting. I am excited to  contribute for the event.


# 53_sotmjp2026_asia_en

## 2026-05-28 18:59
aditimajhi

Hello everyone , I myself Aditi Majhi, I am from India,  Aditi Majhi, English, I am a student of MSc Geoinformatics from Symbiosis and I am a regular mapper in osm India I would like to volunteer for the event by on-site visiting and participating. I am excited to contribute to the event.


# 53_sotmjp2026_asia_en

## 2026-05-28 23:29
akash0076891

Hello everyone! My name is Akash Moghe from India. I am a M.Sc. Geology student passionate about GIS, mapping, and open-source communities. My OSM username is Akash Moghe. I would like to volunteer for the event by on-site visiting.  I’m excited to contribute and learn with everyone here.


# 53_sotmjp2026_asia_en

## 2026-05-29 13:51
khushijha1

Hello everyone! 
My name is Khushi from India. I am an M.Sc. Geology student passionate about GIS, mapping, Aerial imagery and related. my OSM Username: Khushijha I would love to help with mapping support, community coordination, and event activities on-site. Excited to contribute to SotM Asia 2026 Osaka and connect with the OSM Asia community!



---

# 01_アナウンスと告知

## 2026-05-01 22:55
k.sakanoshita

https://discord.gg/ckBuZWYq?event=1459529305447989444


# 01_アナウンスと告知

## 2026-05-01 22:55
k.sakanoshita

明日の Mappy Hourの前にOSM Japan定例会を開きます。


# 01_アナウンスと告知

## 2026-05-09 12:27
k.sakanoshita

さて、今夜21時から #10_マッピング活動  でMappy Hour Japanを開催します！
みんなで好きな場所の地図を描いて、成果発表するオンラインイベントです。
みなさんのお気軽なご参加（チャット）をお待ちしています！


# 01_アナウンスと告知

## 2026-05-09 12:28
k.sakanoshita

明日の開催です。若干名参加できるので、申し込みよろしくお願いします！


# 01_アナウンスと告知

## 2026-05-13 17:19
hokkosha

6月27日（土）に札幌市白石区の札幌市産業振興センターで開催されるOpen Source Conference 2026 Hokkaidoに、OpenStreetMap Japanとして参加します。
https://event.ospn.jp/osc2026-do/
ブース出展の他、大阪から坂ノ下さんに来ていただくので、セミナー出講いただく予定です。
翌日には札幌近郊でマッピングパーティー的な何かも準備中です。
ブースお手伝いでも短時間の冷やかしでも構いませんので、お近くの方はお立ち寄りいただければ幸いです。


# 01_アナウンスと告知

## 2026-05-14 15:39
k.sakanoshita

ありがとうー。早急に企画していかないとね


# 01_アナウンスと告知

## 2026-05-14 15:41
k.sakanoshita

5/31に三国の方たちとマッピングパーティーを開きます。
で、参加者にEveryDoorの操作支援や補助をして頂ける方を募集します！
ご協力できる方は、ご連絡くださいー。


# 01_アナウンスと告知

## 2026-05-16 20:12
k.sakanoshita

さて、今夜21時から #10_マッピング活動  でMappy Hour Japanを開催します！
みんなで好きな場所の地図を描いて、成果発表するオンラインイベントです。
みなさんのお気軽なご参加（チャット）をお待ちしています！


# 01_アナウンスと告知

## 2026-05-17 12:49
k.sakanoshita

5/23のCivicTechForm2026で「OpenStreetMap Japanブース」を出すことになりました！
どなたか、一緒にブース番をされませんか？ご連絡お待ちしています！
https://civictechforum.jp/


# 01_アナウンスと告知

## 2026-05-20 01:40
alt9800

おおお、楽しそう！行こうかな...！


# 01_アナウンスと告知

## 2026-05-28 10:28
k.sakanoshita

OSM Japan Didcordの管理者に @alt9800 さんを追加させて頂きました。
他にも管理者として運用に関わって頂ける方は、ご連絡頂けたら幸いです。


# 01_アナウンスと告知

## 2026-05-28 17:48
k.sakanoshita

@北光社/Hokkosha さんも管理者になって頂きました！


# 01_アナウンスと告知

## 2026-05-30 21:00
k.sakanoshita

さて、今夜21時から #10_マッピング活動  でMappy Hour Japanを開催します！
みんなで好きな場所の地図を描いて、成果発表するオンラインイベントです。
みなさんのお気軽なご参加（チャット）をお待ちしています！


# 01_アナウンスと告知

## 2026-05-31 00:49
k.sakanoshita

4月の定例会で検討した hayashiさんと無限の刃さんのアカウントロックについて、以下にまとめました。ご意見受け付けます。
https://discord.com/channels/1280891177020686347/1503732586613178580/1510308987394986174



---

# 03_雑談_なんでも

## 2026-05-01 01:24
kovoschiz

スパム・詐欺 @K.Sakanoshita 
https://discord.com/channels/1280891177020686347/1280913629813670005/1499197943155134505
https://discord.com/channels/1280891177020686347/1280910861082427412/1499198004471660545
https://discord.com/channels/1280891177020686347/1280914194602131537/1499198028479987892
香港の名を悪用することは嫌（アカウントがハックされるかも）


# 03_雑談_なんでも

## 2026-05-02 19:44
wish.f

先日 @K.Sakanoshita さんと話していたのですが、
毎週の #MappyJourJapan の時間で、OSMをより多くの場面で使われる地図に育てるため、
時々、集中編集テーマを設けることができないかと感じています。
テーマはみなさんからの提案で、地域にこだわらず進めることができればいいなと思います。
(例：サーベイ不要でも参加できる品質向上型の
建物が全く描かれていない地域での集中トレース、道路や森林等の修正など）
ご意見をいただけたらと思います。
(時間があれば今夜の定例会でお話しできたらと思います)


# 03_雑談_なんでも

## 2026-05-02 21:41
btm.smellman

https://wiki.openstreetmap.org/wiki/Japan#Communication_channels slackのinviteリンクがあったので、Discordに書き換えました。


# 03_雑談_なんでも

## 2026-05-02 22:37
k.sakanoshita

それは気が付かなかった！修正ありがとう！


# 03_雑談_なんでも

## 2026-05-05 18:18
gray27

今日もマピラリ撮って回ってたんですが、2.9m高さ制限（鉄道橋クリティカルヒット）よりも幅制限の情報がほしかった地点（通過を断念した


# 03_雑談_なんでも

## 2026-05-06 17:13
gray27

マピラリするときのスマホ固定機材が折れた……


# 03_雑談_なんでも

## 2026-05-07 05:44
hiroshimiura.

OSMを大学へ展開するというアイディアについて2025年2月ころに伺ったことがありますが、TomTomさんは、この方向性は継続していますか？


# 03_雑談_なんでも

## 2026-05-07 05:49
hiroshimiura.

4月12日にPCメイン環境の故障で、リカバー等で時間がかかってしまいました。
DiscordにPCから入れてなかった。ただいまです。


# 03_雑談_なんでも

## 2026-05-07 10:22
ashashash5025

こんにちは。はい、学生向け、今の所Youthmapper中心ですが、継続しております。


# 03_雑談_なんでも

## 2026-05-07 22:47
hiroshimiura.

8月8，9日に、台湾の台北市で、COSCUSP2026があります。
参加予定しているのですが、参加を考えている人はいますか？おすすめですよ。


# 03_雑談_なんでも

## 2026-05-07 22:49
hiroshimiura.

6月6日にOSC仙台が15年ぶりくらいにあります。
https://event.ospn.jp/osc2026-sendai/session/2311041
こちらも参加したいとおもいます。


# 03_雑談_なんでも

## 2026-05-07 23:07
hiroshimiura.

COSCUPのCfPの案を考えてみました。
Title:
Join the Open Map Community: FOSS4G, State of the Map Asia, and Beyond

Abstract:
OpenStreetMap (OSM) is one of the world's largest open-source collaborative projects, with a thriving community across Asia and beyond. The open mapping community has its own vibrant conference culture — and this summer, two major events are happening right after COSCUP, giving you the perfect opportunity to keep the open-source spirit going.

In this session, Hiroshi Miura — representative director of OpenStreetMap Foundation Japan and editor of WeeklyOSM — will share the story of how the open mapping community connects across borders, and invite you to be part of it.

We will introduce:
- FOSS4G Hiroshima (September 1-3, conference + September 4-5, sprint): the global conference for open-source geospatial technology, gathering thousands of GIS developers, researchers, and practitioners from around the world. This year it comes to Hiroshima, Japan. Stay for the sprint and hack together with the community!
- State of the Map Asia 2026 (September 6-7, Osaka): the regional OSM community gathering for Asia, where contributors from across the continent share their work and build connections.
- WeeklyOSM: a multilingual community newsletter keeping the global OSM community informed every week.

Come to COSCUP in Taipei in August, head to Hiroshima for FOSS4G, and wrap up in Osaka for SotM Asia — an open-source summer tour across the region!

No prior knowledge of maps or GIS is needed. If you have ever edited a map, used open geodata, or simply wondered how the map on your phone gets made, this session is for you.

Target audience: Beginner
Language: English
Duration: 30 minutes


# 03_雑談_なんでも

## 2026-05-08 02:05
alt9800

COSCUP、さかのしたさんやWikimediaの方々からいいよ〜ってお話し聞いたり、昨年のSotM Manilaで運営委員の方いらしててすごく行きたくなりました...!!
福岡市からはCOSCUP参加用のグラントとかあるらしいのでちょっと狙ってみようかな...


# 03_雑談_なんでも

## 2026-05-08 19:21
haya_koh

バス路線の`network`タグを関連付けるためのNSIを少し編集しました。
JRグループ各社と京都周辺の主要なバス会社の登録および`operator`タグの追加が主です。
https://github.com/osmlab/name-suggestion-index/pull/12179


# 03_雑談_なんでも

## 2026-05-08 19:24
haya_koh

加えて特に大きな私鉄傘下のバス会社に関連した`network`タグに関する問題提起もしておきました。


# 03_雑談_なんでも

## 2026-05-09 07:32
nguyenhoangan1235

ハノイの通り名について、日本語のカタカナ表記はどこで確認できますか？


# 03_雑談_なんでも

## 2026-05-09 13:07
haya_koh

外国語を日本語に転写する際の注意点は↓ここに載っていますが、これのベトナム語に特化したものやあるいは日本語でハノイ市内の道路名をまとめたサイトは見当たりませんね・・・
https://ja.wikipedia.org/wiki/外国語の日本語表記


# 03_雑談_なんでも

## 2026-05-09 13:39
nguyenhoangan1235

なるほど


# 03_雑談_なんでも

## 2026-05-09 14:16
nmaruichi0129

ハノイのとおりのなについて書かれている資料は、存在しないと予想します。
海外で使う場合は、カタカナを含む日本語表記は `name:ja` で書くのが良いかと思います。
日本向けの表記で「通りの名称」 JA:Japan tagging ( https://wiki.openstreetmap.org/wiki/JA:Japan_tagging#%E9%81%93%E8%B7%AF%E3%81%AE%E5%90%8D%E7%A7%B0 ) 
の末尾の3行の内、 `name:ja`, `name:ja-Hira` のキーを使用するのが、良い気がします。
OSMでのカタカナ表記専用のタグ付けをするキーは無い認識です。(読みを示すためのひらがな表記は、上記の`name:ja-Hira` です)
古い「かな表記」のタグ付けのためのキー `name:ja_kana` は、wiki では、「ひらがな表記」とかかれていたり、単なる「かな表記」書かれている場合もあるのですが、あらたにカタカナで表記するために利用すべきとは思えません。

上記の内容について再確認のために調べ直していたときに `Key:name:ko-Kana` ( https://wiki.openstreetmap.org/wiki/Key:name:ko-Kana )ってキーを見つけて驚きました。
`name:ko-Kana` を私が使う機会は、なさそうですけど……。


# 03_雑談_なんでも

## 2026-05-09 14:26
nguyenhoangan1235

こんにちは！貴重な情報ありがとうございます。参考にさせていただきます。

ベトナムには多くの日本企業が進出していると聞いているので、ハノイ旧市街（東京の銀座のような場所）の地図があれば大変助かります。

ベトナムの通りのカタカナ表記は、こちらのウェブサイト https://vietnam-sketch.com を利用しています。


# 03_雑談_なんでも

## 2026-05-09 14:31
nguyenhoangan1235

どうやら、ベトナムに関する日本の表記慣習としては、カタカナ表記の後に英語表記を併記する（以下のような形式で）のが一般的のようです。
https://vietnam-sketch.com/20200819117835/


私もこれと同じように記述すべきでしょうか？
name:ja=ファンディンフン（Phan Dinh Phung）通り

それとも、むしろ以下のような形式で記述すべきでしょうか？
name:ja=ファンディンフン（Phan Dinh Phung）通り
name:ja_kana=ファンディンフン通り

あるいは、伝統的な宛名形式で：
name:ja=ファンディンフン通り


# 03_雑談_なんでも

## 2026-05-09 14:34
nguyenhoangan1235

あ、読んでいなくてすみません。それなら、こうなりますね：

name:ja=ファンディンフン通り
name:en=Phan Dinh Phung Street
name:vi=Đường Phan Đình Phùng
name=Đường Phan Đình Phùng


# 03_雑談_なんでも

## 2026-05-09 14:38
nguyenhoangan1235

そうすれば、ソフトウェアを使って英単語を検索できるようになります。これは、Yahoo!地図（日本版）でも同様の慣例となっているようです。


# 03_雑談_なんでも

## 2026-05-09 15:38
nmaruichi0129

ベトナム語に限らず外国語全般を苦手としているので、下記ページを該当個所を機械翻訳しながら見てみました。(母国語の日本語も得意は言えない……)
https://wiki.openstreetmap.org/wiki/Vi:Vietnam_Mapping_Guide#%C4%90%C6%B0%E1%BB%9Dng_s%C3%A1_v%C3%A0_%C4%91%C6%B0%E1%BB%9Dng_m%C3%B2n
上記ページには、括弧での表記は、書かれていないので下記が良いように思えます。
> name:ja=ファンディンフン通り
> name:en=Phan Dinh Phung Street
> name:vi=Đường Phan Đình Phùng
> name=Đường Phan Đình Phùng

overpass turbo ( https://wiki.openstreetmap.org/wiki/JA:Overpass_turbo ) で、見てみると実際にタグ付けされた道路の日本語表記検索かけてみた限りでも上記に近いのかなと思います。(画像参照)


# 03_雑談_なんでも

## 2026-05-09 15:44
nguyenhoangan1235

ただ、ベトナムに滞在する日本人の圧倒的多数が、名前を「ファンディンフン（Phan Dinh Phung）通り」のような形式で表記しているのを目にしました。その理由は、実用性を重視する側面と、カタカナ表記の持つ「曖昧さ」という側面が組み合わさった結果ではないかと私は考えています。


# 03_雑談_なんでも

## 2026-05-09 15:44
nguyenhoangan1235

これにはずいぶん戸惑った。どちらの道を選ぶべきなのだろうか？


# 03_雑談_なんでも

## 2026-05-09 17:58
nmaruichi0129

かなり前の日本での OpenStreetMap の通り(道路)の `name` キーのタグ付けでの名称表記では、「日本語名称(英語名称)」形式が一般的でした。
世界的には基本的に`name` キーの値は、現地国の表記だったので、英語名称の併記はされなくなりました。 (まだ併記されたまま残っているものはある) 

OpenStreetMap の名前としては、地図の画面上の表示を理由に「地図を描く」(入力する)ことは正しくないので作図する際の `name:ja` キーのタグ付けとしても「日本語名称(英語名称)」の形式は良くないと思います。

現地で日本人が見て場所を確認するには、「ファンディンフン（Phan Dinh Phung）通り」のような形式である「日本語名称(英語名称)」が良いのは事実でしょうね。
地図表示のレンダラー(アプリやサイト)が、表示言語及び形式をカスタマイズ出来るのが最も適切な回答となるかと思いますが、そういう表示が可能なサイトやアプリがあるかは把握していません。

また地図表示のレンダラー(アプリやサイト)が、表示言語及び形式をカスタマイズ出来るとしても、「ファンディンフン(Phan Dinh Phung)通り」だと
  日本語名称( `name:ja` ):  "ファンディンフン通り"
  英語名称:( `name:en` )  "Phan Dinh Phung Street"
から、「日本語名称(英語名称)」形式だと「ファンディンフン通り(Phan Dinh Phung Street)」となるので理想とされる結果とも言えないかと思います。
わかりやすい地図というのは、難しいところですね。


# 03_雑談_なんでも

## 2026-05-09 20:09
gray27

https://vxtwitter.com/gray_cat27/status/2053020713624485963


# 03_雑談_なんでも

## 2026-05-09 20:16
wish.f

とても興味深いですねー。
有料記事ですがnoteも書かれているみたいなので、読んでみようかな。


# 03_雑談_なんでも

## 2026-05-09 20:18
gray27

国分寺の西南西は主要道1本より先は住宅地だったり谷だったりなので、ほんとそうだなぁと体感土地勘と重ねてみたり。


# 03_雑談_なんでも

## 2026-05-09 20:18
gray27

中野はサンプラザ（跡）に寄りすぎ。


# 03_雑談_なんでも

## 2026-05-09 22:28
kk.wcjp

デフォルトの表示だと、「路傍の神仏」は地図上に表示されないんでしょうか？
https://discord.com/channels/1280891177020686347/1280905549227102210/1502658216872382474 で設定した地蔵堂が、地図上に表示されませんでした。


# 03_雑談_なんでも

## 2026-05-09 23:08
okadatsuneo

表示されますよ。ブラウザの読み込みができてないだけでしょう。Windowsなら、Shift+F5でブラウザをリフレッシュしてみたら、表示されるかと思います。(あるいは数日待つ。)


# 03_雑談_なんでも

## 2026-05-10 22:46
westantenna

cartoのフォントが変わったのでしょうか？
今まで日本国内の地名は日本語のフォント、日本の漢字の字体で表示されていましたが、中国語で一般的な漢字の字体で表示されるようになってしまったようです。
左がブラウザーのキャッシュで表示させたもの、右が再読み込み後に表示させたもの


# 03_雑談_なんでも

## 2026-05-10 22:48
westantenna

瀬戸市の「戸」の一画目が横棒ではなく点に


# 03_雑談_なんでも

## 2026-05-10 23:30
okadatsuneo

cartoのバージョンは変わったようですが、変更内容は下記にあります。フォントはどうなんでしょうね？
https://www.openstreetmap.org/user/imagico/diary/408344
https://github.com/openstreetmap-carto/openstreetmap-carto/compare/v5.9.0%E2%80%A6v6.0.0


# 03_雑談_なんでも

## 2026-05-10 23:50
westantenna

確かに1カ月くらい前にちょっと色変わったな～とは思ってましたが（Remove low zoom landuse fadingと紹介されているものですね）
フォントが変わったのに気づいたのは今日なので、v6.0.0による変更ではないと思います。


# 03_雑談_なんでも

## 2026-05-10 23:50
westantenna

githubのcartoのリポジトリも更新されてなさそうです。よく分かりません。


# 03_雑談_なんでも

## 2026-05-11 09:33
tadanet3

兵庫県は宍粟市の波賀森林鉄道をマッピングしました。
https://www.openstreetmap.org/changeset/182464096#map=16/35.17925/134.56843


# 03_雑談_なんでも

## 2026-05-11 22:41
nyampire3568

公共測量成果の検索サイトがリニューアルされ、以前よりもまた別種の使いづらさになりました。。。
業界狭いので、あまり言うと「作ったのは実は知り合い」の罠にかかりそうですが、こう、なんか、こう、ううーん（）

https://psgsv4.gsi.go.jp/giaSearch/gsimaps/index.html


# 03_雑談_なんでも

## 2026-05-12 00:00
wish.f

今日何気なくデータを見ながら気づいたのですが、
ビルやマンションの名前について
StreetCompleteで編集をすると、`addr:housename=*`
で入力されるんですね。

私はEvery Doorの編集も多いので、
それに従って`name=*`で入力してますが、
新しい発見。


# 03_雑談_なんでも

## 2026-05-12 07:40
hokkosha

`addr:housename=*` は住所の方書名の部分に使うタグだと思ってました。
商業ビル内にテナントで入ってる店舗や企業などのPOI向け。
StreetCompleteとは解釈が違うようです。
私もビル本体の名称は `name=*` 派です。


# 03_雑談_なんでも

## 2026-05-12 22:09
wish.f

同じくそのように使うものだと思ってました。

`StreetComplete:quest_type=AddHousenumber` と一緒にタグ付けされてるので、
そうならない場合もあるのでしょうか...。


# 03_雑談_なんでも

## 2026-05-13 18:10
btm.smellman

@K.Sakanoshita OSC Kyotoの申し込みが始まりました。僕はOSGeo.JPの方で申し込みを送り、隣接希望でOSM Japanを入れました。よろしくー。


# 03_雑談_なんでも

## 2026-05-14 00:04
wish.f

雑談...
たまにやらかしますよね。
編集内容とコメントがずれてしまうこと…。


# 03_雑談_なんでも

## 2026-05-14 00:28
gray27

あるある


# 03_雑談_なんでも

## 2026-05-14 00:28
gray27

「あっ、違う」って気づきながら手はもう動いてて手遅れ


# 03_雑談_なんでも

## 2026-05-14 10:32
btm.smellman

https://www.gsi.go.jp/common/000269991.pdf 日本水準原点が5/20だけ公開らしいです。


# 03_雑談_なんでも

## 2026-05-14 12:06
gray27

陛下即位記念皇居周辺地形図（英語版）を持って行くか…


# 03_雑談_なんでも

## 2026-05-14 21:23
k.sakanoshita

いやぁ、寝起き（疲れが溜まって仕事を早退して寝てた）で寝ぼけた状態で文章を読むと読めないねー（恥ずかしい）。


# 03_雑談_なんでも

## 2026-05-15 14:13
tadanet3

うちの近所の自転車屋さんが
災害時には市職員の自転車は無償修理を行うそうなんです
これを上手いこと表現するタグはあるでしょうか？

災害時に無料になる飲料自販機があるんで、それと似た様なタグになるんちゃうかと想像してます


# 03_雑談_なんでも

## 2026-05-15 14:15
tadanet3

https://wiki.openstreetmap.org/wiki/Key:fee:conditional
fee:conditionalで何とか表現できるのか…


# 03_雑談_なんでも

## 2026-05-15 14:31
tadanet3

fee=yes
fee:conditional=no @ (emergency AND permit)
通常有料、緊急時に許可された者のみ無料
かなぁ…市職員のタグが見付からんかった🔍


# 03_雑談_なんでも

## 2026-05-18 01:03
higa49540

2008/2/19 - 2026/2/19のOSM日本のタグ件数

https://docs.google.com/spreadsheets/d/1Q1bb37S5jNNgeZMsNUckeDTxWAu9EGU56i0uP7ep2Bc/edit?usp=sharing
トップレベルキー https://wiki.openstreetmap.org/wiki/Category:Top-level_keys
をベースに、それぞれ使われているタグ値の件数を拾って、単純な件数順のグラフだけざっと作ってみました。これだけでも味わい深いと思いますが😅 よろしければコピーして自由に分析していただけますと幸いです。
分析の観点はいろいろあるかと思いますが、私自身が過去にやった内容は下記のようなものです。ご参考までに。
https://qiita.com/tags/osm%e7%b5%b1%e8%a8%88


# 03_雑談_なんでも

## 2026-05-20 10:38
gray27

今日の開催要項として見直してたけど、地理院自身は地理院地図の引用に許諾表示いらないのか！w


# 03_雑談_なんでも

## 2026-05-20 14:55
alt9800

別のサーバーでも注意喚起がありましたが、connpassなどにdiscordのリンクがあると、乗っ取ったアカウントを使ってスパム爆撃してくるようです。
https://x.com/viva_tweet_x/status/2056930905294553157?s=46

Discordへのリンクをお伝えするときは、
- クローラーが辿れる場所に記載しない(connpassであれば「参加者の情報」みたいなログインユーザだけが見られる場所に書く)
- 有効期限を7日間で設ける
- リンクの利用回数を50回程度に制限する
など対策が求められそうです。


# 03_雑談_なんでも

## 2026-05-20 15:28
gray27

コミュニティ鯖のセーフティ設定でDMとか招待リンクの規制できなかったっけ


# 03_雑談_なんでも

## 2026-05-20 15:44
alt9800

まるっと制御できましたね確か。


# 03_雑談_なんでも

## 2026-05-20 15:50
gray27

水準原点の公開日、いってきました～


# 03_雑談_なんでも

## 2026-05-20 15:51
gray27

電子基準点の中身も公開してました


# 03_雑談_なんでも

## 2026-05-21 16:24
kovoschiz

https://hothukurou.com/game/Barrier/index.html OSMのデータと実際の数の差はどのくらいか（ `=place_of_worship` ） https://twitter.com/hothukurou/status/1790169631489241092


# 03_雑談_なんでも

## 2026-05-21 23:12
okadatsuneo

地理院地図の住居表示の基礎番号、枝番まできちんと記載されているのを初めて見た。


# 03_雑談_なんでも

## 2026-05-23 12:48
k.sakanoshita

国土交通省なのに背景地図がOpenStreetMap。
じきに、国土地理院おじさんからクレーム受けそうなので、今だけかも知れませんね。
https://x.com/i/status/2057345701475164479


# 03_雑談_なんでも

## 2026-05-23 18:43
alt9800

梅田のBlooming CampにてCivic Tech Forumが行われていおり、OSMのブースを出されていたので遊びに行ってきました！
地域で経済を循環させることが一つのテーマとなっていて、マッピングの持続性を考えるいい契機でした！

お先に失礼します〜！
( @K.Sakanoshita   @Wish_F )


# 03_雑談_なんでも

## 2026-05-24 00:35
mijinkoagar

毎日編集途切れさせちゃった💦


# 03_雑談_なんでも

## 2026-05-26 16:13
kovoschiz

スパム・詐欺 @K.Sakanoshita


# 03_雑談_なんでも

## 2026-05-27 15:17
gray27

今日見たもの


# 03_雑談_なんでも

## 2026-05-27 20:10
wish.f

旧田無市本町の住居表示板ですね
旧保谷市にも本町があって、合併の際に旧市名になったんですよね。


# 03_雑談_なんでも

## 2026-05-27 20:11
gray27

西東京市の中心部はどこだ問題
旧表示が残ってるとは思ってなかった～


# 03_雑談_なんでも

## 2026-05-28 12:11
hokkosha

@K.Sakanoshita  技術的なことは詳しくないので、スパム対応等が中心になると思いますが、Discordの管理権限いただいてお手伝いできればと思います。
https://discord.com/channels/1280891177020686347/1280904713877061653/1509367684171694080


# 03_雑談_なんでも

## 2026-05-28 19:17
mucky9992719

今更ながら、先日台湾の高雄で開催されたWikimedia ESEAP Confに行ってきました。
ホテルの相部屋のルームメイトが、フィリピンのWikimedian兼OSM Mapperの Eugene Alvin Villarさんでした（スカラシップで参加してるのでホテルは原則相部屋）。


# 03_雑談_なんでも

## 2026-05-28 19:18
mucky9992719

私が特にコミュニケーション下手なのもあってあまり話ができなかったのが心残りでした。


# 03_雑談_なんでも

## 2026-05-28 21:10
nyampire3568

おわー！ Seavさんだ！ お元気そうでなにより。
OSMF本家の元理事さんでもあります！


# 03_雑談_なんでも

## 2026-05-28 21:31
mirakiki.

初めて投稿させていただきます。先月から岩手県盛岡市を中心にマッピングを始めた者です。
先ほどPlateau RapiDの存在を知り、Wiki等も拝見してぜひ使用したいと思っておりますが、2点質問があります（ここのルームで良いのでしょうか）。

1つ目は「情報源が自動でタグ付けされるので、保存時は他に追加対応せず通常のiDエディタを使用するときと同じで良いか」という点です。
2つ目は「その建物があることは分かっているがビルか住宅か判別しない場合に、一旦建物全般に変えてインポートしても良いか」という点です。

恐れ入りますが、ご教示いただけますと幸いです。よろしくお願いいたします。


# 03_雑談_なんでも

## 2026-05-28 21:46
mucky9992719

確か今はWikimedia ESEAP（東アジア、東南アジア、パシフィック）のなにかの役を持たれてたと思います。


# 03_雑談_なんでも

## 2026-05-28 21:55
nyampire3568

ようこそ！

1. Rapid Plateauは、編集の保存時に変更セットのタグとして、 source=RapiD_Plateau_JP が追加されます。なので、情報源は特に他に追加する必要はありません。（利用している航空写真もsourceに入ります。`aerial imagery;RapiD_Plateau_JP` みたいなかんじ）
2. ビルか住宅か判別しない場合は、建物全般（building=yes）に変えても大丈夫です。いちおう、Plateauは行政由来のデータセットなので、もし元から入っている場合（レアケース）、その値はけっこう確度高い気がしますが、間違っている可能性は否定できないので、安全側に倒して yes でも問題ないと思っています。

ぜひ使ってみて、なにか感じるところあればフィードバックもらえると嬉しいです。
チャンネルは、ここでも #RapiD_Plateau でもよいと思いますが、長くなりそうなら #RapiD_Plateau がオススメです。


# 03_雑談_なんでも

## 2026-05-28 22:03
mirakiki.

早速ありがとうございます。

おそらく、ここ最近のクマ出没（＆県によるアプリ提供）によって、北東北辺りの方は間接的にOSMタイルを見る機会が増えているので、引き続きマッピングしていこうと思います！


# 03_雑談_なんでも

## 2026-05-30 16:59
nyampire3568

Rapid Plateauの、作業進捗ダッシュボードを作ってみました。
各市町村の作業状況を一覧化できます。

なお、進捗はPlateauのオブジェクトを100、として割合を計算していますが、必ずしもPlateauが正しいわけではないので、インポート完了していても割合は100にはなりません。（だいたい90％以上くらいになる）

https://rapid.nyampire.info/dashboard/


# 03_雑談_なんでも

## 2026-05-30 17:00
nyampire3568

あと、Rapidの上のツールバーに、ダッシュボードとかのリンクを配置してみましたが、 missing translationのエラーがでます。
そのうち直すので、今日のところはこれでご容赦ください（）


# 03_雑談_なんでも

## 2026-05-31 14:15
mijinkoagar

OpenStreetMapにある街路樹とか木のデータは、Yahooカーナビでも表示されるのですが、この間自分が追加したのがもう追加されていました。割と短いスパンで更新しているようです。



---

# 10_マッピング活動

## 2026-05-02 14:06
nguyenhoangan1235

休日を利用して、近所の地図作りを進めている。まだ番地を調べていない路地などが、数多く残っているのだ。


# 10_マッピング活動

## 2026-05-02 14:08
k.sakanoshita

@nguyenhoangan お疲れ様です。ええと、もし良ければname以外にも名前を示すタグがあるので、そこに分けて記載するともっと良くなるかもです。


# 10_マッピング活動

## 2026-05-02 14:10
nguyenhoangan1235

その通りです。「name:vi-Hani」には漢字表記を、「name:vi」にはベトナム語表記を追加しました。実験として、これら両方の名称を「name=」タグにまとめて記載してみようと考えています。おそらく、その漢字表記を認識できるのは80歳以上の方に限られるのではないかと思います。


# 10_マッピング活動

## 2026-05-02 14:10
nguyenhoangan1235

80年前は1945年でした。1945年より前には、ベトナムにおいて漢字はほぼ完全に廃止されていました。


# 10_マッピング活動

## 2026-05-02 14:12
nguyenhoangan1235

現在、秋葉原のデータを参照しながら、「amenity=」をいかにエレガントに描画するかを検討しています。


# 10_マッピング活動

## 2026-05-02 14:15
k.sakanoshita

ご説明ありがとうございます。
ただ、nameタグにまとめるのは、色々と問題があるので分けて頂けたらと思います（後で誰かがたくさん修整する必要も出てきますし）。


# 10_マッピング活動

## 2026-05-02 14:16
nguyenhoangan1235

ご意見ありがとうございます。両方の名前を表示しつつ、「name=」の中ではそれらをどのように区別すればよいでしょうか？


# 10_マッピング活動

## 2026-05-02 14:17
nguyenhoangan1235

例えば香港では、「name=」がこちらと同じような使われ方をしています。これは大きな問題なのでしょうか？


# 10_マッピング活動

## 2026-05-02 14:26
k.sakanoshita

すみません。日本のルールを当てはめようとしていました。国ごとにルールが異なるので、提示頂いた香港は英語を併記することが基本ルールでした。
https://wiki.openstreetmap.org/wiki/Zh-hant:Hong_Kong_tagging


# 10_マッピング活動

## 2026-05-02 14:28
nguyenhoangan1235

承知いたしました！ご説明いただき、ありがとうございます。ただ、ベトナムでは80年前に漢字が廃止されていることを踏まえると、少し「余計なこと」のように感じられるという点については、私も同感です。


# 10_マッピング活動

## 2026-05-02 14:29
k.sakanoshita

ベトナムはどうも地域（少数民族の居住区など）では併記したほうが良い意見がある他は、基本的には分けたほうが良さそうです。ただ、具体的なルールはこれから決めていくのが良いかもですね。


# 10_マッピング活動

## 2026-05-02 14:30
nguyenhoangan1235

おっしゃる通りだと思います。「name=」の欄からは漢字表記の名前を削除したほうがよいでしょう。というのも、それらの名前は書籍の中以外では、実質的に存在しないからです。村の入り口の門でさえ、そうした名前を目にすることは稀です。


# 10_マッピング活動

## 2026-05-02 14:33
nguyenhoangan1235

@K.Sakanoshita あと、ここはベトナム国家大学のすぐ近くなんです。数時間後には、そこで高市早苗さんが講演を行う予定なんですよ（^ω^）


# 10_マッピング活動

## 2026-05-02 14:51
nguyenhoangan1235

name= から漢字を削除しました


# 10_マッピング活動

## 2026-05-02 20:47
btm.smellman

https://www.openstreetmap.org/changeset/182110788#map=19/35.638124/140.157148 ちょっとだけOSM描きました。


# 10_マッピング活動

## 2026-05-02 20:59
k.sakanoshita

Mappy Hour案内文
【MappyHourにご参加されるみなさまへ】
MappyHourは、みんなでOpenStreetMapを描いていくイベントです。

近所でも旅先でも、興味が湧いた場所から気楽に描いていきましょう。
まずは、このチャットに「何処を描きたいか」を投稿してみましょう。
大まかな都市名や駅名でOK。描きたいものがあればそれも合わせて！
地図の描き方が分からない人は、以下のサイトを読んでみてください。
それでも分からなければチャットで質問ください。早めに返答します。

LearnOSM（はじめてからのOpenStreetMapガイド）
https://learnosm.org/ja/beginner/

地図を描いている時（マッピング中）、どう描けば良いか分からない
ものが見つかったら、チャットで描き方を一緒に考えていきましょう。
もちろん、描いている時に気が付いたこと、面白い地物などがあれば
どんどんチャットでネタを提供していきましょう。
そして、地図を描いた後は、チャットで成果発表してみませんか？
https://osm.org で描いた辺りを表示して、URLをチャットに書けば
何処をマッピングしたのか、みんなに伝えることが出来ます。
※画面キャプチャを貼り付けるのも良いですねー（Copyright付けてね）
そうそう、地図を保存する時のコメントに「#MappyHourJapan」を
追記したら、以下のサイトのHashtagsランキングに掲載されるかも？

https://osmstats.neis-one.org/

それでは、みなさん楽しくいきましょう。


# 10_マッピング活動

## 2026-05-02 21:25
k.sakanoshita

今日は、Linuxユーザー改「lilo/東海道Lug」の発表会へ自転車で行ったときのマッピング！
途中で自転車のブレーキが壊れて1時間ほど遅刻したのは内緒だ（笑


# 10_マッピング活動

## 2026-05-02 21:27
kzmi

https://discord.com/channels/1280891177020686347/1280891177608024169/1496039914767253615 でインドアマッピングの事例をたくさん教えていただいたので、実際に筑波大学（茨城県つくば市）内のよく利用するところでなにかマッピングを試してみようと思います


# 10_マッピング活動

## 2026-05-02 21:50
alt9800

OSM2Brenderの逆版をGW中に作れたらいいな...


# 10_マッピング活動

## 2026-05-02 21:51
alt9800

今日はひさびさに柳川市のマッピングしてます！
(久しぶりに自宅にいられるぜ...!!)


# 10_マッピング活動

## 2026-05-02 21:55
gray27

描きました


# 10_マッピング活動

## 2026-05-02 22:00
gray27

時間帯は昼間ですが、今日は現地サーベイもしました。8年くらい前のテナント情報or未プロットでした。人の多さから早々に退却したので、また時機改めて行かなきゃな、という感じです


# 10_マッピング活動

## 2026-05-02 22:13
tom_konda

こんばんは、本日は引き続き相模大塚駅北西エリアを進めていこうと思います。


# 10_マッピング活動

## 2026-05-02 22:16
qing_06282

鹿児島県奄美市
マンネリしてきたので他所様のところをマッピング
(行ったことないけど...)


# 10_マッピング活動

## 2026-05-02 22:21
k.sakanoshita

お疲れ様です！インドアマッピングいいですね。よろしくお願いします！


# 10_マッピング活動

## 2026-05-02 22:22
k.sakanoshita

あー。それは楽しそう。精密な3Dビルディングが量産されると良いですね！


# 10_マッピング活動

## 2026-05-02 22:23
k.sakanoshita

お疲れ様でした！田んぼのなかの集落って感じかな？


# 10_マッピング活動

## 2026-05-02 22:23
k.sakanoshita

お疲れ様です。先ほどもお疲れ様でした！今週もよろしくね！


# 10_マッピング活動

## 2026-05-02 22:23
ryoa8139

たまには都内を。

＞(RapiD_Plateau)追加エリアの希望ですが、もしよろしければ、世田谷区・渋谷区・新宿区・中野区・豊島区を追加いただければと思います。
↑ホントにそう思う・・・（欲を言うと板橋区も）
（建物の数が半端ない＆不整形な建物が多い ）


# 10_マッピング活動

## 2026-05-02 22:24
k.sakanoshita

お疲れ様でした！気分転換にいいと思います！（私もたまに全く知らない場所をマッピングするので分かります）


# 10_マッピング活動

## 2026-05-02 22:25
gray27

あと、高層物の影で見えないとか


# 10_マッピング活動

## 2026-05-02 22:25
k.sakanoshita

お疲れ様です！都内は意外とマッピングされていないですからね。よろしくお願いします！


# 10_マッピング活動

## 2026-05-02 22:41
nmaruichi0129

こんばんは、
本日は、久しぶりにスポーツ的な意味でサイクリングしました。
サイクルコンピュータの最大勾配が、14% でところがありました。
そのルートのなかに、私が以前に描いていた林道があるのですが、その林道は、Google Map にありません。
Street View では、林道入り口に柵がしてあったので現地確認しました。
確認前に調べたところ、災害復旧工事の対象となっている様だった(もともと「かなりやばい(危ない)多くの未舗装路を道路」でした)ので、現地確認しました。
やはり柵をされていました。(現地で工事が行われていることは、わからなかったので access=no と柵を描いておきます。)

また新しい橋が開通したので、先週現地確認に行きました。予算削減のため初期の構想から歩道が外されたのは知っていたですが、歩行者も自転車も通行禁止でしたので走れませんでした。
上記のアクセス制限は、タグ付けされていないので設定しておこうと思います。
ベタ踏み橋と評価される 6% 勾配のある橋の下り線です。

あと、最近に描いていた住宅団地の建物を追加が終わりそうなのでそちらにも取りかかりたいと思いますが、作業は間に合わない気がします。
そういえば、定例会でフォローしておくといったのだ遅れるかもしれません。


# 10_マッピング活動

## 2026-05-02 22:42
okadatsuneo

こんばんは。田園調布の建物空白域を埋めてます。


# 10_マッピング活動

## 2026-05-02 22:47
k.sakanoshita

お疲れ様でした！歩道がなくなった橋は残念ですね。うーん。お忙しい中、フォローありがとうｇざいます。余裕のある時で十分ですので！


# 10_マッピング活動

## 2026-05-02 22:47
k.sakanoshita

お疲れ様でした！田園調布にも空白ありましたかー。感謝！


# 10_マッピング活動

## 2026-05-02 23:26
kzmi

想定外に時間を使ってしまいましたが、図書館の内部が無事マッピングできました！
JOSM初利用でもあったのですが良い感じに使い慣れることができました 🍵 
https://openlevelup.net/?l=0#20/36.08612/140.10623
https://www.openstreetmap.org/changeset/182119397


# 10_マッピング活動

## 2026-05-03 00:07
hokkosha

今日は沖縄アリーナというところに推し活にやってきました。
もう疲れたけど、会場周辺の敷地内通路とか最新になってなかったのでちょっとだけ修正。


# 10_マッピング活動

## 2026-05-03 00:08
k.sakanoshita

お疲れ様でした！インドアアプリが充実していくと良いですね。


# 10_マッピング活動

## 2026-05-03 00:08
k.sakanoshita

沖縄にきてましたか！そちらも併せてお疲れ様でした！


# 10_マッピング活動

## 2026-05-03 00:14
nmaruichi0129

住宅団地の建物を追加は、完了かと思います。この後は、現地調査して公園やその他描ける地物を修正したいと思います。
林道の名前で調べたときに事業費の書かれた「林道災害復旧事業」の資料を見たので直ったら、通れるようになるのか気になります。
橋の方は、予定していた通行禁止以外に 'bridge:name' キーを設定しただけです。


# 10_マッピング活動

## 2026-05-03 00:25
tom_konda

今晩の成果です。
駅から近い区画は埋まってきた感じです。
引き続き、周辺を埋めていきたいです。
https://www.openstreetmap.org/changeset/182121899


# 10_マッピング活動

## 2026-05-03 00:42
hokkosha

沖縄アリーナのあるコザ運動公園、地理院シームレス画像には存在せずEsri画像には存在する敷地内通路と駐車場が多数ありましたが、今日現地行ってみてEsriが正しいのを確認したので、Esriトレースで少々修正。
もう眠いのでまた今度にします。
ライブは2日間なので、2日目ももうちょっと周辺見れるといいなと思いつつ、多分暑くてやらない気がします。


# 10_マッピング活動

## 2026-05-03 01:33
wish.f

本日の成果は
数年前に警察の管轄変更があったところの交番等に入ってる名称の修正（とその近辺の修正）
建物が三重にトレースされていた（！）造幣局広島支局の修正
あと建物が描かれてないところのトレースをやってました。

どうも、JOSMでデータをダウンロードせずにトレースされてたようで...笑


# 10_マッピング活動

## 2026-05-03 06:01
gray27

おはようございﾏｯﾋﾟﾝ


# 10_マッピング活動

## 2026-05-03 11:18
stolas_goetia_

甲斐町公園


# 10_マッピング活動

## 2026-05-03 15:53
k.sakanoshita

お疲れ様でした！結構な量の建物書かれましたね。すごい。


# 10_マッピング活動

## 2026-05-03 15:54
k.sakanoshita

お疲れ様でした！花博近くの地図も充実してきましたね。


# 10_マッピング活動

## 2026-05-03 15:56
k.sakanoshita

お疲れ様でした！JOSM使いがみんな熟練とは限らないのがありますよね（汗


# 10_マッピング活動

## 2026-05-03 15:56
k.sakanoshita

お疲れ様でした！丁寧な公園マッピングですね。


# 10_マッピング活動

## 2026-05-03 19:24
alt9800

新興住宅地(といっても10年ものくらいですが)も道路も書かれてなくてギョッとしますね〜、頑張って追加しなきゃ... ＠柳川市


# 10_マッピング活動

## 2026-05-03 19:57
stolas_goetia_

福岡県柳川市間ですね、わかりました.
近いうちに佐賀へ行く予定なので、その際にここを通れるか確認して、地図編集をしようと思っています。


# 10_マッピング活動

## 2026-05-04 11:10
k.sakanoshita

すみませんが、この投稿はOpenStreetMapと関係あるかご返答ください。


# 10_マッピング活動

## 2026-05-04 11:33
nguyenhoangan1235

tại sao anh lại ở đây? server này cấm ko quảng cáo rác.
(なぜここにいるのですか？このサーバーはスパム広告を禁止しています。)


# 10_マッピング活動

## 2026-05-04 17:04
gray27

インドアマッピングと呼べるほどではないけれど


# 10_マッピング活動

## 2026-05-04 21:03
alt9800

(背景地理院地図航空写真)
今年も有田陶器市に行ってきました。
昨年は気が付かなかったのですが、有田町内はbingの2011年のソースからインポートされた建物が多くて建物とそれに対する窯元などPoIのマッピングは充実してきているものの、しかしながら道路や航空写真に対して建物がずれていて修正が必要なところも結構ありそうです(画像はセットバック後)
新興の陶器屋さんも素敵なお店がたくさんできていたので地図に残さねばという所存です


# 10_マッピング活動

## 2026-05-04 21:11
alt9800

最近こちらのチャンネルにもスパムがたまに流れてきますね。
(あるいはツールを使った人間による無差別なメッセージなんでしょうけどBotと変わりはないので...) 
デフォルトでは三人くらいから通報受けると強制的にほかのユーザにも表示されなくなってるはずで、
`...>メッセージの通報>スパム`と入れると重みづけできて他のユーザも助かると思います。


# 10_マッピング活動

## 2026-05-06 18:10
gray27

私だけかしら


# 10_マッピング活動

## 2026-05-06 18:12
gray27

うーん、応答速度は遅いけど動かないことはないな iD


# 10_マッピング活動

## 2026-05-06 18:14
k.sakanoshita

EveryDoorの動きも少し遅い感じですねー


# 10_マッピング活動

## 2026-05-06 18:25
tom_konda

さっき EveryDoor からアップロードしようとしたら拒否されました。
再試行したらアップロードできたので、サーバの調子が悪いのかもしれないですね


# 10_マッピング活動

## 2026-05-06 19:11
gray27

今日の夕方はそんなに人も多くなくわりとゆっくりサーベイできました


# 10_マッピング活動

## 2026-05-06 19:11
wish.f

JOSMでもサーバの反応がないメッセージが出ました


# 10_マッピング活動

## 2026-05-07 15:00
gray27

規模が縮小してしまった山梨県中央市のショッピングセンターをマッピングしてきました


# 10_マッピング活動

## 2026-05-07 17:41
gray27

PCから手直し


# 10_マッピング活動

## 2026-05-08 02:07
alt9800

九州産業大学に行ってまいりました。
色々書き方のスタイルでよくないお作法かもしれませんが、芝生のレイヤーを分けて描くことでサッカーコートを実現していて感心しました。


# 10_マッピング活動

## 2026-05-09 18:56
canunen_tomtom

Good evening. For those of you who might be interested to address and check data validation issues, these three Maproulette challenges are also available: 

https://maproulette.org/browse/challenges/54920
https://maproulette.org/browse/challenges/54921
https://maproulette.org/browse/challenges/54728
https://maproulette.org/browse/challenges/54755

I am particularly curious about a high number of roads tagged as **alley**, which by definition provides only back access for utilities such as garbage collection. If a road segment has access to a main entrance of a structure, it would be either service or higher (residential etc.). 

Do you think it is a misinterpretation or a mistranslation in the presets? In Turkish community we also have a translation issue with **living streets** so editors overuse that tag for Turkish data. 

I am also checking those roads from GSI datasets and they look like driveable, mostly residential roads providing direct access to buildings. 

Any clarification will be much appreciated. Thank you.


# 10_マッピング活動

## 2026-05-09 20:58
k.sakanoshita

Mappy Hour案内文
【MappyHourにご参加されるみなさまへ】
MappyHourは、みんなでOpenStreetMapを描いていくイベントです。

近所でも旅先でも、興味が湧いた場所から気楽に描いていきましょう。
まずは、このチャットに「何処を描きたいか」を投稿してみましょう。
大まかな都市名や駅名でOK。描きたいものがあればそれも合わせて！
地図の描き方が分からない人は、以下のサイトを読んでみてください。
それでも分からなければチャットで質問ください。早めに返答します。

LearnOSM（はじめてからのOpenStreetMapガイド）
https://learnosm.org/ja/beginner/

地図を描いている時（マッピング中）、どう描けば良いか分からない
ものが見つかったら、チャットで描き方を一緒に考えていきましょう。
もちろん、描いている時に気が付いたこと、面白い地物などがあれば
どんどんチャットでネタを提供していきましょう。
そして、地図を描いた後は、チャットで成果発表してみませんか？
https://osm.org で描いた辺りを表示して、URLをチャットに書けば
何処をマッピングしたのか、みんなに伝えることが出来ます。
※画面キャプチャを貼り付けるのも良いですねー（Copyright付けてね）
そうそう、地図を保存する時のコメントに「#MappyHourJapan」を
追記したら、以下のサイトのHashtagsランキングに掲載されるかも？

https://osmstats.neis-one.org/

それでは、みなさん楽しくいきましょう。


# 10_マッピング活動

## 2026-05-09 21:38
k.sakanoshita

6/21に三ノ宮で五宮～八宮を歩くマッピングパーティするので、その下見と軽くマッピングしました。
ただ、建物がまだまだ少ないので、建物マッピングに協力してくれる方がいるとうれしいなー。


# 10_マッピング活動

## 2026-05-09 21:40
nmaruichi0129

こんばんは、
本日は、mapillary の写真をアップロードをまとめて行いました。
この中にGW中のものがあり、描かれていない短い道もあったのでマッピングしたいと思います。
その他、最近に描いていた住宅団地の周辺も描くかも……。


# 10_マッピング活動

## 2026-05-09 22:00
k.sakanoshita

お疲れ様です！マピラリーお疲れ様でした！
道のマッピングよろしくお願いしますね！


# 10_マッピング活動

## 2026-05-09 22:01
k.sakanoshita

ここだけはげ山ー。リレーション壊れてる？（あまり見たくない）
https://www.openstreetmap.org/relation/11542725#map=12/35.9091/136.3129


# 10_マッピング活動

## 2026-05-09 22:07
kk.wcjp

https://www.openstreetmap.org/changeset/182424023#map=17/34.624264/135.554408
環濠都市だった平野の「平野十三口」（とその跡地）を揃えました


# 10_マッピング活動

## 2026-05-09 22:17
okadatsuneo

Hi,
From what I've seen, it seems that some mappers prefer to tag "highway=service" with "service=alley," even if they're just regular residential roads.


# 10_マッピング活動

## 2026-05-09 22:51
okadatsuneo

マルチポリゴンのウェイが交差していたのを直したので、これで直るかも？です。


# 10_マッピング活動

## 2026-05-09 22:59
tom_konda

こんばんは、本日も相模大塚駅北西エリア周辺のマッピングをしていこうと思います。


# 10_マッピング活動

## 2026-05-09 23:08
k.sakanoshita

お疲れ様でした！平野区のあたりはマッピングがまだまだな場所なので、ありがたくー。


# 10_マッピング活動

## 2026-05-09 23:09
wish.f

今日のMappyHourは明日のOSM概要説明のスライドを作っているのですが、
途中ですべての内容が文字化けしてしまってなんでやねん！っとなっています。


# 10_マッピング活動

## 2026-05-09 23:10
k.sakanoshita

ドラクエ２のふっかつの呪文みたい！


# 10_マッピング活動

## 2026-05-09 23:11
k.sakanoshita

ありがとう！道路などを修正されている方がクロスさせてしまったのかな。とにかく感謝！


# 10_マッピング活動

## 2026-05-09 23:12
k.sakanoshita

お疲れ様です！来年の今頃はお世話になってそうな場所なので、よろしくお願いします！


# 10_マッピング活動

## 2026-05-09 23:14
wish.f

突然Noto Sans JPフォントのエラーが発生したみたいです笑


# 10_マッピング活動

## 2026-05-10 00:17
nmaruichi0129

接続する道路の方も精度が低かったので線形修正を行ったので、最初の方のみになりました。


# 10_マッピング活動

## 2026-05-10 02:27
tom_konda

今晩の成果です。桜森交差点付近が大分埋まりました。
https://www.openstreetmap.org/changeset/182430692


# 10_マッピング活動

## 2026-05-10 08:51
gray27

昨夜の描き描き


# 10_マッピング活動

## 2026-05-10 13:53
kussun0183

こんにちは。OSMとuMapのことを紹介することになったので、簡単に紹介サイトを作りました。
久しぶりに著作権ページみたけど、
著作権表示が、@OpenStreetMap contributorsから、@OpenStreetMapに変わったのかな？
https://minamiosakasensyuwakayamatankenki.info/archives/2839?preview_id=2839&preview_nonce=bf9092648b&preview=true&_thumbnail_id=2845


# 10_マッピング活動

## 2026-05-10 14:55
gray27

WordPressの記事リンク、previewだからかな、見れなかったですー


# 10_マッピング活動

## 2026-05-10 14:55
gray27

2839?pre の?以後を消したら普通に見えた


# 10_マッピング活動

## 2026-05-10 18:27
zaneo

目標は、一時停止標識、横断歩道、車線数、制限速度、路面状況でした。


# 10_マッピング活動

## 2026-05-10 22:51
westantenna

四日市の中央通の通行方法が大きく変わったところを、ざっくり反映しました。大きな書き換えは緊張します。


# 10_マッピング活動

## 2026-05-13 11:34
nguyenhoangan1235

この地域における、JAXAの森林被覆データをOpenStreetMapへインポートする作業のうち、20%が完了しました。現在は、マッピング済みの森林データに対する品質確認（QA）を行っており、その後、各森林データにJAXAへのクレジット情報を追加する作業を進めています。

この地域の作業が完了した暁には、機械学習への活用を通じて、衛星データの有効性をさらに高めることにつながるよう願っています。


# 10_マッピング活動

## 2026-05-13 11:36
nguyenhoangan1235

データは現在、まだクリーンアップの段階にあります。データのQA（品質保証）を行うために、「divide and map. now.」を使用しています。
-> https://qa.damn-project.org/mappy/#area=2729


# 10_マッピング活動

## 2026-05-15 17:21
canunen_tomtom

皆さん、こんにちは！

今週土曜日のMappy Hourにぴったりかもしれない、2つのMapRouletteチャレンジを共有させてください。日本における重複した道路セグメントと未接続の道路セグメントを特定・修正するチャレンジです。

🔹 重複した道路（Duplicated Highways）：https://mpr.lt/c/54967
🔹 未接続の道路（Disconnected Highways）：https://mpr.lt/c/54965

今週土曜日にマッピングするものをお探しでしたら、ぜひ挑戦してみてください！

==========
Hi everyone!
 
I'd like to share two MapRoulette challenges that might be a fit for this Saturday's Mappy Hour, focusing on identifying and fixing duplicated and disconnected highway segments in Japan

Duplicated Highways: https://mpr.lt/c/54967
Disconnected Highways: https://mpr.lt/c/54965

If you're looking for something to map this Saturday, feel free to give these a try!

Happy Mapping! 🗺️


# 10_マッピング活動

## 2026-05-16 20:59
k.sakanoshita

Mappy Hour案内文
【MappyHourにご参加されるみなさまへ】
MappyHourは、みんなでOpenStreetMapを描いていくイベントです。

近所でも旅先でも、興味が湧いた場所から気楽に描いていきましょう。
まずは、このチャットに「何処を描きたいか」を投稿してみましょう。
大まかな都市名や駅名でOK。描きたいものがあればそれも合わせて！
地図の描き方が分からない人は、以下のサイトを読んでみてください。
それでも分からなければチャットで質問ください。早めに返答します。

LearnOSM（はじめてからのOpenStreetMapガイド）
https://learnosm.org/ja/beginner/

地図を描いている時（マッピング中）、どう描けば良いか分からない
ものが見つかったら、チャットで描き方を一緒に考えていきましょう。
もちろん、描いている時に気が付いたこと、面白い地物などがあれば
どんどんチャットでネタを提供していきましょう。
そして、地図を描いた後は、チャットで成果発表してみませんか？
https://osm.org で描いた辺りを表示して、URLをチャットに書けば
何処をマッピングしたのか、みんなに伝えることが出来ます。
※画面キャプチャを貼り付けるのも良いですねー（Copyright付けてね）
そうそう、地図を保存する時のコメントに「#MappyHourJapan」を
追記したら、以下のサイトのHashtagsランキングに掲載されるかも？

https://osmstats.neis-one.org/

それでは、みなさん楽しくいきましょう。


# 10_マッピング活動

## 2026-05-16 21:09
hokkosha

久しぶりの参加です。
GW沖縄旅行中に体調を崩し、帰ってきてから寝込んでOSMの連続編集記録が199日で途切れてしまいました😭 
今年こそ365日編集を達成したかったのに無念…

復活してから気を取り直してマッピングも再開。
沖縄本島も中部までいくとあまりマッピングが進んでいない箇所があり、レンタカーで幹線道路を通り過ぎただけではありますが、イオンモール沖縄ライカムという巨大モールの周辺の森林などが全然描かれていなかったところをちょっと埋めました。


# 10_マッピング活動

## 2026-05-16 21:11
k.sakanoshita

お疲れ様です。体調不良の中、無理せずご参加くださいー。


# 10_マッピング活動

## 2026-05-16 21:12
hokkosha

ありがとうございます。
ちなみに現地でもあまりパソコン開く気力がなかったのですが、現地ではEvery Doorでホテル周辺のマンションの名前だけ入れてなんとか連続編集つないだりしてました。
普段はJOSMですが、スマホアプリという選択肢があることは大事ですね。


# 10_マッピング活動

## 2026-05-16 21:22
junkyard.critter

初めての参加です！
東京の東急目黒線の西小山駅～洗足駅周辺をマッピングしようと思います


# 10_マッピング活動

## 2026-05-16 21:30
k.sakanoshita

始めまして！意外と首都圏のマッピングはまだまだなのでありがたい！よろしくお願いしますね！


# 10_マッピング活動

## 2026-05-16 21:33
tom_konda

こんばんは。
本日も相模大塚駅の辺り（今回は北方向）のマッピングをしていこうと思います。


# 10_マッピング活動

## 2026-05-16 21:39
k.sakanoshita

お疲れ様です！今週も引き続きよろしくお願いしますね！


# 10_マッピング活動

## 2026-05-16 21:40
k.sakanoshita

そうそう、マッピングのネタが無い方は、ご提案頂いたMapRoulette如何でしょうか？


# 10_マッピング活動

## 2026-05-16 21:48
qing_06282

こんばんは
桜島の道路形状修正など調整をしていきます


# 10_マッピング活動

## 2026-05-16 21:49
k.sakanoshita

お疲れ様です！桜島はいつか行きたい場所！
マッピングよろしくお願いします！


# 10_マッピング活動

## 2026-05-16 22:33
nmaruichi0129

本日、(西風新都と免許鵜センター間に)新しい道路がOSMに(現地に道路名の表示は無かった気がするが、)「西風新都環状線」と言う名称で描かれているの気づき、Mapillary用の写真を撮りとgpx取りに(70km弱の)サイクリングを行いました。
上記の道は、航空写真では工事中の状態ではっきりとはわからない気がしていますが、地理院時地図には記載されています。
その際に他の新しい道が完成しているの気づきました。
前の日曜日に最近に描いていた住宅団地の(70km弱の)サイクリングでの現地照査とmapillary の写真撮影+アップロードを行っています。(←来週以降になりそう)
まだOSMに描かれていない「その際に他の新しい道」を描いておこうと思います。こちらは久しぶりにGNSSのトレースログの情報からになります。(描いた後でMapillaryにアップします)


# 10_マッピング活動

## 2026-05-16 22:55
junkyard.critter

眠くなってきましたので今日はここまでにします！
https://www.openstreetmap.org/changeset/182743545
明日続けます！


# 10_マッピング活動

## 2026-05-16 22:57
k.sakanoshita

お疲れ様でした！新しい道ってわくわくしますねー。引き続きよろしくお願いします！


# 10_マッピング活動

## 2026-05-16 22:59
nyampire3568

Plateau用Rapidの改修をしています。
基本的にClaude codeさん任せなので、僕的にはポチポチ内容見ながらOKだしたりツッコミしたりしています。
バグを取ったり、Upstreamの改修を取り込んだりして、来週はデータ更新をしようかな、というところ。
そこそこ使い勝手よくなってきたと、自己肯定感あげております（）

https://rapid.nyampire.info/


# 10_マッピング活動

## 2026-05-16 23:00
k.sakanoshita

お疲れ様でした！変更セットのコメントも丁寧で良い感じですね！


# 10_マッピング活動

## 2026-05-16 23:43
gray27

https://www.openstreetmap.org/changeset/182746014 branchやらaddr:*やらをちょっとお手入れ
本業をさっき終わらせてきたのでちょっとだけ。


# 10_マッピング活動

## 2026-05-16 23:52
qing_06282

natural=screeとnatural=woodの調整でちょっとは航空写真に寄せることができたかなーと


# 10_マッピング活動

## 2026-05-16 23:55
k.sakanoshita

お疲れ様です。かなり良くなった感じがしますね。こういった感じでPLATEAUのデータが使えるのは理想的だなと思います。これを使ったワークショップとか開けたらいいけど、興味持ってくれる方がいるかなぁ。


# 10_マッピング活動

## 2026-05-16 23:57
k.sakanoshita

お疲れ様でした！お店の追加は嬉しいですねー。


# 10_マッピング活動

## 2026-05-17 00:33
nmaruichi0129

本日の編集です。
今回追加したかった新しい道(1本のウェイ)に対して既存の未舗装だった護岸道路と接続と障害物(車両止め?)は別の編集で設定したいと思います。
また上記の道を含む本日サイクリング分のMapillaryのアップロード中です。


# 10_マッピング活動

## 2026-05-17 00:47
tom_konda

今晩の成果です。
本当はもう2ブロックぐらいやりたかったのですが、気力が持たず断念。
https://www.openstreetmap.org/changeset/182748799


# 10_マッピング活動

## 2026-05-19 21:29
gray27

今日はちょこっと現地


# 10_マッピング活動

## 2026-05-19 21:49
gray27

気づいたら所沢駅南西部～ドーム周辺の宅地が全部描かれてる…


# 10_マッピング活動

## 2026-05-21 11:18
mapconcierge

青学の授業で、RapiD 経由の PLATEAU インポートを学生たちに試してもらいました！
南側の東村山市は PLATEAU建物インポート済みなので、これで面的に接続されたと思います。

特に、狭山丘陵を活動拠点としている公益財団法人 トトロのふるさと基金さんが活動のなかでOSM使われていたので優先しました！


# 10_マッピング活動

## 2026-05-21 11:20
gray27

そりゃーあっという間に進むわけだ！


# 10_マッピング活動

## 2026-05-21 11:22
mapconcierge

今どきの大学生初心者に建物入力作業を計測させましたが、背景の航空写真がクリアでテンポよくいくと 100建物/min くらいのスピードがでています。取りこぼしの建物は Validator として古橋がチェックしてフォローアップしています。


# 10_マッピング活動

## 2026-05-21 13:12
gray27

久々に`addr`タグ触ってます


# 10_マッピング活動

## 2026-05-21 20:09
nyampire3568

rapid plateauですが、いま、ジオメトリが壊れてるのを入れ替えてます。
明日くらいまでかかるはず。


# 10_マッピング活動

## 2026-05-23 15:01
nyampire3568

Rapid Plateauのデータ入れ替えと、Relationの投入機能追加、完了しました！
https://rapid.nyampire.info/


# 10_マッピング活動

## 2026-05-23 15:03
nyampire3568

ストレージを増強したので、少し余裕ができました。
対象の都市を増やす事が可能です。
2025年に追加された自治体も対象にできるかと思います。

https://front.geospatial.jp/plateau_portal_site/


# 10_マッピング活動

## 2026-05-23 20:58
k.sakanoshita

Mappy Hour案内文
【MappyHourにご参加されるみなさまへ】
MappyHourは、みんなでOpenStreetMapを描いていくイベントです。

近所でも旅先でも、興味が湧いた場所から気楽に描いていきましょう。
まずは、このチャットに「何処を描きたいか」を投稿してみましょう。
大まかな都市名や駅名でOK。描きたいものがあればそれも合わせて！
地図の描き方が分からない人は、以下のサイトを読んでみてください。
それでも分からなければチャットで質問ください。早めに返答します。

LearnOSM（はじめてからのOpenStreetMapガイド）
https://learnosm.org/ja/beginner/

地図を描いている時（マッピング中）、どう描けば良いか分からない
ものが見つかったら、チャットで描き方を一緒に考えていきましょう。
もちろん、描いている時に気が付いたこと、面白い地物などがあれば
どんどんチャットでネタを提供していきましょう。
そして、地図を描いた後は、チャットで成果発表してみませんか？
https://osm.org で描いた辺りを表示して、URLをチャットに書けば
何処をマッピングしたのか、みんなに伝えることが出来ます。
※画面キャプチャを貼り付けるのも良いですねー（Copyright付けてね）
そうそう、地図を保存する時のコメントに「#MappyHourJapan」を
追記したら、以下のサイトのHashtagsランキングに掲載されるかも？

https://osmstats.neis-one.org/

それでは、みなさん楽しくいきましょう。


# 10_マッピング活動

## 2026-05-23 21:18
k.sakanoshita

じー。


# 10_マッピング活動

## 2026-05-23 21:18
nmaruichi0129

こんばんは、
先々週の日曜日に最近に描いていた住宅団地の(70km弱の)サイクリングで現地調査(+mapillary)を元に公園など名前を確認した情報を加えたいと思います。
住宅団地内の公園のほとんどは、現状は住宅地扱いになっているので分割することになります。


# 10_マッピング活動

## 2026-05-23 21:19
k.sakanoshita

お疲れ様です！70kmってすごい距離ですね。公園マッピングよろしくお願いします！


# 10_マッピング活動

## 2026-05-23 21:27
wish.f

こんばんは
Civic Tech Forum の前後に周辺のサーベイをしてきたので、編集していこうと思います。


# 10_マッピング活動

## 2026-05-23 21:31
qing_06282

こんばんは
数年放置されていた地図メモつぶしにサーベイしてきたので反映します


# 10_マッピング活動

## 2026-05-23 21:31
sava_god

こんばんは、初参加ですがよろしくお願いします。卒研のため住宅街をマッピングしようと思います。


# 10_マッピング活動

## 2026-05-23 21:32
nmaruichi0129

ちょっとジロ・デ・イタリアを見ながら開始の投稿をしていました。(時々書くのを忘れて、TV見てました。)
「70km弱」は、先週の投稿のコピぺだったりしますが、正確には、 5/10 に 68.7km
先週の 5/16 が、 76km のサイクリングしていました。
(GPSの取得に使っている サイクルコンピュータ(Garmin) の関係で半月ぐらいに200km走るチャレンジをやってみようとしたためだったりします。)
最近は、一回のサイクリングでは 100km以下の短い距離しか走れていませんけどね。


# 10_マッピング活動

## 2026-05-23 21:44
k.sakanoshita

今日はありがとう！マッピングよろしくお願いします！


# 10_マッピング活動

## 2026-05-23 21:45
k.sakanoshita

100km以下が短い距離とはー。サーベイし放題ですね。すごい。


# 10_マッピング活動

## 2026-05-23 21:45
k.sakanoshita

お疲れ様です！おー。地図メモを解消させるのは地味に大事なのでありたがたく！


# 10_マッピング活動

## 2026-05-23 21:46
k.sakanoshita

お疲れ様です！始めまして！卒研ですか、何か気になることとか、分からないこと。協力が欲しいことがあれば、お気軽に、このチャンネんでお問い合わせくださいー。


# 10_マッピング活動

## 2026-05-23 21:49
sava_god

昨日の夜、国土地理院のオレンジ枠を、自動検出し、補助するようなプログラムを作成しようとしたのですが、うまくいかず諦めました。


# 10_マッピング活動

## 2026-05-23 21:50
k.sakanoshita

ええと。それは禁止されている行為なので、止めて頂きたく（OpenStreetMap Foundation Japanが国土地理院とそう調整したハズです）。


# 10_マッピング活動

## 2026-05-23 21:51
sava_god

そうなんですね、知りませんでした


# 10_マッピング活動

## 2026-05-23 21:52
sava_god

どちらかというと、密集度の計算の補助のため導入したく試行錯誤していました。


# 10_マッピング活動

## 2026-05-23 21:53
k.sakanoshita

ここに書いてあったりします。
って、普通はみんな見る場所でも無いので、知らないのは仕方ないかなと。
https://wiki.openstreetmap.org/wiki/JA:GSImaps


# 10_マッピング活動

## 2026-05-23 21:54
k.sakanoshita

具体的には「地理院タイルのデータを形式変換や抽出してインポートすることは許可されていません。」となります。


# 10_マッピング活動

## 2026-05-23 21:55
k.sakanoshita

ざっくりとした場所を教えて下さいな。私も少しならマッピングするのでー。


# 10_マッピング活動

## 2026-05-23 21:56
sava_god

石川県金沢市の犀川と浅野川に挟まれた領域全ての建物マッピングをしています。


# 10_マッピング活動

## 2026-05-23 21:57
sava_god

qgisやflo-2dでの洪水、氾濫シュミレーションに必要なため作成しています。


# 10_マッピング活動

## 2026-05-23 21:59
k.sakanoshita

あー。なるほど。ここはマッピングのしがいがありますね（金沢のど真ん中）。


# 10_マッピング活動

## 2026-05-23 22:00
k.sakanoshita

金沢駅の辺りは再開発していて、航空写真や地理院地図の更新が間に合っていないので、既に書かれている場所を修整する際は慎重（明らかに古いと分かる場所に絞る）にマッピング頂けるとありがたく


# 10_マッピング活動

## 2026-05-23 22:02
sava_god

一応グーグルマップとの２画面で確認しながら作業していますが、参照先のおすすめなどはありますでしょうか？


# 10_マッピング活動

## 2026-05-23 22:03
k.sakanoshita

ええと、Google Mapsの参照はしないようにお願いします。これはGoogle Mapsをコピーしていると判断されるのを避けるためです。


# 10_マッピング活動

## 2026-05-23 22:04
sava_god

おすすめの航空写真などはありますか


# 10_マッピング活動

## 2026-05-23 22:04
qing_06282

ベースは国土地理院 全国最新写真(シームレス)
- Mapbox衛星画像
- Bing Maps Aerial
- Esri World Imagery
がシームレスより最新の場合があるので、
経年変化（住宅・ミニ団地やソーラーパネルなど）を見つけて採用してます
ただし、3つの航空写真は要位置修正です


# 10_マッピング活動

## 2026-05-23 22:11
sava_god

参考にさせていただきます。


# 10_マッピング活動

## 2026-05-23 22:13
qing_06282

調べたところ、金沢市は
地理院: 2007
https://maps.gsi.go.jp/#14/36.572527/136.655159/&base=std&ls=std%7Cgsi-compare-photo&blend=0&disp=11&lcd=gsi-compare-photo&vs=c1g1j0h0k0l0u0t0z0r0s0m0f1&d=m
Esri: 2026-02-26
https://livingatlas.arcgis.com/wayback/#mapCenter=136.64484%2C36.57928%2C15&mode=explore&active=64001


# 10_マッピング活動

## 2026-05-23 22:19
wish.f

最近のサーベイとの比較での体感ですが、
金沢周辺はMapbox衛星画像が最新だと思います
ご参考まで


# 10_マッピング活動

## 2026-05-23 22:27
nmaruichi0129

昔は、160〜200kmのサイクリング年に数度はやって居たんですけど。(200kmは過去一回のみ)
> 100km以下が短い距離とはー。サーベイし放題ですね。すごい。
100km以上のサイクリングを優先していると気になるところで止まってのサーベイが出来ません。
片道70kmで往復140kmぐらいになるしまなみ海道でサーベイしたのが最長かなって思って見てみると……。

下記の様に自転車通行可の歩道が、`highway=cycleway` にされていました。(自転車専用どうで無いのでまずいですね。 https://wiki.openstreetmap.org/wiki/JA:Japan_tagging)
https://www.openstreetmap.org/way/162654198 (来島海峡大橋)
https://www.openstreetmap.org/way/753252343 (伯方橋/大島大橋)
ただ、2年前に`highway=cycleway` に設定された方が、`highway=footway` に戻していた例もあったので、戻し忘れかな……。
私自身の編集内容でもあまり良くないのもあったので(すぐに取りかかる気力は無いので)いずれ直したいと思います。


# 10_マッピング活動

## 2026-05-23 22:33
sava_god

ドーナツ型の構造物はどのようにマッピングすればいいのでしょうか？


# 10_マッピング活動

## 2026-05-23 22:36
qing_06282

パッと説明できそうにないので...
https://learnosm.org/ja/beginner/id-editor/#マルチポリゴンの描き方
https://learnosm.org/ja/josm/josm-relations/#マルチポリゴンリレーションの作成


# 10_マッピング活動

## 2026-05-23 22:51
sava_god

出来ました、ありがとうございます


# 10_マッピング活動

## 2026-05-23 23:34
k.sakanoshita

とりあえず、金沢の海側をマッピング！


# 10_マッピング活動

## 2026-05-23 23:36
nyampire3568

マッピングではないですが、Rapid Plateauの対象都市が、どのくらいの建物投入率なのか、を、一覧化できるダッシュボードを作ろうとしています。
他にもつくりたいものあるのだけど、こう、OSMFJの事務作業しろ、という冷静な声も脳内にあり、はい。


# 10_マッピング活動

## 2026-05-23 23:37
nyampire3568

こう、Githubの草表示みたいなかんじで、自分がどれだけ今週・今月に、何をマッピングして何をがんばったか、サマリして褒めてくれるメールを送る、みたいな要約サービスがほしいんですよね。
みんながんばってるんだから、褒められるべきじゃん。


# 10_マッピング活動

## 2026-05-24 00:04
qing_06282

天文館は俺の技量じゃサーベイ、マッピングできない...


# 10_マッピング活動

## 2026-05-24 00:08
gray27

日本国内の`addr`タグを`addr:*`に分解し終わりました


# 10_マッピング活動

## 2026-05-24 00:24
wish.f

本日の成果です
うめきたの森も少しずつ様子が見えて、新梅田シティの一部も道路工事で用地が削られて、全体の完成が近づいてきてますね。


# 10_マッピング活動

## 2026-05-24 02:21
nmaruichi0129

今回の成果
公園を主に描いたつもりでしたが、あまり進みませんでした。
その要因として、しまなみ海道サイクリングロードの歩道が自転車道になっている問題を書いたことと、もう一つの原因あり。
もう一つの原因は、私の地元の廿日市市の女子野球チームの野球場を追加したことです。
なせか広島市にあります。(理由は推測でききるんけど……。)


# 10_マッピング活動

## 2026-05-24 09:51
alt9800

アーケードマッピングむずいですよね〜！

お隣の熊本でもCode forのひとびとが頑張ってるんですけどなかなか進んでないみたいです


# 10_マッピング活動

## 2026-05-24 12:04
qing_06282

難しいですねー。
人混みの多さ、店舗・POI)の数に加えて、サービス内容に応じたタグ付けや位置合わせなど、様々な要素が絡んできますね。
人を集めて、通りやブロック単位に分けたり、テーマを決める（飲食店Onlyや娯楽施設Onlyなど）など、企画して進めるのも面白いかもしれませんが、それでもかなりの長期戦になりそうですね。


# 10_マッピング活動

## 2026-05-24 12:06
hokkosha

おはようございます。昨晩は安定の寝落ちでした💤 
昨日限定ではなく1週間分のスクショですが、沖縄北中城村の森林をかなり描き足しました。今日は沖縄市方向にも少し進出しています。
沖縄本島は一般の居住エリアの密集度が激しくて、米軍基地エリアの贅沢な土地の使い方とは対照的ですが、私が普段描いてる北海道は米軍寄りの密度なので、沖縄の住宅地の建物マッピングに手を出す気力が湧かない…


# 10_マッピング活動

## 2026-05-24 14:46
gray27

うーん？集合体か？

`addr:full`がインポートされている長野県佐久市を久々に。正規表現をアップデートしたのでLevel0編集が捗っています


# 10_マッピング活動

## 2026-05-24 18:26
gray27

もう１波やった


# 10_マッピング活動

## 2026-05-24 18:35
gray27

OverpassTurbo→Level0→サクラエディタ→Level0→OSM でガツガツやってます


# 10_マッピング活動

## 2026-05-24 18:37
gray27

`addr:housenumber`だけレンダリングされるのはstreet文化圏だといいんだろうけど、`123番地45号`みたいな場合は`123-45`って出ると嬉しいかも と思う 1号 祭り


# 10_マッピング活動

## 2026-05-24 22:16
nononoexe

久しぶりにマッピングしました。今回は金沢駅の西側の建物をマッピング


# 10_マッピング活動

## 2026-05-25 00:38
k.sakanoshita

そういえば、未返答の問い合わせが2件ほどありましたねー。


# 10_マッピング活動

## 2026-05-25 00:39
k.sakanoshita

お疲れ様でした！天文館って、そんなにややこしいんですか（よく知らない）。


# 10_マッピング活動

## 2026-05-25 00:40
k.sakanoshita

お疲れ様でした！日本国内ってのが大きなスケールですね。すごい。


# 10_マッピング活動

## 2026-05-25 00:41
k.sakanoshita

お疲れ様でした！そういった所から、様々な問題が見えてくるかも知れませんね。マッピング進めたい所です。


# 10_マッピング活動

## 2026-05-25 00:42
k.sakanoshita

お疲れ様でした！金沢ありがたやー。まだまだ全然なエリアなので、充実させていきたいところです。


# 10_マッピング活動

## 2026-05-27 03:27
gray27

おはようございﾏｯﾋﾟﾝ
国分寺駅北口を進めました with RapiDPlateau


# 10_マッピング活動

## 2026-05-27 22:25
gray27

住宅地をRapiD-Praleauで繋げた。細かな住宅が多い


# 10_マッピング活動

## 2026-05-27 22:42
gray27

線路側の未プロットが気になってしまったので埋めてきました


# 10_マッピング活動

## 2026-05-27 23:35
gray27

今日はもうこれのケアはしない！沼すぎる！


# 10_マッピング活動

## 2026-05-27 23:42
gray27

これも積み残し～
府中市＊＊町 をcityにしちゃってる
だいたい ＊＊町N丁目。


# 10_マッピング活動

## 2026-05-28 07:42
naminami_t

うへー、
何故かこの辺だけ過去に住所を書いたんですが

https://www.openstreetmap.org/?#map=19/34.675348/135.768936

このやり方でOKですか？


# 10_マッピング活動

## 2026-05-28 07:44
gray27

https://www.openstreetmap.org/node/2462801283 私はこのNodeに合わせて漢数字「一丁目」にしたくなりますが、housenumberに枝番が入るの含めて見た感じ問題なさそうな入力ですね◎


# 10_マッピング活動

## 2026-05-28 17:35
gray27

`addr:street`を1つ消しに来たらすごいものを見てしまった


# 10_マッピング活動

## 2026-05-28 23:07
wish.f

週末に旅行で降り立った駅の駅前に建物がほとんどなかったので、少しずつ描き足し。
駅をマッピングするとstop_areaリレーションを設定すると警告で躓き……(wikiの記述もこのあたりまでカバーできるといいんだけども)
ともあれ、通ったところに地図ができてくのが楽しいわけで。


# 10_マッピング活動

## 2026-05-28 23:22
wish.f

アーケードマッピング、時間はかかりますが、やってみるとハマりますよ
（クエリの書き方勘違いしてやっと出せたので）


# 10_マッピング活動

## 2026-05-28 23:22
wish.f

元の状態を残しておけばよかったと後悔


# 10_マッピング活動

## 2026-05-28 23:24
wish.f

ライフサイクルが短い店も増えているので、フォローアップが課題ですね


# 10_マッピング活動

## 2026-05-29 01:58
gray27

住所タグを触り続けています


# 10_マッピング活動

## 2026-05-29 09:42
gray27

だいぶ都内の`addr:street`が片付いてきたなぁ


# 10_マッピング活動

## 2026-05-30 15:49
alt9800

住所設定の便利帳、海外の方や初心者の方も増えて来たのでどこかにまとめたいですね
住所録を打ち込むとOSMに適した形にしてくれるパーサなどあるといいのかも(すでにあったりしますかね？)


# 10_マッピング活動

## 2026-05-30 16:15
alt9800

そういえば昨日迷ったドメスティックな地物として、「着物の着付け教室」というものがありました。
iDエディター上では「カルチャーセンター」でもないし、「道場」でもないし、なんか習い事の教室として便利なタグがあるといいな〜と思いました。


# 10_マッピング活動

## 2026-05-30 16:16
alt9800

九工大戸畑キャンパス周辺を拡充中、北九州は区によっては公的に照会したっぽい「市道〇〇号」のようなデータを整備してある道路も見かける一方で戸畑区はそもそも道路が書かれていないような場所も住宅街に置いて散見されます。頑張って書くぞ〜


# 10_マッピング活動

## 2026-05-30 18:45
gray27

https://discord.com/channels/1280891177020686347/1386969584166506546/1399218578485542974
割と最近(?)整備したので、まぁ…
パーサーはデジタル庁がなんか頑張ってなかったっけ、あれは標準を提供するだけだっけ


# 10_マッピング活動

## 2026-05-30 20:06
wish.f

「着物の着付け教室」
`amenity=training` で `training=fashion`
とかですかね...。
(どこかでマッピングした気がするけど見つけられませんでした)
https://wiki.openstreetmap.org/wiki/JA:Tag:amenity%3Dtraining


# 10_マッピング活動

## 2026-05-30 20:09
tom_konda

ドメスティックな習い事でいうと、書道教室のタグもそうですね。
カリグラフィーの文脈から有りそうなのですが、見つけられず。


# 10_マッピング活動

## 2026-05-30 20:09
wish.f

`training=kimono` でも10か所あるようです。


# 10_マッピング活動

## 2026-05-30 20:11
wish.f

`training=calligraphy`が浜松に31か所、豊川市に2か所ありました…
`training=*` が浜松には多いようで、kimonoも9か所浜松に。


# 10_マッピング活動

## 2026-05-30 20:13
alt9800

標準化されてないけど、データ上見分けがつくようにマッピングするといいのですね、なるほど


# 10_マッピング活動

## 2026-05-30 20:14
alt9800

むむむ、nameに入れてある...


# 10_マッピング活動

## 2026-05-30 20:15
wish.f

`training=fashion` は日本にはなかったです笑
とはいえ、1か所しかついてない`training=*`もかなり多いので、できれば整えたいところですね。


# 10_マッピング活動

## 2026-05-30 20:59
k.sakanoshita

【MappyHourにご参加されるみなさまへ】
MappyHourは、みんなでOpenStreetMapを描いていくイベントです。

近所でも旅先でも、興味が湧いた場所から気楽に描いていきましょう。
まずは、このチャットに「何処を描きたいか」を投稿してみましょう。
大まかな都市名や駅名でOK。描きたいものがあればそれも合わせて！
地図の描き方が分からない人は、以下のサイトを読んでみてください。
それでも分からなければチャットで質問ください。早めに返答します。

LearnOSM（はじめてからのOpenStreetMapガイド）
https://learnosm.org/ja/beginner/

地図を描いている時（マッピング中）、どう描けば良いか分からない
ものが見つかったら、チャットで描き方を一緒に考えていきましょう。
もちろん、描いている時に気が付いたこと、面白い地物などがあれば
どんどんチャットでネタを提供していきましょう。
そして、地図を描いた後は、チャットで成果発表してみませんか？
https://osm.org で描いた辺りを表示して、URLをチャットに書けば
何処をマッピングしたのか、みんなに伝えることが出来ます。
※画面キャプチャを貼り付けるのも良いですねー（Copyright付けてね）
そうそう、地図を保存する時のコメントに「#MappyHourJapan」を
追記したら、以下のサイトのHashtagsランキングに掲載されるかも？

https://osmstats.neis-one.org/

それでは、みなさん楽しくいきましょう。


# 10_マッピング活動

## 2026-05-30 21:04
alt9800

福岡県南で仕事で訪れた場所をマッピングしています。主要駅周辺でも道路がぐにゃ〜〜となっていたり...修正中です @久留米市田主丸


# 10_マッピング活動

## 2026-05-30 21:10
k.sakanoshita

お疲れ様です！これはやりがいありますねー。よろしくお願いします！


# 10_マッピング活動

## 2026-05-30 22:13
nmaruichi0129

こんばんは、
本日も70km(69.1km)弱サイクリングしましたが、今回はサーベイ目的ではなく一部のセンサー(心拍とケイデンス)に問題があったのでガーミンストアにいきました。
まさか在庫があるとは思っていませんでした。
公開GPSトレースのファイルに記録されていると思いますが、地図には関係ありません。
その他、安全にサイクリング(サーベイ)するためにボトルをもう一本つけたくてボトルケージを買いました。

先週、報告していたしまなみ海道サイクリングロードの問題は愛媛県側は修正しておきました。
本日は、しまなみ海道サイクリングロードの広島分で気になる部分の修正をしたいと思います。


# 10_マッピング活動

## 2026-05-30 22:19
hokkosha

こんばんは。今日は広島県呉市に来ていますが、中心部は店などのマッピング率が高く、今更初見の観光客に等しい私がマッピングできるようなものがなし。
ということで、別に行く予定も何もないのですが、情島（なさけじま）という離島の建物がマッピングされてなかったので追加してみました。


# 10_マッピング活動

## 2026-05-30 22:22
k.sakanoshita

お疲れ様です。在庫があるのは良かったですね。取り寄せだと何日掛かるか気になりますし。


# 10_マッピング活動

## 2026-05-30 22:24
k.sakanoshita

お疲れ様です。呉ですかー。行きたい街だなぁ。楽しんでください！
あれ、情島って二つあるんですかね。
https://www.openstreetmap.org/way/131159704#map=16/34.16171/132.57476


# 10_マッピング活動

## 2026-05-31 00:02
tom_konda

今晩は、本日も相模大塚駅の北のエリアの建物形状の修正を進めようと思います。


# 10_マッピング活動

## 2026-05-31 01:08
tom_konda

本日の成果です。1ブロックの一部のみ形状修正しました 🏘️ 
https://www.openstreetmap.org/changeset/183406736


# 10_マッピング活動

## 2026-05-31 01:09
wish.f

こんばんは
引き続き各務原市で建物のトレースなどやってました。
解像度が高い画像があればなぁ。


# 10_マッピング活動

## 2026-05-31 01:09
nmaruichi0129

今回は、しまなみ海道サイクリングロードでは自転車専用道の標識は見てないので `highway=cycleway` や `bicyle=designated` を除去しました。
あと先週編集していた所に公園を追加しました.


# 10_マッピング活動

## 2026-05-31 01:10
k.sakanoshita

お疲れ様でした！建物の形が詳細になるのは楽しくなりますね。


# 10_マッピング活動

## 2026-05-31 01:10
k.sakanoshita

お疲れ様でした！ボケボケな航空写真だとマッピング厳しいですしね。


# 10_マッピング活動

## 2026-05-31 01:11
k.sakanoshita

お疲れ様でした！おー。公園ありがたい。サイクリングロードだけど自転車専用の標識は無いって不思議な気もしますね（そんなものなのかな）


# 10_マッピング活動

## 2026-05-31 01:12
k.sakanoshita

今日の昼間、明日の三国マッピングパーティに向けての準備（建物などの詳細化、更新など）してました。


# 10_マッピング活動

## 2026-05-31 15:01
alt9800

引き続きガリガリ書いているのですが、過去、矩形化機能が知られてなかったが故にポリゴンが大きくズレてたりするのをみると、エディタの設計って大事だな〜、ノウハウを多くの人が共有してくれると嬉しいな〜って思いますね。


# 10_マッピング活動

## 2026-05-31 15:01
alt9800

先人の頑張りをいい感じに修正できた時が一番嬉しいかもしれない


# 10_マッピング活動

## 2026-05-31 22:53
wish.f

今日の三国のマッピングパーティーのフォローで、
商店街ひとつ埋めきった...



---

# 20_開発・翻訳関連

## 2026-05-01 17:24
k.sakanoshita

OSMで音声ナビ案内（付近のamenity+shopを検索して道順案内）するWebサイトをテスト的に作ってみました。
https://armd-01.sakura.ne.jp/bird/


# 20_開発・翻訳関連

## 2026-05-01 17:24
k.sakanoshita

お手数ですが、みなさんのスマホでも一応動くかご確認いただいて、その結果を教えて頂けると幸いです。


# 20_開発・翻訳関連

## 2026-05-02 18:27
yohei4912

Pixel 6(Android16)とNothing Phone 3a(Android15)で検索＆音声案内問題なしです☺️


# 20_開発・翻訳関連

## 2026-05-02 18:27
k.sakanoshita

ありがとう！


# 20_開発・翻訳関連

## 2026-05-02 19:59
wish.f

検索＆音声案内できてます！
面白いですね


# 20_開発・翻訳関連

## 2026-05-03 22:19
btm.smellman

https://openstreetmap-japan.github.io/ だいたい出来てきた。


# 20_開発・翻訳関連

## 2026-05-05 04:48
btm.smellman

実装完了しました。og:imageなどへの対応もしています。
問題無ければopenstreetmap.jpを差し替えます。
セキュリティ的に落としたいので...


# 20_開発・翻訳関連

## 2026-05-05 10:06
k.sakanoshita

ご対応ありがとうございます。まずは一旦差し替えて頂けたらと。よろしくお願いします。


# 20_開発・翻訳関連

## 2026-05-05 16:54
btm.smellman

では、今晩差し替えてみます。


# 20_開発・翻訳関連

## 2026-05-05 21:32
btm.smellman

差し替えました。


# 20_開発・翻訳関連

## 2026-05-07 22:52
hiroshimiura.

weeklyOSMの協力者募集します。
翻訳だけでなく、日本発でもっと記事を打ち出していきたい！


# 20_開発・翻訳関連

## 2026-05-17 07:18
gray27

`https://tile.openstreetmap.jp/styles/openmaptiles#4.46/35.7/141.45`へのリンクがあるとJPサイトっぽくていいのかな、って思った


# 20_開発・翻訳関連

## 2026-05-18 16:30
btm.smellman

リンクだけで良いかな。あと、どこらへんにリンクがあると良いかな？


# 20_開発・翻訳関連

## 2026-05-18 22:32
gray27

一案として


# 20_開発・翻訳関連

## 2026-05-18 23:06
btm.smellman

おお、よさげ。入れて置きますね。ちなみにPR送ってもOKですし、openstreetmap-japanの方で管理者も募集してるので、良かったら管理者になりますか？w


# 20_開発・翻訳関連

## 2026-05-18 23:12
gray27

メンテナーにはなってもいいですが管理者・ω・；


# 20_開発・翻訳関連

## 2026-05-18 23:14
gray27

me https://github.com/graycat27


# 20_開発・翻訳関連

## 2026-05-18 23:21
btm.smellman

inviteしました。


# 20_開発・翻訳関連

## 2026-05-18 23:23
gray27

joined


# 20_開発・翻訳関連

## 2026-05-19 15:40
btm.smellman

サイドメニュー作りました


# 20_開発・翻訳関連

## 2026-05-27 09:38
btm.smellman

https://smellman.hatenablog.com/entry/2026/05/27/084825 OpenMapTilesでルーティングするというすげーライブラリが出てきたので日本のタイルサーバで試したって話を書きました。



---


---


---

# OSMJP定例会

## 2026-05-02 20:23
k.sakanoshita

https://discord.com/channels/1280891177020686347/1490184006912704632


# OSMJP定例会

## 2026-05-02 20:27
k.sakanoshita

https://civictechforum.jp/


# OSMJP定例会

## 2026-05-02 20:47
hayashi9934

ヘッドホン用意します



---


---


---


---

