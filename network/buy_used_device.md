# Network/中古機材の購入
## vendor, product
- Allied Telesis
  - ファームウェアのダウンロード: 保守契約は不要, ハードウェアのシリアル番号が必要
- Cisco
  - ファームウェアのダウンロード: 保守契約が必要
  - Cisco IOS XE 16.10.1a 以降でスマートライセンスが導入
    - 中古機器への影響が気になるところ
- NEC
  - UNIVERGE IX
    - ファームウェアのダウンロード: 保守契約は不要

## initialize
### Allied Telesis
1. console ポートを PC に接続 (9600bps)
1. 電源投入直後，Ctrl + B を叩いて Boot Menu を開く
1. 5 を入力 (`5. Special boot options`)
1. 1 を入力 (`1. Skip startup script (Use system defaults)`)
1. 0 を入力 (`0. Return to previous menu`)
1. 9 を入力 (`9. Quit and continue booting`)
1. 初期ユーザでログイン (user: `manager`, pass: `friend`)
1. `erase factory-default` を実行
