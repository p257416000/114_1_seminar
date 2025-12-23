# Ultra Lightweight Dehaze Methods for Robot Vision Using High-Levell Synthesis
演講日期:114/12/23\
演講者:宋啟嘉 教授


## 以前研究
如何縮小AI模型

FPGA

## HLS(High-Level Synthesis)

不用手刻很底層的硬體語言，用C來寫，開發比較快，硬體也能跑很省電/很即時

講師有在ppt內比較

## Dehaze 除霧
需要對影像做處理，因為YOLO讀取影像時會有問題，車子不易辨識

講師做了多組測試條件(不同處理的圖)

讓YOLOv7去跑看哪種除霧方式最好

## 把除霧搬到 FPGA
好處FPGA速度快

## HLS(續)關於加速處理
可以用loop unrolling做把本來做四次的東西一次做完

array partition 讓硬體拿到更多資料

allocation 少用幾個乘法器或加法器 節省空間但會變慢

pipelining 上一張圖在運算是下一張圖已經讀取了

## 暗光增強
暗光需要NPU但我不想要多加一顆，所以我需要新的算法

## 水下影像研究
生成式AI不是很好，生成水底下的樣子，可能需要更多資料集

