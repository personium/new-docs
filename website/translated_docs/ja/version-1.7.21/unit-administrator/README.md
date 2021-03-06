---
id: version-1.7.21-README
title: Unit管理者向けガイド
sidebar_label: Unit管理者向けガイド
---

構築・設定済のPersonium Unitに対してUnitユーザトークンを使ってアクセスして、
Unit管理者の業務、すなわちCellの作成・払出しや払出したCellの管理等を実施する方のためのガイドドキュメントです。

Personium Unitを構築する方や、Personiumサーバプログラムをビルド・デプロイ・設定する方は、[サーバソフトウェア運用者向けガイド](../server-operator/README.md)をご覧ください。

## UnitユーザとユニットレベルAPI

UnitユーザとはPersonium Unitで認識されるUnitユーザトークンの発行を受けたユーザで、
CellのCRUD等ユニットレベルのAPIを操作可能な主体となります。

* [Unitユーザ](./Unit-User.md)

Cellの生成や管理を司るユニットレベルAPIへのアクセスにはUnitユーザトークンが必要です。また
Cellは生成されたときにどのUnitユーザトークンで生成されたかを覚えており、自身を作成した
Unitユーザに対しては、常にCellレベル・BoxレベルのすべてのAPIに特権アクセスを許可します。

## チュートリアル

Personium Unitを管理するための基本的な操作に関するチュートリアルを公開しています。
Personium Unitを初めて管理される方はご確認ください。

* [Cellの払い出し チュートリアル](./tutorial.md)


## GUIを利用したユニットの管理

以下のユニットマネージャGUIを使うことで、ほぼすべてのAPIアクセスをUnitユーザとして実施することができます。

[app-uc-unit-manager](https://github.com/personium/app-uc-unit-manager)

このツールは複数の起動方法をサポートしており、ユーザCellのHomeアプリから起動したときは、
アクセスすべき対象CellのURLやアクセスのためのトークン情報が起動パラメタとして付加された形で起動します。
その場合このアプリはCellマネージャとして振舞います。一方で、特にそのようなパラメタ指定なく起動したときは、
ユニットマネージャGUIとして起動します。

## Cell払出サンプルクライアント

前述ユニットマネージャGUIを使えば、手動で様々なAPI操作を試すことができますが、Unit管理者にとって
Cell発行希望者に対していちいち手動でレコードを追加してゆくのは非現実的でしょう。

多くの場合、所定仕様でのCellを作成するプログラムを作成したり、
Cell利用申込画面を作成したりといったこととなります。その際は
以下のサンプルアプリをご活用ください。

[app-uc-cell-creator](https://github.com/personium/app-uc-cell-creator)

小規模な運用であれば、このサンプルプログラムそのものを使ってCellの払出をするのでもよいでしょう

## その他

* [データの管理](./Data_Management.md)


## 関連するリポジトリ
* [app-uc-unit-manager](https://github.com/personium/app-uc-unit-manager)
* [app-uc-cell-creator](https://github.com/personium/app-uc-cell-creator)

