 PumpkinPie

ウェーブレット変換を用いて画像を処理するアプリケーション（大学の授業でのグループ課題）。
画像かJSONファイルの信号を読み込み、画像であったらRGB成分ごとにウェーブレット変換を行、結果を画像かJSONファイルの信号として出力する

<!-- 例：画像を読み込み、RGB成分ごとにウェーブレット変換を行い、結果を〇〇として出力する -->

## 概要

- 入力：画像ファイル・JSONファイル（例：画像ファイル）
- 処理：画像をRGBの3成分に分解し、成分ごとにウェーブレット変換（ハールウェーブレット）を適用
- 出力：変換後の画像 / 係数データ

## 実行例

<img width="870" height="362" alt="image" src="https://github.com/user-attachments/assets/f1ca8fe5-b4fd-4d99-a0ab-2ba6a006e265" />


## 主な機能

- 画像のRGB成分への分解
- ウェーブレット変換
- 採用率調整
- ファイル保存

## 担当箇所

私（MikanKi）は以下を担当しました。

- 画像をRGB成分に分離するクラス（`RGB.java`）の設計・実装
- 変換計算の正しさを確認するテスト（`RGBTest.java, ImageWaveletTransformationTest.java, SignalWaveletModelTest.java, SignalWaveletTransformationTest.java`）の作成

## 使用技術

| 項目 | 内容 |
|------|------|
| 言語 | Java |
| ビルド | Maven |
| テスト | JUnit |
| CI | GitHub Actions |

## 動かし方

https://drive.google.com/file/d/1fpKR7aDEOsYhxBhdoRuOoG2_oKap1Awn/view?usp=share_link
でzipファイルをダウンロードし、適当な場所で展開する

ターミナルを開き、展開して得られるPumpkinPieというディレクトリへ移る。
```bash
$ cd PumpkinPie
```

中身を確認する。
```bash
$ ls *
```

さらに、targetディレクトリへ移動する。
```bash
 % cd target
```

実行するためのコマンドは以下の通りである。
```bash
$ java -jar PumpkinPie.jar
```
ただし、実行にはJava21が必要である。


## 工夫した点・学んだこと

- RGB分離とウェーブレット計算を別クラスに分け、テストしやすくし、役割分担を容易にできた
- 計算結果を既知の値と比較するテストで、実装の誤りを早期に見つけた

## チーム

- 6人（授業名：プロジェクト演習、3年度春学期）
- Project Manager：山口 大翔​
- Substitute Project Manager：工藤 大夢​
- Designer：山本 剛士、濱坂 颯太​
- Tech Lead：戸田 翔伍、フェリシア アイヴィー​（私）
- Quality Assurance：工藤 大夢​
