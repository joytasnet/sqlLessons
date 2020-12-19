# 準備

## 以下のデータベースを作成せよ

```
CREATE DATABASE cafe_app
DEFAULT CHARACTER SET utf8;
```
## 以下の2つのテーブルを作成し、初期データを挿入せよ

### categories
```
CREATE TABLE categories(  
id INT(15) PRIMARY KEY AUTO_INCREMENT,  
category VARCHAR(10) NOT NULL  
);  

INSERT INTO categories (id,category)  
VALUES  
(1,'フード'),  
(2,'ドリンク'),  
(3,'デザート'),  
(4,'セット');  
```

### menu
```
CREATE TABLE menu(  
id INT(15) PRIMARY KEY AUTO_INCREMENT,  
name VARCHAR(30) NOT NULL,  
cat_id int(11) DEFAULT NULL,  
price int(11) DEFAULT NULL,  
stock VARCHAR(20) DEFAULT NULL
);  


INSERT INTO menu(id,name,cat_id,price,stock)  
VALUES  
(1,'トースト',1,300,'inStock'),
(2,'ピザトースト',1,700,'inStock'),
(3,'ドライカレー',1,1000,'inStock'),
(4,'コーヒー',2,500,'inStock'),
(5,'紅茶',2,500,'inStock'),
(6,'ケーキ',3,500,'inStock'),
(7,'プリン',3,500,'inStock'),
(8,'試作メニュー',NULL,NULL,NULL),
(9,'試作ドリンク',2,NULL,NULL),
(10,'試作デザート',3,NULL,NULL),
(11,'セット値引き',4,-100,'inStock');

CREATE TABLE stock_id(
id INT(15) PRIMARY KEY AUTO_INCREMENT,
name VARCHAR(30) DEFAULT NULL
);

INSERT INTO stock_id
(1,'inStock'),
(2,'limitedStock'),
(3,NULL);

```
## 以下の問いに答えよ

1.menuテーブルから、カテゴリーがセットでないものを抽出せよ

2.categoriesテーブルに、テイクアウトを追加せよ

3.menuテーブルに以下のものを追加せよ。カテゴリーはテイクアウト、在庫はinStockとする。
・持ち帰りコーヒー　400円
・持ち帰りサンドイッチ 700円
・持ち帰りケーキ 400円

4.categoriesテーブルに新しいカテゴリーをひとつ追加せよ。

5.試作メニューを考案し、名前、カテゴリー、値段、在庫の有無を設定せよ。

6.試作ドリンク、試作デザートも同様に考案し、項目を設定せよ。

7.好きな組み合わせでメニューを3つ選び、合計金額を抽出せよ。
なお、ドリンクとドリンク以外のメニューを同時に選んだ場合、セット値引きを適用すること。

8.menuテーブルの総数をカウントせよ。

9.すべてのメニューの平均値を抽出せよ。

10.メニューから値段が一番高い順に3つ抽出せよ。

11.任意の数のメニューを在庫切れ(NULL)にせよ。

12.任意の数のメニューを在庫わずか(limitedStock)にせよ。

13.在庫状況が違うものごとに、メニューの数をカウントせよ。

14.任意のメニューをひとつ選んで削除せよ。

15.デザートメニューを一律50円値上げせよ。

16.ドリンクメニューを2つ選び、名前にプレミアムをつけて200円値上げせよ。
在庫がない場合はNULLから変えること。

17.カテゴリーごとの値段の平均値をとり、一番安いカテゴリーを抽出せよ。

18.全てのメニューの値段のうち、8番目に安いものから高いものへ3種類抽出せよ。

19.全てのメニューの中から、500円以上700円以下のものを抽出せよ。

20.カラム(name,price,stock)を(名前、値段、在庫)と書き換えて抽出せよ。
