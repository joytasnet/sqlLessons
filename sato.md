# 準備

## 以下のデータベースを作成せよ

```

CREATE DATABASE cd_app
DEFAULT CHARACTER SET utf8
```

## 以下の２つのテーブルを作成せし、初期データを挿入せよ

### categories

```
CREATE TABLE `categories` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `category` varchar(10) NOT NULL
);

INSERT INTO `categories` (`id`, `category`)
VALUES
(1, '洋楽'),
(2, 'J-POP'),
(3, '演歌'),
(4, 'DANCE');
```

### cds

```
CREATE TABLE `cds` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `title` varchar(255) NOT NULL,
  `cat_id` int(11) DEFAULT NULL,
  `price` int(11) DEFAULT NULL
);

INSERT INTO `cds` (`id`, `title`, `cat_id`, `price`)
VALUES
(1, 'PLEASE PLEASE ME', 1, 2800),
(2, 'With the Beatles', 1, 2800),
(3, 'A Hard Days Night', 1, 2800),
(4, '17歳の地図', 2, 3200),
(5, '回帰線', 2, 3200),
(6, '壊れた扉から', 2, 3200),
(7, '北の大地', 3, 3600),
(8, '目蒲線物語', NULL, 1200);

```

## 以下の問に答えよ(20問)

1. cdsに以下のデータを挿入せよ
  (Help,1,2800)

1. tetetwete
  

