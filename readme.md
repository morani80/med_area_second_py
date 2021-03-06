
## 2次医療圏

## about
2次医療圏のデータを作成する。2次医療圏は医療計画が策定される単位なので、分析に利用することがある。

#### 参考

|医療圏の単位|note|
|---|---|
|1次医療圏|概ね市町村単位. 日常生活に密着した保健医療を提供する区域|
|2次医療圏|一般に複数の市区町村で構成. 健康増進・疾病予防から入院治療まで一般的な保健医療を提供する区域|
|3次医療圏|都道府県単位(北海道のみ、6つ). 先進的な技術を必要とする特殊な医療1に対応する区域|


## 2次医療圏コード(4digit)
もとにするデータは[政府統計データ](https://www.e-stat.go.jp/stat-search/)からCSVファイルの形でダウンロードできる。  
医療施設調査 x年医療施設（静態・動態）調査 > 表番号E1:病院数；病床数，病院－病床の種類・二次医療圏・市区町村別  
4桁が2次医療圏コード、5桁が市町村コードを表す。  

#### 参考
![厚生労働省の資料](howto_2ndarea.jpg)
出典:厚生労働省

## 処理
上記からダウンロードしたCSVを加工し、Outputのcsvファイルを作成する

## Output
{市町村コード(5digit), 市町村名, 2次医療圏コード(4digit), 2次医療圏名, 都道府県コード(2digit), 都道府県名}
のCSVファイル

(eg)
|市町村コード|市町村名|2次医療圏コード|2次医療圏名|都道府県番号|都道府県|
|---|---|---|---|---|---|
|01202|函館市|0101|南渡島|01|北海道|
|01236|北斗市|0101|南渡島|01|北海道|
|...|...|...|...|...|...|
