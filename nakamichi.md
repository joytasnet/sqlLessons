# 準備

## 以下のデータベースを作成せよ

```

CREATE DATABASE sales_management
DEFAULT CHARACTER SET utf8
```

## 以下の２つのテーブルを作成せし、初期データを挿入せよ

### client

```
CREATE TABLE `client` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
	`name` VARCHAR(30) NOT NULL,
  `business_format` varchar(20) DEFAULT NULL,
	`peace_price` int(2) DEFAULT NULL,
	`total_sales` int(11) DEFAULT NULL
);

INSERT INTO `client`
VALUES
(1,'ビックカメラ','家電',4,20000000),
(2,'ピーコックストア','SM',1,NULL),
(3,'サンドラッグ','DS',2,NULL),
(4,'イトーヨーカドー','GMS',2,NULL),
(5,'ファミリーマート','CVS',7,NULL),
(6,'VIVA_HOME','HS',3,NULL);

```

### store

```
CREATE TABLE `store` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `name` varchar(255) NOT NULL,
  `client_id` int(11) DEFAULT NULL,
  `peaces` int(11) DEFAULT NULL,
	`day` DATE NOT NULL
);

INSERT INTO `store`
VALUES
(1, '有楽町', 1, 1200000,'2020-08-27'),
(2, '新宿西口小田急百貨店', 1, 900000,'2020-08-12'),
(3, '新宿東口', 5, 12000,'2020-10-12'),
(4, '新宿東口', 3, 40000,'2020-10-12'),
(5, '中野坂上', 2, 80000,'2020-09-06'),
(6, '用賀', 2, 110000,'2020-09-11'),
(7, '東府中', 3, 80000,'2020-10-04'),
(8, '昭島昭和',3, 300000,'2020-10-11'),
(9, '国領',4,2100000,'2020-07-21'),
(10,'有楽町',5,13000,'2020-06-21'),
(11,'志木',6,2400000,'2020-08-22')
;

```

### market
```
CREATE TABLE `market` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `store_place` varchar(255) NOT NULL,
  `client_id` int(11) DEFAULT NULL,
  `peaces` int(11) DEFAULT NULL,
	`day` DATE NOT NULL
);

INSERT INTO `market`
VALUES
(1, '有楽町', 1, 1200000,'2020-08-27'),
(2, '新宿西口小田急百貨店', 1, 900000,'2020-08-12'),
(3, '新宿東口', 5, 12000,'2020-10-12'),
(4, '新宿東口', 3, 40000,'2020-10-12'),
(5, '中野坂上', 2, 80000,'2020-09-06'),
(6, '用賀', 2, 110000,'2020-09-11'),
(7, '東府中', 3, 80000,'2020-10-04'),
(8, '昭島昭和',3, 300000,'2020-10-11'),
(9, '国領',4,2100000,'2020-07-21'),
(10,'有楽町',5,13000,'2020-06-21'),
(11,'志木',6,2400000,'2020-08-22')
;
```

## 以下の問に答えよ(20問)

1. marketテーブルを誤って作ってしまったため削除せよ。

1. 下記のデータを挿入せよ。  
(池袋西口,1,2200000,2020-08-07)
(六本木,5,13000,2020-11-12)
(新線新宿,5,7000,2020-07-12)

1. clientの内容を全て抽出せよ。

1. clientの中の新宿を含むデータの個数(peaces)を全て1000個増やせ。

1. storeテーブル内の8月~12月の取引を抽出し、peacesの数で降順ソートせよ。

1. storeテーブル内のnameカラムに宿が含まれる件数を抽出せよ。

1. storeテーブル内のpeacesの平均値を出せ。

1. storeテーブル内のclient_id3の個数(peaces)の平均値を抽出せよ。

1. storeテーブル内のclient_id毎の個数(peaces)の合計を求め、300000~3000000の間の項目を抽出せよ。

1. storeテーブル内のday(実施日)が古い順に3件表示せよ。ただし一番古いものは除く。

1. storeテーブル内の個数(peaces)が最小のレコードをpeacesを777に変更せよ。

1. storeテーブル内の個数(peaces)が777のレコードを削除してください。

1. clientテーブルのtotal_salesを売上合計と表示せよ。

1. clientテーブルとstoreテーブルをLEFT JOINし(client.nameがidの横に来るようにしてください)、id順にソートして表示せよ。

1. clientテーブルのビックカメラ(id=1)のtotal_salesの値をstore内のclient_idの合計に置き換えよ。

1. clientテーブルのidが2~6までの項目のtotal_salesの値をstoreのclient_id毎の合計に置き換えよ。(CASE文で置き換えしてください)

1. clientテーブルを全権抽出し、total_salesの大きい順に表示してください。

1. clientテーブルのpeace_priceとstoreテーブルのpeacesを用いて8月の売上の合計を求めよ。(求めたカラムの表示名は8月売上合計にすること)

1. clientテーブルのtotal_salesの平均値を求めよ。

1. client テーブルのtotal_salesの合計値を求め、カラム名を第四四半期売上高として表示せよ。


