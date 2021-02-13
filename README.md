# ScoopとVSCodeで Go 言語の環境構築

 ## 使用環境

 - Windows 10 Home Ver. 2004

## マニフェスト検索

Scoop に Go 言語の実行環境があるか、キーワード `go` で検索する

```console
scoop search go
```

Go 言語のパッケージが見つからない

```
'extras' bucket:
    appengine-go (1.9.70)
    clingo (5.4.0)
    godot-mono (3.2.3)
    godot (3.2.3)
    gog-galaxy-plugin-downloader (0.2.2)
    goldendict (1.5.0-RC2-372-gc3ff15f)
    google-java-format (1.9)
    googlechrome-beta (87.0.4280.40)
    googlechrome-canary (88.0.4307.2)
    googlechrome-dev (88.0.4302.0)
    googlechrome-portable (86.0.4240.111)
    googlechrome (86.0.4240.111)
    mongodb-compass-community (1.21.2)
    outlook-google-calendar-sync (2.8.0-beta)
    rust-msvc-nightly (nightly) --> includes 'cargo.exe'
    rust-nightly (nightly) --> includes 'cargo.exe'
    ungoogled-chromium-portable (85.0.4183.83)
    ungoogled-chromium (85.0.4183.121-1)
```

## Java バケットの追加

Java バケットに `go` パッケージがあるので、Java バケットを追加する

```console
scoop bucket add java
```

Java バケット追加後に、再度マニフェストを検索する

```concole
scoop search go
```

```
'java' bucket:
    dragonwell8 (8.3.3)

    argocd (1.7.8)
    centrifugo (2.7.2)
    forego (20180217041714)
    gauche (0.9.9) --> includes 'gosh.exe'
    global (6.6.3) --> includes 'gozilla.exe'
    go-ipfs (0.7.0)
    go (1.15.3)
    gobuster (3.1.0)
    gof (0.0.10)
    gogs (0.12.3)
    gomake (2.4.1)
    gomplate (3.8.0)
    gopass (1.10.1)
    goreleaser (0.146.0)
    gource (0.51)
    govc (0.23.0)
    gow (0.8.0)
    hugo-extended (0.77.0)
    hugo (0.77.0)
    mailsend-go (1.0.9)
    megacmd (1.4.0) --> includes 'mega-logout.bat'
    mongodb (4.2.7)
    nyagos (4.4.8_0)
    rust-msvc (1.47.0) --> includes 'cargo.exe'
    rust (1.47.0) --> includes 'cargo.exe'
    tinygo (0.15.0)
    unxutils (2007.03.01) --> includes 'stego.exe'
```

## Go をインストール

```console
scoop install go
```

以下のコマンドで環境変数 GOROOT のパスを確認できる

```console
$env:GOROOT
```

```
C:\Users\＜ユーザ名＞\scoop\apps\go\current
```

以下のコマンドでGoのバージョンを確認できる

```console 
go version
```

```
go version go1.15.8 windows/amd64
```

