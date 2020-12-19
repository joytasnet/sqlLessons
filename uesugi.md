# 準備

## 以下のデータベースを作成せよ

```

CREATE DATABASE Station
DEFAULT CHARACTER SET utf8
```

## 以下の２つのテーブルを作成せし、初期データを挿入せよ

### Hinbiya_line

```
CREATE TABLE `Hibiya_line` (
  `id` varchar(3) PRIMARY KEY,
  `station` varchar(30) NOT NULL
);

INSERT INTO `Hibiya_line` (`id`, `station`)
VALUES
('H01','中目黒'),
('H02','恵比寿'),
('H03','広尾'),
('H04','六本木'),
('H05','神谷町'),
('H06','虎ノ門ヒルズ'),
('H07','霞ヶ関'),
('H08','日比谷'),
('H09','銀座'),
('H10','東銀座');
```

### Chiyoda_line

```
CREATE TABLE `Chiyoda_line` (
  `id` varchar(3) PRIMARY KEY,
  `station` varchar(30) NOT NULL
);

INSERT INTO `Chiyoda_line` (`id`, `station`)
VALUES
('C01','代々木上原'),
('C02','恵比寿'),
('C03','明治神宮前'),
('C04','表参道'),
('C05','乃木坂'),
('C06','赤坂'),
('C07','国会議事堂'),
('C08','霞ヶ関'),
('C09','日比谷'),
('C10','二重橋前');
```

## 以下の問に答えよ(5問)

1. Hibiya_lineに以下のデータを挿入せよ
  ('H11','築地')

2. よく見ると、日比谷線と千代田線では乗り換え可能な駅が二つある。
この二つの駅と、それぞれの番号を結びつけるテーブルを作成せよ。
ただし、以下の情報を用いること。
テーブル名：Stations
カラム名：station(varchar(30)),Hibiya_id(varchar(3)),Chiyoda_id(varchar(3))
※なお、stationはNOT NULL、それ以外はNULLを許可して良いものとする。

3. 国民の強い要望により、日比谷線の「虎ノ門ヒルズ」がダサいとして改名になった。
「虎ノ門ヒルズ」を、新しく「虎ノ門サンクチュアリ」にせよ。
(なお、私のネーミングセンスは問わないこと)

4. さらに勢いに乗った国民は、千代田線の「明治神宮前」を「神宮球場」に変えることにした。
Chiyoda_lineの「明治神宮前」を「神宮球場」に改名せよ。
(なお、「東京音頭」をyoutubeで調べるかは任意とする)

5. 贅沢なことに、先ほど改名した「虎ノ門サンクチュアリ」は銀座線の乗り換えができる。
同様に銀座線に乗り換えられる「銀座」と一緒に、Stationsに追加することにした。
以下の情報を用いてStationsテーブルにカラムとデータを追加せよ。
カラム名：Ginza_id(varchar(3))
カラムの追加方法：ALTER TABLEを用いる。(ALTER TABLEは調べてみよう)
データ1：虎ノ門サンクチュアリ,(Hibiya_id)H06,(Chiyoda_id)NULL,(Ginza_id)G07
データ2：銀座,(Hibiya_id)H09,(Chiyoda_id)NULL,(Ginza_id)G09
