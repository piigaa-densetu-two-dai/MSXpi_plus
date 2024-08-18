テスト版です

2nd PSG音源+FM音源(MSX-MUSICC)のファームウェアです。

音声データの生成にemu2149/emu2413(great!)を使用しています。
https://github.com/digital-sound-antiques/emu2149
https://github.com/digital-sound-antiques/emu2413

使用法

1. psgfm.binファイルの後ろにMSX-MUSIC(MSX2PMUS.rom)のROMファイルを連結します。

unixのcatコマンドを使用する例
$ cat psgfm.bin MSX2PMUS.rom > firmware.bin

windowsのcopyコマンドを使用する例
>copy /b psgfm.bin + MSX2PMUS.rom firmware.bin

2. uf2conv.exeを用いて1で作成したfirmware.binをuf2ファイルに変換します。

例: windowsコマンドプロンプト上で
uf2conv.exe firmware.bin firmware.uf2

uf2conv.exeはhttps://github.com/piigaa-densetu-two-dai/MSXpi_typeAにあります。

3. MSXに刺さっていない状態のMSXπをブートモードでPCに接続します。

まずSOUNDスイッチを「1」側にしてください。
MSXπのBOOTSELボタンを押しながらPCとUSB接続して下さい。
接続が成功するとドライブが認識されます。

4. MSXπに2で作成したfirmware.uf2ファイルを書き込みします。

3で認識されたドライブにfirmware.uf2をドラッグアンドドロップ(コピー)します。
コピーが完了するとドライブが見えなくなります。

5. 書込みが終わったらPCから外します。

SOUNDスイッチを「1」側にして使用して下さい。

注意：PCとの接続中はバスバッファの入力がフロート状態となります。
あまり良い状態ではないので長時間のPC接続は避けてください。
