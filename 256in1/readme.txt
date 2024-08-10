ロム魂(256in1)SCC音声出力対応版のファームウェアです。
最大256のROMファイルをMSXπのフラッシュメモリに格納する事が出来ます。
ファイル格納用のフラッシュメモリ領域は16Mバイト弱です。
圧縮可能なファイル(128kバイト以下のファイル)はzlib形式で自動的に圧縮、伸張されるので
計16Mバイト以上のファイルを格納する事が可能です。

対応ファイル形式
* 各種ROMファイル
  非メガROM(ファイルサイズ32k以下のもの)、ASCII8Kマッパー、ASCII16Kマッパー、KONAMIマッパー、KONAMI SCCマッパー、R-TYPEマッパーに対応

CASファイルと32kを超えるノーマルロム(主にピーガー伝説のsg1000.exeで作成したロム)には対応しません。
CASファイルや32kを超えるノーマルロムを使用する場合はMSXπ完全互換モードでMSXπ typeA用の256in1を使用してください。

使用法

1. 256in1ファームウェアファイルを作成します。

256in1に含めたいROMファイル(1～256ファイル)を用意し、以下の形式の名前にリネームします。

* ROMファイルの場合
<NAME>.<MAPPER>.rom

<NAME>=任意の名前
この名前はゲーム選択メニューに表示されます。16文字を超える部分はメニューに表示されません。

<MAPPER>=ROMのマッパー形式(normal, ascii8k, ascii16k, konami, scc, rtype の何れか)
* normal: 非メガROM
* ascii8k: メガROM ASCII8Kマッパー
* ascii16k: メガROM ASCII16Kマッパー
* konami: メガROM konamiマッパー
* scc: メガROM konami SCCマッパー
* rtype: メガROM R-TYPEマッパー

例:
1942.ascii8k.rom
Gradius.konami.rom
R-Type.rtype.rom
Super Pierrot.ascii16k.rom
Thexder.normal.rom

上記ROMファイルと256in1.exeを同じディレクトリにおいて256in1.exeを実行します。
コマンドプロンプトで実行すると以下のようなメッセージが出ます。
(ダブルクリックによる実行でも構いません)

～ ピーガー伝説のロム魂(256in1)ツール SCC音声出力対応版 ～
[000] mapper:82 offset:00001900 name:1942
[001] mapper:84 offset:00009856 name:Gradius
[002] mapper:90 offset:00017361 name:Hydlide
[003] mapper:05 offset:0001b3e9 name:R-Type
[004] mapper:83 offset:0007b3e9 name:Super Pierrot
[005] mapper:81 offset:00081af5 name:Thexder
使用領域: 564kB
空き領域: 15819kB

同ディレクトリに作成される256in1.uf2というファイルが256in1ファームウェアファイルです。

2. MSXに刺さっていない状態のMSXπをブートモードでPCに接続します。

まずSOUNDスイッチを「1」側にしてください。
MSXπのBOOTSELボタンを押しながらPCとUSB接続して下さい。
接続が成功するとドライブが認識されます。

3. MSXπに1で作成した256in1.uf2ファイルを書き込みします。

2で認識されたドライブに256in1.uf2をドラッグアンドドロップ(コピー)します。
コピーが完了するとドライブが見えなくなります。

4. 書込みが終わったらPCから外して完了

SOUNDスイッチを「1」側にして使用して下さい。

注意：PCとの接続中はバスバッファの入力がフロート状態となります。
あまり良い状態ではないので長時間のPC接続は避けてください。

5. ゲーム起動方法

キーボード又はジョイスティック1の上下左右でゲームを選択してスペース又はトリガー1でゲーム起動です。

上: 1戻る
下: 1進む
左: 16戻る
右: 16進む
