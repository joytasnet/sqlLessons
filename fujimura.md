# 準備

## 以下のデータベースを作成せよ

```

CREATE DATABASE dvd_app
DEFAULT CHARACTER SET utf8
```

## 以下の２つのテーブルを作成せし、初期データを挿入せよ

### categories

```
CREATE TABLE `categories` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `category` varchar(20) NOT NULL
);

INSERT INTO `categories` (`id`, `category`)
VALUES
(1, 'アクション'),
(2, 'サスペンス'),
(3, 'コメディ'),
(4, 'ホラー'),
(5, 'SF'),
(6, '恋愛'),
(7, 'アニメ');

```

### dvds

```
CREATE TABLE `dvd` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `title` varchar(255) NOT NULL,
  `cat_id` int(11) DEFAULT NULL,
  `starring` varchar(40) NOT NULL
);

INSERT INTO `dvd` (`id`, `title`, `cat_id`, `starring`)
VALUES
(1, 'ターミネーター:ニュー・フェイト', 5,'アーノルド・シュワルツェネッガー'),
(2, 'ぐらんぶる', 3,'竜星涼,犬飼貴丈'),
(3, '【初回仕様】ぐらんぶる DVD プレミアム・エディション', 3,'竜星涼,犬飼貴丈'),
(4, 'ハーレイ・クインの華麗なる覚醒', 1,'マーゴット・ロビー'),
(5, 'イップ・マン 完結', 1,'ドニー・イェン'),
(6, 'ランボー ラスト・ブラッド', 6,'シルベスター・スタローン'),
(7, 'ボヘミアン・ラプソディ北の大地', 6,'ラミ・マレック'),
(8, 'ファンタスティック・ビーストと黒い魔法使いの誕生', 5,'エディ・レッドメイン'),
(9, 'スター・ウォーズ/スカイウォーカーの夜明け(数量限定)', 5,'デイジー・リドリー'),
(10, 'フォードvsフェラーリ', 3,'マット・デイモン'),
(11, 'ジョーカー', 3,'ホアキン・フェニックス');


```

## 以下の問に答えよ(20問)

1. dvdに以下のデータを挿入せよ
  (12,'ドラえもん',7,ドラえもん')

2. categoriesが「恋愛」であるものを全て抽出せよ

3. categoriesが「アクション」である映画のtitleのみ抽出せよ

4. idが1－5の映画のstarringのみ抽出せよ

5. idが6－8の映画のタイトルを降順で抽出せよ

6. マット・デイモンがstarringの映画を抽出せよ

7. id 「1」のcategoriesを「1」に変更せよ

8. titleに「ー」が含まれる映画を全て抽出せよ

9.categoriesがホラーかSFであるものを全て抽出せよ

11.全ての映画のタイトルのみを抽出せよ

12．すべての映画ののcategoriesとstarringのみ抽出せよ

13．titleに「らんぶ」が含まれてるtitleを全て抽出せよ

14．idが6－8の映画のタイトルを順で昇順で抽出せよ

15.categoriesがコメディであるものを全て抽出せよ

16.categoriesが「サスペンス」である映画のtitleのみ抽出せよ

17categoriesが「SF」である映画を全て抽出せよ

18.categoriesに「ドラマ」を追加せよ

19.categoriesに「アダルト」を追加せよ

20.categories「アダルト」を今すぐに削除せよ
