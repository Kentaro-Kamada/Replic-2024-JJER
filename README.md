# Replic-2024-JJER

[鎌田（2024）](https://researchmap.jp/kamaken/published_papers/44513554)の再現コードです。

再現結果：https://kentaro-kamada.github.io/Replic-2024-JJER/

## 再現の方法

### `01_rawdata/生協調査`にデータを保存する

生データを格納するディレクトリです。再現の際は[SSJデータアーカイブ](https://csrda.iss.u-tokyo.ac.jp/)より該当するデータを申請し、以下に示すファイル名のファイルを`01_rawdata/生協調査`に保存してください。

使用データは以下の通りです。

- 0053.sav：[第29回学生生活実態調査，1993](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0053)
- 0078.sav：[第27回学生生活実態調査，1991](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0078)
- 0079.sav：[第28回学生生活実態調査，1992](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0079)
- 0080.sav：[第30回学生生活実態調査，1994](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0080)
- 0125.sav：[第31回学生生活実態調査，1995](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0125)
- 0126.sav：[第32回学生生活実態調査，1996](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0126)
- 0127.sav：[第33回学生生活実態調査，1997](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0127)
- 0128.sav：[第34回学生生活実態調査，1998](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0128)
- 0157.sav：[第35回学生生活実態調査，1999](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0157)
- 0201.sav：[第36回学生生活実態調査，2000](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0201)
- 0267.sav：[第37回学生生活実態調査，2001](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0267)
- 0292.sav：[第38回学生生活実態調査，2002](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0292)
- 0345.sav：[第39回学生生活実態調査，2003](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0345)
- 0399.sav：[第40回学生生活実態調査，2004](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0399)
- 0519.sav：[第41回学生生活実態調査，2005](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0519)
- 0562.sav：[第42回学生生活実態調査，2006](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0562)
- 0605.sav：[第43回学生生活実態調査，2007](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0605)
- 0664.sav：[第44回学生生活実態調査，2008](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0664)
- 0753.sav：[第45回学生生活実態調査，2009](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0753)
- 0812.sav：[第46回学生生活実態調査，2010](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0812)
- 0841.sav：[第47回学生生活実態調査，2011](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0841)
- 0879.sav：[第48回学生生活実態調査，2012](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0879)
- 0955.sav：[第49回学生生活実態調査，2013](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=0955)
- 1057.sav：[第50回学生生活実態調査，2014](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=1057)
- 1099.sav：[第51回学生生活実態調査，2015](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=1099)
- 1163.sav：[第52回学生生活実態調査，2016](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=1163)
- 1232.sav：[第53回学生生活実態調査，2017](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=1232)
- 1295.sav：[第54回学生生活実態調査，2018](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=1295)
- 1384.sav：[第55回学生生活実態調査，2019](https://ssjda.iss.u-tokyo.ac.jp/Direct/gaiyo.php?eid=1384)

### パッケージをインストール

本プロジェクトでは`renv`を用いてパッケージのバージョン管理を行っています。`renv`パッケージをダウンロードしたのち、`renv::restore`を用いてパッケージのインストールを行ってください。

```{r}
install.package('renv')
renv::restore()
```

### コードの実行

以下のコードを、この順番で実行してください。

1. `04_script/変数ラベル値ラベル作成.qmd`
1. `04_script/大学コード処理.qmd`
1. `04_script/データ前処理.qmd`

### 図表の再現

`05_教育学研究/本文.qmd`を実行することで、本文中の図表を再現することができます。

また、再現結果のページはこれをrenderしたものになります。

