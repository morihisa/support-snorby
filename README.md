# このリポジトリは「ハニーポットと学ぶ侵入検知システム」のコマンド入力サンプルを紹介しています。
技術書典5で紙の本を頒布。カラー電子版は booth でご購入いただけます。 https://morihi-soc.booth.pm/items/1036585

## インストール環境
下記の OS にて、インストールできることを確認しています。

- Ubuntu 16.04 Server 64bit

## インストール手順
解説は「ハニーポットと学ぶ侵入検知システム」を参照してください。インストール順序は、下記の通りです。

1. snort-install.txt
1. detection-test.txt
1. barnyard2-install.txt
1. snorby-install.txt

Snorby インストール後は、 ***必ずパスワードを変更*** してください。

## 各種ソフトウェアの起動コマンドまとめ
- Snortの起動
	- $ sudo snort -q -u snort -g snort -c /etc/snort/snort.conf -i ens33 -k none &
- Barnyard2の起動
	- $ sudo barnyard2 -c /etc/snort/barnyard2.conf -d /var/log/snort -f snort.u2 -w /var/log/snort/barnyard2.waldo -g snort -u snort &
- Snorbyの起動
	- $ cd /opt/snorby/
	- $ sudo bundle exec rails server -e production &
- WOWHoneypotの起動
	- $ cd ~/wowhoneypot
	- $ python3 ./wowhoneypot.py &

***
- Author: @morihi_soc (https://www.morihi-soc.net/ )
