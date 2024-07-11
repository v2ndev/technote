# Network/SFP EEPROM
## links
- [SFF-8472](https://members.snia.org/document/dl/25916)

## memo
- SFP モジュールには I2C EEPROM (または EEPROM エミュレーション) が内蔵されている
- 0x50 (EEPROM), 0x51 (制御/モニタ用?)

## unlock
- Finisar
  - addr = 0x51, pos = 0x7b に 0x00 0x00 0x00 0x00 を書き込む

## AT-x series の i2c コマンド
- アライドテレシスの一部のスイッチは，SFP モジュールの I2C バスが /dev/i2c-* として見える
  - AT-x230-10GT, AT-SH230-28GT, AT-GS980MX/28 にて確認
  - AT-x510-28GTX では見えない
  - 多分，AT-xX30 系で使えるようになったのだと思う
- コマンド
  - `i2crpobe <i2c bus device>` デバイスを検出する
  - `i2cdump <i2c bus device> <addr> <len>` 読み込み
  - `i2cwrite <i2c bus device> <addr> <pos> <data...>` 書き込み
  - 数値は 16 進数で指定する
