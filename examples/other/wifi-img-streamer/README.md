## コンパイルコード  

> **注意** **> 公式のコンパイルコードだとWIFIアクセスポイントにならないので、必ず`SETUP_WIFI_AP=1`を追加して実行するようにしてください。**
```python:コンパイル  
docker run --rm -v ${PWD}:/module aideck-with-autotiler tools/build/make-example examples/other/wifi-img-streamer SETUP_WIFI_AP=1 image
```  
<br>
<br>

## cfloaderを用いたフラッシュ方法
> **注意** **> 公式だとE7E7...の所はないかもだけど、入れたほうがいい。（と思う。）**
```python:フラッシュ  
cfloader flash examples/other/wifi-img-streamer/BUILD/GAP8_V2/GCC_RISCV_FREERTOS/target.board.devices.flash.img deck-bcAI:gap8-fw -w radio://0/80/2M/E7E7E7E7E7
```
