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

```bash

```

## 工夫した点・学んだこと

- 〇〇（例：RGB分離とウェーブレット計算を別クラスに分け、テストしやすくした）
- 〇〇（例：計算結果を既知の値と比較するテストで、実装の誤りを早期に見つけた）

## チーム

- 〇〇人（授業名：〇〇、〇〇年度）
- 役割分担：〇〇

## ライセンス

授業課題のため〇〇
A few notes on it:
