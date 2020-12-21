#問題
まずサーバ直下に以下を、
CREATE DATABASE games_app
DEFAULT CHARACTER SET utf8

次に以下の２つのテーブルを作成し、初期データを挿入せよ。

CREATE TABLE `categories` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `category` varchar(10) NOT NULL
);

INSERT INTO `categories` (`id`, `category`)
VALUES
(1, 'アクションゲーム'),
(2, 'ローグライトゲーム'),
(3, 'シューティングゲーム'),
(4, 'パズルゲーム');
);

CREATE TABLE `hard` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `type` varchar(10) NOT NULL
);

INSERT INTO `hard` (`id`,`type`)
VALUES
(1,'ファミコン'),
(2,'プレイステーション'),
(3,'セガサターン'),
(4,'PC'),
(5,'スイッチ');

CREATE TABLE `games` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `title` varchar(255) NOT NULL,
  `cat_id` int(11) DEFAULT NULL,
  `price` int(11) DEFAULT NULL,
  `type_id` varchar(255) NOT NULL
);

INSERT INTO `games` (`id`, `title`, `cat_id`, `price`, `type_id`)`
VALUES
(1, 'ヒットラーの復活', 1, 2800, 1),
(2, 'キングスフィールド', 1, 800, 2),
(3, 'ソルスティス', 1, 1800, 1),
(4, 'Noita', 2, 2200, 4),
(5, 'トルネコの大冒険2', 2, 1200, 2),
(6, 'グラディウスデラックスパック', 2, 3200, 2),
(7, 'バトルガレッガ', 3, 13600, 3),
(8, 'ザナック', NULL, 2200, 1),
(9, 'バベルの塔', NULL, 700, 1),
(10, 'ソロモンの鍵', NULL, 1200, 1);

１、全件抽出せよ。

２、title,type_idのカラムを抽出せよ。

３、'の'が含まれる曖昧検索をせよ。

４、'cat_id'がnullでなく、priceが2000以上のものを抽出せよ。

５、カテゴリーごとの合計価格を求め、合計価格が3000以下の項目cat＿idを抽出せよ。

６、カテゴリ未分類のものを抽出し、idを5,'未分類'とせよ。

７、カテゴリごとの平均価格を求め、昇順に抽出せよ。

８、値段が3番目に高いものを抽出せよ。取得カラムは、title,price。

９、全てのゲームのpriceの平均を求めよ。

１０、hardのtypeがファミコンのものをすべて1000値上げせよ。

１１、最も価格が高いものを半額にせよ。

１２、次のデータを追加せよ。シャドウゲイト ,1800,ファミコン

１３、プレイステーションのものを全て削除せよ。

１４、次のテーブルを作成せよ。
CREATE TABLE `shop` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `place` varchar(10) NOT NULL
  `cat_id` int(11) NOT NULL
);

１５、以下の店舗データを入力せよ。
INSERT INTO `shop` (`id`,`place`,`cat_id`)
VALUES
(1, '札幌',1),
(2, '中村橋',2),
(3, '中野',3),
(4, '秋葉原',4);

１６、以下の構文で、テーブル同士を結合せよ。
SELECT
  テーブル.表示するフィールド
FROM
  テーブル１ INNER JOIN テーブル２
ON
  テーブル.比較するフィールド

実行するSQL文
  SELECT
  game.id, game.title, game.cat_id, game.price, game.type_id,shop.place
FROM
  game INNER JOIN shop
ON
  game.cat_id = shop.cat_id;

１７、gamesテーブルで、カテゴリがPCのものを、同タイトル２本さらに追加せよ。

１８、登録件数を抽出せよ。

１９、cat_idをcat.idに変更せよ。

２０、最も値段が高いタイトルから2000割引し、カテゴリ合計が最も安いものに含まれるそれぞれのタイトルを1000ずつ値上げせよ。