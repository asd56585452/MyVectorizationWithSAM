# MyVectorizationWithSAM
 
多媒體技術概論的final，Group 14

## 實作方式

1. 先透過SAM將圖片分塊，在將每一塊個別Vectorization
2. 用opencv找出輪廓，並將mask中空填充以及進一步切塊
3. 每一塊初始用一條bezier_curve描述，並計算誤差，將誤差最大的bezier_curve切成兩個bezier_curve，直到設定的數量上限
4. 最後用mask決定color

## 如何使用

1. clone此資料夾
2. 安裝SAM(Segment Anything Model)，並將vit_h的Model Checkpoints放在與程式同目錄下
3. 安裝opencv、scipy、matplotlib
4. 修改參數並執行SAMVG-sam_v1.ipynb

##pngtosvg setting
1. run pip install cairosvg
2. install gtk3-runtime-3.24.31-2022-01-04-ts-win64.exe
 from https://github.com/tschoonj/GTK-for-Windows-Runtime-Environment-Installer/releases
3. add C:\Program Files\GTK3-Runtime Win64\bin to PATH
