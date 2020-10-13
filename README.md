# CentOS Linux 8 LiveGNOME 日本語UI kickstart

## 内容

次の CentOS 8 Liveメディア を作成するための kickstart および簡易構築スクリプトです。

1. CentOS 8 LiveGNOME 日本語UI版

## 用途

- オリジナルの専用Liveメディアなどを作成する際のベース
- HDD などを処分するとき、論理的に完全削除を行いたい場合など

## 要件

- CentOS Linux 8.2.2004 またはその他 RHEL8.2 互換 OS が稼働しているマシン
- root権限
- git、lorax-lmc-novirt、lorax-templates-rhel、および依存パッケージがインストールされていること

## 実行例

この実行例は CentOS 8.2.2004 (Minimal Install) に git、lorax-lmc-novirt、lorax-templates-rhel のみをインストールした状態で実行しています。


```
# git clone https://github.com/lunatilia/centos-8-livemedia-japanese
# cd centos-8-livemedia-japanese
# ./c8live-builder centos-8-live-gnome.cfg 
```

## ディスクイメージ
- [ディスクイメージのダウンロード](https://github.com/lunatilia/centos-8-livemedia-japanese/releases/tag/1.0.2-20201014)

## ライセンス

[GNU GPLv2](https://github.com/lunatilia/centos-8-livemedia-japanese/blob/master/LICENSE) (The CentOS Projectのデフォルトライセンス)

## 参考

- lorax 28 : https://weldr.io/lorax/f28-branch/lorax.html
- Livemedia-creator- How to create and use a Live CD : https://fedoraproject.org/wiki/Livemedia-creator-_How_to_create_and_use_a_Live_CD
- centos-7-livemedia-japanese : https://github.com/lunatilia/centos-7-livemedia-japanese
