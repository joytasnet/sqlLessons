
# 準備

## 以下のデータベースを作成せよ

```

CREATE DATABASE zoo_app
DEFAULT CHARACTER SET utf8
```

## 以下の２つのテーブルを作成せし、初期データを挿入せよ

### foodhabit

```
CREATE TABLE `foodhabit` (
  `id` int(100) PRIMARY KEY AUTO_INCREMENT,
  `habit` VARCHAR(10) NOT NULL,
	);

INSERT INTO foodhabit
VALUES
(1,'肉食')
(2,'草食')
(3,'雑食')

```
### animals

```
CREATE TABLE `animals` (
  `id` int(100) PRIMARY KEY AUTO_INCREMENT,
	'class' VARCHAR(5) NOT NULL,
  `category` VARCHAR(10) NOT NULL,
	'name' VARCHAR(255) NOT NULL,
	'age' INT
	'food_id' INT
	);

INSERT INTO animals
VALUES
(1, '哺乳類','ライオン','猫モドキ',6,1),
(2, '爬虫類','ワニ','ラコステ',42,1),
(3, '爬虫類','ワニ','クロコダイル',35,1),
(4, '哺乳類','オオカミ','ルーピン',3,1),
(5, '鳥類','ペンギン','ビス',4,1),
(6, '肉食性','ピクミン','赤ピクミン',0,1) 
(7, '哺乳類','ゾウ','ぞう',12,2),
(8, '鳥類','ダチョウ','ウエシマ',56,2),
(9, '爬虫類','リクガメ','ガメラ',82,2),
(10, '哺乳類','チンチラ','けだま',1,2),
(11, '哺乳類','熊','くまもん',5,3),
(12, '哺乳類','チンパンジー','コメ君',18,3),
(13, '哺乳類','猿','ジョージ',7,3)
(14, '鳥類','フラミンゴ','ヨネヅ'29,3)
```

## 以下の問に答えよ(20問)

1. animalsに以下のデータを挿入せよ
		クラス:ポケモン.カテゴリー:NULL.名前:ピカチュウ.age:無.food_id:2

1. animalsからcategoryにピクが含まれている動物を削除せよ
  
1. animalsからclassが哺乳類のデータを抽出せよ
		
1. animals内のnameにコメが含まれるデータのnameをパン君に修正せよ

1. animals内の全てのデータを抽出せよ。

1. それぞれのテーブルでageの低い順にデータを抽出せよ

1. animals内のclassがポケモンのデータのcategoryをねずみポケモンにせよ

1. class毎の平均年齢(age)を求め降順に抽出せよ。取得カラムはclass,avg(age)とする

1. animalsのデータをageが低い順に抽出せよ。

1. animals内のcategoryが哺乳類でないデータを抽出せよ

1. animels内のnameにピンが含まれるデータのnameをルーピン先生にせよ

1. animals内のfood&#095idが1のデータを抽出せよ

1. habitが肉食と草食のどちらでもないanimalsの名称とfood&#095idを抽出せよ。

1. animals内のcategoryがワニのデータのageを1上げよ

1. animalsで主キーの役割を果たしている列名を答えよ

1. animals内のageの平均値を抽出せよ

1. animals内の同classの数が最も多いデータを出力せよ。取得カラムはclassとcategoryのみとする

1. animals内のcategoryがライオンのデータのnameを好きに変えよ

1. animals内のfood&#095idがfoodhabit内のidと一致するものを内部結合せよ

1. animals内のcategoryダチョウのデータを削除せよ

## お疲れ様です
