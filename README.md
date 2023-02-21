テレビ番組表の記録(2023年分)
==

概要
--

日本全国のテレビ番組表１年分をどれだけ小さな容量でアーカイブできるか実験をおこなうプロジェクトです。  
なおかつ、まとまったデータを欲しい人が大量にHTTPリクエストを投げなくても済むようなアーカイブ作成も目的としています。  
`timetable.yanbe.net` の代替コンテンツとして、2023年分についても独自に記録をつける事にしました。  
2023年分の集計は終わりましたが、データの修正をおこなう場合もあります。

* [2024年分はこちら](https://github.com/head-jockaa/timetable2024)

使い方
--

`https://github.com/head-jockaa/timetable2023` のページにある緑色の `Code` ボタンを押して `Download ZIP` を選んでください。  
ダウンロードされたZIPファイルを展開して `2023.html` をブラウザで開けばOKです。  
`scripts` フォルダの中にある圧縮ファイル `archive.7z` を展開すると、たぶん `archive` というフォルダができるので、その中にjsファイルを配置するようにします。  
7-Zip形式に対応した解凍ソフトを使ってください。

* `scripts/archive/encoder.js`
* `scripts/archive/timetables.js`
* `scripts/archive/titles.js`
* `scripts/archive/descriptions.js`
* `scripts/archive/radio_encoder.js`
* `scripts/archive/radio_timetables.js`
* `scripts/archive/radio_titles.js`
* `scripts/archive/radio_descriptions.js`

データ収集対象
--

* 全都道府県の地上波テレビ、BSデジタルテレビ
  * 普段から独自編成しているマルチチャンネルはできるだけ対象とする（NHK総合、NHKEテレ、TOKYOMX、TVK、チバテレ、群馬テレビ、三重テレビ、サンテレビ、NHK-BS1、BS日テレ、BS-TBS、BSフジ、BSテレ東、放送大学）
  * CS放送の番組表については検討中だが、どちらかというと、あんまりやりたくない
  * インターネット放送は対象外
* タイムテーブルを形作る上で最低限必要な要素
  * 開始時刻、放映時間、ジャンル、各種アイコン、番組名、番組概要を記録する
  * 🙇‍♀️出演者等の詳細な記事情報については、負担が大きい事と目的にそぐわない事から対象外とさせて下さい🙇‍♂️

※ 緊急報道特番はTwitterの書き込みからの再現を試みていますが、必ずしも正確ではありません  
※ ニュース番組概要など番組表の変更を考慮して、当日深夜に取得  
※ おまけでラジオ放送の記録もおこなう

2022年以前
--

* [2022年分](https://github.com/head-jockaa/timetable2022)
* [2021年分](https://github.com/head-jockaa/timetable2021)

2020年以前のデータは `timetable.yanbe.net` から吸い出した物です。  
恐る恐るアクセスしなくてはならず、全てのデータが揃うには3年掛かるかもしれません。

* [2007年分](https://github.com/head-jockaa/timetable2007)
* [2008年分](https://github.com/head-jockaa/timetable2008)
* [2009年分](https://github.com/head-jockaa/timetable2009)
* [2010年分](https://github.com/head-jockaa/timetable2010)
* [2011年分](https://github.com/head-jockaa/timetable2011)
* [2012年分](https://github.com/head-jockaa/timetable2012)
* [2013年分](https://github.com/head-jockaa/timetable2013)
* [2014年分](https://github.com/head-jockaa/timetable2014)
* [2015年分](https://github.com/head-jockaa/timetable2015)
* [2016年分](https://github.com/head-jockaa/timetable2016)
* [2017年分](https://github.com/head-jockaa/timetable2017)
* [2018年分](https://github.com/head-jockaa/timetable2018)
* [2019年分](https://github.com/head-jockaa/timetable2019)
* [2020年分](https://github.com/head-jockaa/timetable2020)

設計
--

* javascriptを利用し、番組表のデザインに自由度を与える。
* 辞書ファイルの用意、2バイト文字への変換、関東キー局との差分を求めることにより、データサイズをなるべく小さく抑える。 
  * 7zipの力も借りて、今の所20MB以下に抑えられる見込み。

作り方は2022年版をご覧ください。
