# 準備

## 以下のデータベースを作成せよ

```

CREATE DATABASE game_app
DEFAULT CHARACTER SET utf8
```

## 以下の２つのテーブルを作成せし、初期データを挿入せよ

### gamehard

```
CREATE TABLE game_hard (
  id int(11) PRIMARY KEY AUTO_INCREMENT,
  機種名 varchar(20) NOT NULL,
  開発元 varchar(20) NOT NULL
);

INSERT INTO game_hard (id,機種名,開発元)
VALUES
(1,'3DS','任天堂'),
(2,'Switch','任天堂'),
(3,'PSVita','Sony'),
(4,'PS4','Sony'),
(5,'Xbox One','マイクロソフト');
```

### game_soft

```
CREATE TABLE game_soft (
  id int(11) PRIMARY KEY AUTO_INCREMENT,
  title varchar(255) NOT NULL,
  genre varchar(255) NOT NULL,
  released date,
  hard_id int(11),
  price int(11)
);

INSERT INTO game_soft (id,title,genre,released,hard_id,price)
VALUES
(1,'New スーパーマリオブラザーズ2','アクション','2012-07-28',1,4571),
(2,'ポケットモンスター サン・ムーン','RPG','2016-11-18',1,5478),
(3,'リズム天国 ザ・ベスト＋','リズムゲーム','2015-06-11',1,4700),

(4,'あつまれ どうぶつの森','コミュニケーションゲーム','2020-03-20',2,5980),
(5,'ゼルダの伝説 ブレス オブ ザ ワイルド','アクションアドベンチャー','2017-03-03',2,6980),
(6,'ポケットモンスター ソード・シールド','RPG','2019-11-15',2,6578),

(7,'太鼓の達人 Vバージョン','リズムゲーム','2015-07-09',3,5960),
(8,'テラリア','アクションアドベンチャー','2014-02-06',3,2838),
(9,'地球防衛軍3 PORTABLE','3Dアクション シューティング','2012-09-27',3,5800),

(10,'ゴッド・オブ・ウォー','アクションアドベンチャー','2018-04-20',4,2189),
(11,'Ghost of Tsushima','ステルスゲーム','2020-07-17',4,6900),
(12,'グランツーリスモＳＰＯＲＴ','レースゲーム','2017-10-19',4,6900),

(13,'ウィッチャー３ ワイルドハント','アクションアドベンチャー RPG','2015-05-21',5,6036),
(14,'Sonic Mania','アクションアドベンチャー','2017-08-15',5,1944);

INSERT INTO game_soft (id,title,genre,hard_id,price)
VALUES(15,'Cuphead','シューティング アクション',5,2350);
```

## 以下の問に答えよ(20問)

1.game_softのreleasedがNULLのデータを抽出せよ

2.問1で抽出したデータのreleasedのNULLを'2017-09-29'へ変更せよ

3.game_softのreleasedがNULLではないデータを抽出せよ

4.game_hardの開発元が任天堂のデータを抽出せよ

5.game_hardの開発元がソニーではないデータを抽出せよ

.'genre','released'を'ジャンル','発売日'と表示させて抽出せよ

.game_softのpriceが5000以上のデータを抽出せよ 取得項目はtitleとpriceとする

.priceの値が最も大きいデータを抽出せよ 取得項目はtitleとする

.game_softをreleasedの昇順で並び替えよ

.releasedが'2016-01-01'より前のデータのpriceを半額にせよ

.genreの種類一覧を抽出せよ

.genreにて'アクション'が含まれているデータを抽出せよ

.機種名毎に、使用できるソフトのpriceの合計を表示せよ 取得項目は機種名とsum(price)とする

.機種名毎に、使用できるソフトのpriceの平均を表示せよ 取得項目は機種名とavg(price)とする

.機種名が3DSで使用できるgame_softのデータを抽出せよ

.titleの文字数を表示せよ

.priceの合計額を、3桁毎に[,]をいれて表示せよ

.titleがCupheadのデータを、Switchで使用できるソフトとして変更せよ

.game_softに タイトル:Horizon Zero Dawn,発売日:2017-03-02,hard_id:4 のデータを挿入せよ

.開発元がSonyの機種で使用できるgame_softのデータを削除せよ
