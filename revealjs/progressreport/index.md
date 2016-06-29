---
revealjs-url: https://cdnjs.cloudflare.com/ajax/libs/reveal.js/3.3.0
theme: beige
history: true
# minScale: 1.4
css: style.css

title: Progress report
author: Sodeyama
date: 2016.7.15
...

# 概要

##

 - 現状
 - 論文紹介
 - 研究テーマについて
 - 今後の予定

# 現状

## モンテカルロ木探索実装中

## 論文を読んでみた

 - 局所評価関数を使う新たなUCT探索法の提案とオセロによる評価
 - 前原彰太 橋本剛 小林康幸
 - 2010年6月
 - 情報処理学会研究報告

# 論文紹介

## 「局所評価関数を使う新たなUCT探索法の提案とオセロによる評価」

## 内容一覧

- 研究背景
- UCB値とモンテカルロ木探索
- 提案手法
- 実験結果

## 研究背景

- モンテカルロ木探索 = モンテカルロ法 + UCT
- 局面の評価関数の研究はほとんど行われていない

<!-- リストの終わり -->

→UCBの値に局面評価関数を加えてみる

## UCB値とモンテカルロ木探索

 - 計算式 : $$UCB値 = \overline{ x_j }+c\sqrt{ \frac{ 2\log n }{ n_j } }$$
 - $\overline{ x_j }$ : 期待値
 - $c\sqrt{ \frac{ 2\log n }{ n_j } }$ : バイアス

## 大浦の手法

 - 合法手の数をカウント
 - オセロ : 合法手が多い = 有利
 - 終局の情報　＋　合法手の数

## 提案手法の木探索

 - Sum1 : 先手の子ノード数
 - Sum2 : 後手の子ノード数
 - Score : 終局での状況

## 提案手法 : UCT+

 - $$UCB+値 = (\overline{ x_j }+E_j)+c\sqrt{ \frac{ 2\log n }{ n_j } }$$
 - $E_j$ : Sum1,Sum2
 - $x_j$ : Score

## 実験結果

# 研究テーマについて

# 今後の予定

 - 研究テーマの詳細を決める
 - CUDAの学習