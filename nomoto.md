# 準備

## 以下のデータベースを作成せよ

```

CREATE DATABASE cinema_app
DEFAULT CHARACTER SET utf8
```

## 以下の２つのテーブルを作成せし、初期データを挿入せよ

### countries

```
CREATE TABLE `countries` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `country` varchar(10) NOT NULL
);

INSERT INTO `countries` (`id`, `country`)
VALUES
(1, 'アメリカ'),
(2, 'フランス'),
(3, '台湾'),
(4, '韓国'),
(5, '日本');
```

### cinemas

```
CREATE TABLE `cinemas` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `title` varchar(255) NOT NULL,
  `cat_id` int(11) DEFAULT NULL,
  `director` varchar(50) DEFAULT NULL
);

INSERT INTO `cinemas` (`id`, `title`, `cat_id`, `director`)
VALUES
(2, '紳士は金髪がお好き', 1, 'ハワード・ホークス'),
(1, 'めまい', 1, 'アルフレッド・ヒッチコック'),
(3, '気狂いピエロ', 2, 'ジャン・リュック・ゴダール'),
(4, 'ポンヌフの恋人', 2, 'レオス・カラックス'),
(5, '牯嶺街少年殺人事件', 3, 'エドワード・ヤン'),
(6, 'ミレニアム・マンボ', 3, 'ホウ・シャオシェン'),
(7, 'はちどり', 4, NULL),
(8, 'めし', NULL, '成瀬巳喜男');

```

## 以下の問に答えよ(20問)

1. cinemasに以下のデータを挿入せよ
  ('寝ても覚めても',5,'濱口隆介')

1. ciemasテーブルのidが９のdirectorを濱口竜介に変更せよ

1. ciemasテーブルのdirectorがNULLのデータを抽出せよ。

1. cinemasテーブルのidが７のdirectorにキム・ボラと追加せよ

1. cinemasテーブルのidが8のcat\_id がcontriesテーブルと結合したときに日本になるようにせよ

1. cinemasテーブルの全てのデータを抽出せよ。

1. cinemasテーブルのtitleの文字数を抽出せよ。

1. cinemasテーブルのtitleを題名とし、directorを監督とし、題名と監督だけ抽出せよ。

1. cinemasテーブルのtitleを題名とし、directorを監督とし、題名と監督だけ抽出せよ。

1. cinemasテーブルとcountriesテーブルを内部結合し、titleとdirectorとcountryを表示せよ。

1. countriesテーブルのcountryに香港を追加せよ。

1. cinemasテーブルのidが９のデータを削除せよ。

1. cinemasテーブルのdirectorに「人」が含まれているデータ以外を抽出せよ。

1. cinemasテーブルのtitleとtitleの文字数を抽出し昇順に表示せよ。

1. cinemasテーブルに以下のデータを挿入せよ。
('恋する惑星',6,'ウォン・カーウァイ')

1. cinemasテーブルのtitleに「人」が含まれているデータを抽出せよ。

1. cinemasテーブルのdirectorに「人」が含まれているデータ以外を抽出せよ。

1. cinemasテーブルのdirectorとdirectorの文字数を抽出し降順に表示せよ。

1. cinemasテーブルのdirectorの文字数の合計を表示せよ。

1. cinemasテーブルのidが1,2はアメリカ3,4はヨーロッパ それ以外はアジアとしカラム名をエリアとせよ。取得データはtitle,director,エリアとする。
