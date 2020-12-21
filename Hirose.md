##以下のデータベースを作成せよ
```
CREATE DATABASE
DEFAULT CHARACTER SET utf8
```
##以下の２つのテーブルを作成せし、初期データを挿入せよ
positions
```
CREATE TABLE positions(
	id int PRIMARY LEY AUTO_INCREMENT,
	position varchar(10) NOT NULL
);

INSERT INTO positions(id,position)
VALUES
(1,'捕手'),
(2,'内野手'),
(3,'外野手');
```
members
```
CREATE TABLE members(
	id int PRIMARY KEY AUTO_INCREMENT,
	name varchar(255) NOT NULL,
	cat_id int DEFAULT NULL,
	num int NOT NULL,
	ave double DEFAULT NULL
);

INSERT INTO members(name,cat_id,num,ave)
VALUES
('モヤ',2,1,0.274),
('安達',2,3,0.289),
('福田',2,4,0.258),
('宗',3,6,0.225),
('ジョーンズ',3,10,0.257),
('吉田',3,34,0.350),
('佐野',3,93,0.214),
('頓宮',1,44,0.313),
('岡田',2,55,0.256);
```
##以下の問に答えよ(20問)
1. membersテーブルからname,num,aveの一覧を取得する。各見出しは次のようにすること。&nbsp;&middot;名前 &middot;背番号 &middot;打率
1. membersテーブルからnumが一桁のデータを取得する。
1. membersテーブルからnameに&#34;田&#34;を含むデータをnumが昇順になるように取得する。
1. members テーブルからaveが0.25以上のname,aveの一覧を降順に取得する。っか生み出しは次のようにすること。&nbsp;&middot;名前&middot;打率
1. membersに以下の3つのデータを挿入せよ
name&#58;中川,若月,杉本
cat&#095;id&#58;2,1,3
num&#58;67,37,99
ave&#58;0.146,0.240,0.269
1. membersテーブルからpositionが&#34;内野手&#34;のデータについてname,num,aveの一覧を抽出する
1. idが7のmemberのnumを41に変更せよ
1. position毎のaveの平均を算出し、降順に抽出せよ
1. membersテーブルからaveが5番目に高いデータを抽出せよ
1. membersテーブルからnumが10以上50未満のデータを抽出せよ。ただし記述条件は一つであること
1. membersテーブルからpositionが&#34;捕手&#34;、&#34;内野手&#34;のいずれかであるデータを抽出せよ。ただし条件式は一つであること。
1. membersテーブルの中でnumが30番台で一番aveの高いデータを抽出せよ
1. membersテーブルの中でnameの文字数が2文字ではないデータを抽出せよ
1. membersの中で最も大きいnumの数字を抽出せよ
1. membersをposition毎に分類しそれぞれ最も大きいnumの数字を抽出せよ
1. membersの中で最もaveが低いデータを抽出せよ
1. membersテーブルの登録件数を抽出せよ
1. membersテーブルを&#34;name&#040;背番号&#58;num&#041;の打率はave&#34;という形式で抽出せよ&#040;例 モヤ&#040;背番号&#58;1&#041;の打率は0.274&#041;
1. membersテーブルからname,aveのデータを抽出し、aveが0.3以上であればgood、0.2以上0.3未満であればsoso、0.2未満であればbadと出力せよ。goodなど出力するカラムは&#34;評価&#34;とする。
1. membersテーブルとpositionテーブルをidとcat&#095;idで結合し、name,num,position,aveの一覧を抽出する。各見出しは以下のようにすること。&nbsp;&middot;名前 &middot;背番号 &middot;ポジション &middot;打率

