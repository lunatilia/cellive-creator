# Enterprise Linux(EL) 8 LiveGNOME 日本語UI kickstart

## 内容

次の EL 8 Liveメディア を作成するための kickstart および構築用のサンプルスクリプトです。

1. CentOS 8 LiveGNOME 日本語UI版
2. CentOS Stream 8 LiveGNOME 日本語UI版
3. AlmaLinux 8 LiveGNOME 日本語UI版
4. Rocky Linux 8 RC1 LiveGNOME 日本語UI版 **TEST RELEASE**

## 用途

- オリジナルの専用Liveメディアなどを作成する際のベース
- HDD などを処分するとき、論理的に完全削除を行いたい場合など

## 要件

- CentOS Linux 8.3.2011 またはその他 RHEL8.3 互換 OS が稼働しているマシン
- root権限
- git、lorax-lmc-novirt、lorax-templates-rhel、および依存パッケージがインストールされていること

## 実行例

この実行例は CentOS 8.3.2011 (Minimal Install) に git、lorax-lmc-novirt、lorax-templates-rhel のみをインストールした状態で実行しています。

```
# git clone https://github.com/lunatilia/el8-livemedia-japanese
# cd el8-livemedia-japanese
```

- CentOS 8 の場合

```
# mv samples/cent8live-builder .
# ./cent8live-builder kickstarts/centos-8-live-gnome.cfg 
```

- CentOS Stream 8 の場合

```
# mv samples/cstream8live-builder .
# ./cstream8live-builder kickstarts/centos-stream-8-live-gnome.cfg
```

- AlmaLinux 8 の場合

```
# mv samples/alma8live-builder .
# ./alma8live-builder kickstarts/almalinux-8-live-gnome.cfg
```

- Rocky Linux 8 の場合

```
# mv samples/rocky8live-builder .
# ./rocky8live-builder kickstarts/rocky-8-live-gnome.cfg
```

## ディスクイメージ

- [ディスクイメージのダウンロード](https://github.com/lunatilia/el8-livemedia-japanese/releases/tag/1.1.0-20210505)
  - AlmaLinux、Rocky Linux のOSイメージは除外

## ライセンス

[GNU GPLv2](https://github.com/lunatilia/el8-livemedia-japanese/blob/main/LICENSE) (The CentOS Projectのデフォルトライセンス)

## 参考

- lorax 28 : https://weldr.io/lorax/f28-branch/lorax.html
- Livemedia-creator- How to create and use a Live CD : https://fedoraproject.org/wiki/Livemedia-creator-_How_to_create_and_use_a_Live_CD
- centos-7-livemedia-japanese : https://github.com/lunatilia/centos-7-livemedia-japanese
