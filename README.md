![logo1](https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_13.png)


[English README is here]()



## 概要

有償ソフトウェア、スケジュールナース上で動く、塾講師のシフト作成問題を解くプロジェクトです。
オリジナル問題は、Qiitaでの記事、[Google OR-Toolsによる最適化プロジェクト入門](https://qiita.com/yukiopt/items/dab6bc76d9ff41d551f5)です。

## スケジュールナースのインストール

スケジュールナースは、Windows10/11で動く、有償ソフトです。480円/月(2024　12月現在)

1. [インストールサイト](https://apps.microsoft.com/store/detail/9N94ZPBTB0RL)でインストールします。

2. GithubViewerを開きます。 

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/github_viewer.png" width="400"/></div>

3. 本サイトが出てくるまで　Nextを押します。
<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/select_file_on_github.png" width="600"/></div>

4. 本プロジェクトをダウンロードします。 
<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/downloaded_file.png" width="600"/></div>

5. プロジェクトに名前を付けて保存します。


6. 求解ボタンを押します。
<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/solve_window.png" width="1200"/></div>

##　モデル化

### 空きコマを出来るだけ少なくしたい

当該制約とは無関係な出勤ペナルティ発生部(行制約:3)をオフにします。(当該ソフト制約のチェックを外して求解します。)
また、勤務シフト希望が変わらないように、予定の重みを重くします。

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_21.png" width="1200"/></div>


### 出勤日数を出来るだけ少なくしたい

題意より、ソフト出勤希望を全てオフにしています。また前述の空きコマのペナルティをオフにして求解します。

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_22.png" width="1200"/></div>



## 実装

シフト形態は、規定されていないのですが、4コマ、3コマ、2コマ連続の全てのパターンがあり得る、と想定しました。(1コマ単独は禁止を想定）

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_18.png" width="1200"/></div>


目的のペナルティを発生させている部分の制約は、以下です。

### 空きコマ時間


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_20.png" width="1200"/></div>


### 出勤(休みの否定)


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_19.png" width="1200"/></div>

## アルゴリズム

下記アルゴリズムの選択が可能です。


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_16.png" width="1200"/></div>


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_23.png" width="1200"/></div>

## 予定入力例

全セル、レベル1に制約しています。

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_17.png" width="1200"/></div>


## シフト解例

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_24.png" width="1200"/></div>


## タスク解例

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_26.png" width="1200"/></div>


## シフト・タスク解例
<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_25.png" width="1200"/></div>


