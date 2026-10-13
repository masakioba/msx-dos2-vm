# MSX-DOS2 VM and BDS C for Web

A web-based MSX-DOS 2 compatible environment with built-in BDS C and a machine language monitor.

BDS Cとマシン語モニタを内蔵した、WebベースのMSX-DOS 2互換環境です。

## Overview / 概要

MSX-DOS2 Virtual Machine runs in a web browser using JavaScript. It emulates the Intel 8080, Z80, and R800 instruction sets and provides CP/M and MSX-DOS 1/2 compatible system calls.

JavaScriptを使用してWebブラウザ上で動作します。Intel 8080、Z80、R800の命令セットをエミュレートし、CP/MおよびMSX-DOS 1/2互換のシステムコールを提供します。

Unlike a conventional MSX emulator, it does not emulate the entire MSX hardware. It focuses on running MSX-DOS programs in a convenient environment.

This software consists of a CPU emulator and an MSX-DOS compatibility layer.

このソフトウェアはCPUエミュレーターとMSX-DOS互換レイヤーで構成されています。

It does not use the original MSX-DOS or any MSX ROMs. MSX BIOS is not implemented.

本物のMSX-DOSやMSX ROMは使用していません。MSX-BIOSも実装していません。

Unlike a conventional MSX emulator, it does not emulate the entire MSX hardware. It focuses on running DOS programs in a convenient environment.

一般的なMSXエミュレーターとは異なり、MSXのハードウェア全体は再現しません。MSX-DOSプログラムを使いやすい環境で実行することを目的としています。

## Testing Status / 動作確認状況

This software has undergone only limited testing. Most features have not been verified.

このソフトウェアの動作テストは限定的です。ほとんどの機能は動作確認できていません。

So far, BDS C is the only software that has been tested successfully.

現在までに動作を確認したソフトウェアはBDS Cのみです。

The Z80/R800 extended instructions and MSX-DOS 1/2 extended system calls have not been tested.

Z80/R800拡張命令と、MSX-DOS/MSX-DOS2拡張システムコールの動作確認はしていません。

## Features / 主な機能

- Intel 8080, Z80, and R800 instruction emulation  
  Intel 8080、Z80、R800の命令エミュレーション
- CP/M and MSX-DOS 1/2 compatible system calls  
  CP/MおよびMSX-DOS 1/2互換システムコール
- Built-in BDS C compiler and linker loader  
  BDS Cコンパイラおよびリンカの読み込み機能
- Machine language monitor with memory editing, registers, Run, and Step  
  メモリ編集、レジスタ表示、Run、Stepに対応したマシン語モニタ
- DOS shell with directory and file commands  
  ディレクトリ操作とファイル操作に対応したDOSシェル
- Built-in vi-like text editor  
  vi風テキストエディター
- Persistent virtual disk using IndexedDB  
  IndexedDBを使用した永続的な仮想ディスク
- File upload and download  
  ファイルのアップロードとダウンロード

## Getting Started / 使用方法

Open `msxdos2vm.html` in a web browser.

Webブラウザで `msxdos2vm.html` を開きます。

Type `HELP` to display the available commands.

`HELP` と入力すると、使用できるコマンドの一覧が表示されます。

Click **Load BDS C** to load the BDS C development tools from `bdsc.js`.

**Load BDS C** ボタンを押すと、`bdsc.js` からBDS Cの開発ツールを読み込みます。

## Limitations / 制限事項

This project does not emulate MSX video or sound hardware. Software that directly accesses MSX hardware may not work.

MSXの映像・音声ハードウェアはエミュレートしていません。MSXのハードウェアを直接操作するソフトウェアは動作しない場合があります。

CPU instruction and DOS compatibility are still under development.

CPU命令およびDOS互換性については、引き続き開発中です。

## BDS C

BDS C is a C compiler for CP/M-80 and MSX-DOS, targeting the Intel 8080 CPU.

BDS CはCP/M-80とMSX-DOS向けの8080 CPU対応のC言語コンパイラです。

BDS C was developed by Leor Zolman and released into the public domain in 2002.

BDS CはLeor Zolman氏によって開発され、2002年にパブリックドメインとして公開されました。

Official website / 公式サイト: https://www.bdsoft.com/resources/bdsc.html

## Compiling with BDS C / BDS Cでのコンパイル方法

To compile `ABC.C`, run the following commands:

`ABC.C` をコンパイルするには、次のコマンドを実行します。

```text
A:\>cc abc.c
A:\>clink abc
```

To run the compiled program:

コンパイルしたプログラムを実行するには、次のコマンドを入力します。

```text
A:\>abc
```

## License / ライセンス

MIT License
