# I2C液晶1602

makecode I2C 液晶 1602 擴展  

  
![](lcd.jpg)


## 添加擴展

打開 makecode 編輯器，在項目中選擇擴展，然後在位址欄輸入下面網址  

https://github.com/mymell2003/I2CLCD1620_TW  

搜索後就可以添加並使用擴展了。

## 基本用法
```
let item = 0
OLED12864_I2C.init(60)
item = 0
basic.forever(() => {
    OLED12864_I2C.showNumber(0, 0, item, 1)
    item += 1
    basic.pause(1000)
}) 
```

## I2C 地址
有兩種I2C液晶模組，它們的位址不相同：    
- 39: PCF8574  
- 63: PCF8574A  

如果將位址設置為0，擴展會自動搜索並識別正確的位址
- 0：自動位址模式

## API

- **LcdInit**(address: number)  
初始化 LCD  
address: I2C 地址  
 0: 自動識別位址  
 39: PCF8574  
 63: PCF8574A

- **ShowNumber**(n: number, x: number, y: number)  
在液晶的指定位置顯示數位。  
n: 數字  
x: 液晶X軸座標, [0 - 15]  
y: 液晶Y軸座標, [0 - 1]  

- **ShowString**(s: string, x: number, y: number)  
在液晶指定位置顯示字串show a string in LCD at given position.  
s: 將要顯示的英文字串  
x: 液晶X軸座標, [0 - 15]  
y: 液晶Y軸座標, [0 - 1]  

- **on**()  
打開液晶的顯示功能

- **off**()  
關閉液晶  

- **clear**()  
清除液晶顯示的內容  

- **BacklightOn**()  
打開液晶的背光燈  

- **BacklightOff**()  
關閉液晶的背光燈  

- shl()
螢幕向左移動

- shr()
螢幕向右移動 


## 授權方式

MIT

microbit/micropython 中文社區版權所有 (c) 2018  

## 支援硬體

* for PXT/microbit


