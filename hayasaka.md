#以下のデータベースを作成せよ

CREATE DATABASE school_db
DEFAULT CHARACTER SET utf8

#以下の4つのテーブルを作成せし、初期データを挿入せよ

##schools
CREATE TABLE schools(
  id int PRIMARY KEY AUTO_INCREMENT,
	name VARCHAR(255) NOT NULL
);

INSERT INTO schools(name)
	VALUES('A校'),
	('B校'),
	('C校');

##students
CREATE TABLE students(
  id int PRIMARY KEY AUTO_INCREMENT,
	name VARCHAR(255) NOT NULL,
	school_id int NOT NULL
);

INSERT INTO students(name,school_id)
	VALUES('山田太郎',1),
	('鈴木花子',1),
	('高橋みお',1),
	('赤井ハルト',1),
	('渡辺壮太',1),
	('伊藤メイ',1),
	('小林葵',1),
	('吉田優斗',1),
	('佐々木のぞみ',2),
	('松本ひとし',2),
	('中村ともや',2),
	('田中けい',2),
	('鈴木ヒカル',2),
	('本田つばさ',2),
	('森あきと',3),
	('前田陸',3),
	('長谷川カイト',3),
	('石井あさひ',3),
	('坂本こはる',3),
	('青木りん',3);

##subjects
CREATE TABLE subjects (
  id int PRIMARY KEY AUTO_INCREMENT,
	name VARCHAR(255) NOT NULL
);

INSERT INTO subjects(name)
	VALUES('国語'),
	('数学'),
	('英語'),
	('理科');

##exams
CREATE TABLE exams(
  id int PRIMARY KEY AUTO_INCREMENT,
	student_id int NOT NULL,
	date DATE NOT NULL,
	subjects_id int NOT NULL,
	score int NOT NULL
);

	
INSERT INTO exams(student_id,date,subjects_id,score)
	VALUES
	(1,'2019-12-15',1,65),
	(1,'2019-12-15',2,80),
	(1,'2019-12-15',3,59),
	(1,'2019-12-16',4,90),
	(1,'2019-12-16',5,78),
	(2,'2019-12-15',1,90),
	(2,'2019-12-15',2,78),
	(2,'2019-12-15',3,85),
	(2,'2019-12-16',4,92),
	(2,'2019-12-16',5,70),
	(3,'2019-12-15',1,45),
	(3,'2019-12-15',2,62),
	(3,'2019-12-15',3,50),
	(4,'2019-12-15',1,77),
	(4,'2019-12-15',2,82),
	(4,'2019-12-15',3,46),
	(9,'2019-12-10',1,83),
	(9,'2019-12-10',2,90),
	(9,'2019-12-10',3,55),
	(10,'2019-12-10',1,67),
	(10,'2019-12-10',2,42),
	(10,'2019-12-10',3,96),
	(16,'2019-12-11',1,67),
	(16,'2019-12-11',2,42),
	(16,'2019-12-11',3,96),
	(17,'2019-12-11',1,67),
	(17,'2019-12-11',2,42),
	(17,'2019-12-11',3,96);


##以下の問に答えよ(20問)

1.studentsテーブルにname(藤井サクラ)、school_id(3)を追加せよ

2.studentsテーブルの全てのデータを抽出せよ。

3.subjectsテーブルにname(地理・歴史)を追加せよ

4.subjectsテーブルの全てのデータを抽出せよ。

5.studentsテーブルのschool_id=1以外のデータを抽出せよ。

6.studentsテーブルのschool_id=7のデータを削除せよ。

7.examsテーブルのstudent_id=1,subjects_id=1のscoreを66にせよ。

8.examsテーブルの日付を昇順に並べ替えよ。

9.studentsテーブル。名前に[木]が含まれる生徒を抽出せよ

10.全生徒数を抽出せよ。

11.examsテーブル。スコアの平均を求めよ。

12.studentsとschoolsを内部結合。学校名と生徒名を表示せよ。

13.studentsとexamsを内部結合。試験を受けた生徒のidと名前を抽出。重複は除外する。

14.subjectsとexamsを内部結合。科目ごとの平均点を求めよ。

15.schoolsとstudentsを内部結合。各学校の生徒数を求めよ。取得カラムは学校名と生徒数とする。

16.studentsとexamsを内部結合。試験を受けた生徒の合計点を求め、降順に抽出せよ。取得カラムは生徒名と合計点とする。


