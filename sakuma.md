# 準備

## 以下のデータベースを作成せよ

```
CREATE DATABASE equipments_app
DEFAULT CHARACTER SET utf8;
```

## 以下の２つのテーブルを作成し、初期データを挿入せよ

### categories

```
CREATE TABLE `categories` (
  `id` int PRIMARY KEY AUTO_INCREMENT,
  `category` varchar(10) NOT NULL
);

INSERT INTO `categories` (`id`, `category`)
VALUES
(1, 'weapon'),
(2, 'protecter'),
(3, 'アクセサリー');
```

### equ

```
CREATE TABLE `equ` (
  `id` int PRIMARY KEY AUTO_INCREMENT,
  `name` varchar(10) NOT NULL,
  `cat_id` int(1) NOT NULL,
	`value` int(3) DEFAULT NULL,
  `b_price` int(5) DEFAULT NULL,
  `s_price` int(5) DEFAULT NULL
);

INSERT INTO equ(id,name,cat_id,value,b_price,s_price)
VALUES
(1,'果物ナイフ', 1,5,100,30),
(2,'アイアンソード',1,10,200,120),
(3,'皮の帽子',2,3,40,20),
(4,'クリスタルヘルム',2,50,3000,1500),
(5,'お鍋のフタ',2,4,100,50),
(6,'イージスの盾',2,4,100,50),
(7,'布の服',2,2,30,20),
(8,'ゴールドアーマー',2,30,4000,4000),
(9,'スライムピアス',3,5,500,250),
(10,'リボン',3,20,10000,1000);
```

## 以下の問に答えよ(20問)

1. categoriesテーブルのidの3categoryを「accesory」に変更せよ

1. categoriesテーブルのデータを取得せよ

1. categoriesテーブルから文字数が6のデータを抽出せよ

1. equテーブルに次のデータを追加せよ name:王者の剣 cat_id:1 value:100 b_price:30000 s_price:NULL

1. equテーブルをnameの昇順で表示せよ

1. equテーブルからb_priceの値が2番目から4番目に高いデータを抽出せよ

1. equテーブルからb_priceが3000以上のデータを抽出せよ

1. equテーブルからcat_idが2以外のデータを抽出せよ

1. equテーブルからcat_idが2でvalueが30以上のデータを抽出せよ

1. equテーブルからvalueが10未満もしくは20以上のデータを抽出せよ

1. equテーブルからvalueが10~30のデータを取得せよ

1. equテーブルのうち、valueが20以上のデータの件数を求めよ

1. equテーブルからnameに「イ」が含まれるデータのnameとcate_idを抽出せよ

1. equテーブルからnameを名前、b_priceを買値、s_priceを売値として抽出せよ

1. equテーブルからs_priceがb_priceの半分の値を超えるデータを抽出せよ

1. equテーブルからnameを名前として、s_priceからb_priceを引いた値を差額として取得せよ(NULLは除外すること)

1. equテーブルからnameを名前として、b_priceを価格として、cat_idの値に「階」を結合した文字列(例:1階)を売り場として取得せよ

1. equテーブルとcategoriesテーブルを結合し、name,category,valueを抽出し、cat_idの昇順、次いでvalueの降順で表示せよ

1. equテーブルとcategoriesテーブルを結合し、category名とcategory別のb_priceの平均(整数で表示)を昇順で表示せよ

1. equテーブルとcategoriesテーブルを結合し、category別のs_priceの合計を求め、求めた値が1000以上のcategory名とその値を表示せよ
