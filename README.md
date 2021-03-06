## oose_0324031
資3A 0324031 廖家生  
資3A 0324023 劉明憲  
資3A 0324057 李栢陞  
### 摘要：
在眾多的交通工具中，許多人們都會使用汽車作為代步工具，若你家中有汽車的話，相信在你投保的保險中會有「車險」這個項目，如果你覺得車險費用機制是不公平（如：在一年內不論開車的里程數多寡，車險的費用都是一樣的），可以參考我們的車險機制，我們車險的機制主要是在一年內依照 **「駕駛行為」、「行駛里程」、「駕駛時段」** 來決定費用的價格。

在車險方面，我們會安裝一個小黑盒(OBU)在汽車上，小黑盒可記錄車子的 **「速度」、「加速度」以及「煞車距離」……** 等，有了這些資料就可以了解駕駛人的 **「駕駛行為」、「時間」以及「里程數」** ，接著將這些資料上傳到雲端進行分析，就能夠得知駕駛人在開車上的行為並且藉此計算出車險費用。如下圖：

![Alt text](operation.jpg "運作流程")

![Alt text](系統介面.jpg "系統介面")

### 使用者使用案例  
![Alt text](userUseCase.png "使用者使用案例")

| 使用者個案名稱：客戶登入|
| :----------------------------|
| 行為者：客戶<br>目標：客戶能以會員身分登入系統<br>前提：客戶尚未以會員身分登入系統<br>結束狀態：客戶透過手機上網，利用APP登入<br>一系列事件：客戶登出系統<br>正常程序—<br>1. 	客戶透過手機上網，利用APP登入<br>2. 	系統驗證帳密<br>3. 	系統驗證登入成功<br>例外狀況—<br>系統驗證失敗，客戶無法登入|

### 「客戶登入」個案強韌圖  
![Alt text](clientRA.png "客戶使用個案強韌圖")

### 「客戶登入」個案活動圖  
![Alt text](clientAD.png "客戶登入活動圖")

|使用者個案名稱：查看駕駛行為|
|:-------------------------|
| 行為者：客戶<br>目標：查看本身駕駛行為資訊<br>前提：會員成功登入系統<br>結束狀態：客戶離開「查看駕駛行為」操作介面<br>一系列事件：<br>正常程序—<br>1. 	客戶會員登入成功<br>2. 	使用「查看駕駛行為」功能<br>3. 	查看客戶駕駛行為相關資訊<br>例外狀況—<br>系統登入驗證失敗，無法使用此功能|

### 「查看駕駛行為」個案強韌圖  
![Alt text](driverRA.png "駕駛使用個案強韌圖")

### 「查看駕駛行為」個案活動圖  
![Alt text](driverAD.png "駕駛使用個案活動圖")

|使用者個案名稱：尋找車輛位置|
|:----------------------|
| 行為者：客戶<br>目標：尋找自己愛車所在位置<br>前提：會員成功登入系統<br>結束狀態：客戶離開「尋找車輛位置」操作介面<br>一系列事件：<br>正常程序—<br>1. 	客戶會員登入成功<br>2. 	使用「尋找車輛位置」功能<br>3. 	顯示出客戶愛車所在的位置<br>例外狀況—<br>系統登入驗證失敗，無法使用此功能|

### 「尋找車輛」個案強韌圖  
![Alt text](findCarRA.png "尋找車輛使用個案強韌圖")

### 「尋找車輛」個案活動圖  
![Alt text](findCarAD.png "尋找車輛使用個案活動圖")

### 循序圖    
![Alt text](sequenceDiagram.png)
### 「車機系統」介面藍圖  
![Alt text](介面藍圖_車機系統.jpg)
### 「駕駛行為」介面藍圖  
![Alt text](介面藍圖_駕駛行為.jpg)
### 「尋車系統」介面藍圖  
![Alt text](介面藍圖_尋車系統.jpg)
### 「客戶登入UI」介面詞彙  
![Alt text](介面詞彙_客戶登入UI.png)
### 「駕駛行為UI」介面詞彙  
![Alt text](介面詞彙_駕駛行為UI.png)
### 「尋找車輛UI」介面詞彙  
![Alt text](介面詞彙_尋找車輛UI.png)
### 使用者個案之行為狀態機圖  
![Alt text](login status diagram.png)
![Alt text](drive status diagram.png)
![Alt text](findcar status diagram.png)
### 車機APP之行為狀態機圖  
![Alt text](app status diagram.png)
### 「客戶登入」使用者個案之類別圖  
![Alt text](login type.png)
### 「查看駕駛行為」使用者個案之類別圖  
![Alt text](drive type.png)
### 「尋找車輛」使用者個案之類別圖  
![Alt text](findCar type.png)
### OCL描述產生的 Java 程式碼
### 以客戶登入為例
![Alt text](ocl.PNG)
### 駕駛行為APP之實體類別圖
![Alt text](駕駛行為APP之實體類別圖.png)
### MDA轉換-PIM 轉 EJB PSM 與 Java Code
### 以「查看駕駛行為」為例
### 類別 Driving_behavior 轉成樣板類別
![Alt text](mda.PNG)
### 駕駛行為APP之元件圖  
![Alt text](元件圖.png)
### 目的：

1. 車險費用能有公平的計算方式  
    費用方面，我們會依照駕駛的里程數進行費用的調整，如：在一年內行駛距離較長者，費用方面就會比一般的費用較高，反之，距離較少者費用就會較低，這是一種使用者付費的觀念。

2. 使用較低保費改正不良駕駛習慣  
    訂定較低的保費方案，如果駕駛人達成上述的優良駕駛規則，就可以使車險的保費減少，從這當中就可以改正駕駛的不良行為，在交通方面也能有所改善。  

3. 想要掌握駕駛行為  
    掌握駕駛人的駕駛行為，可以判斷出駕駛是否是一位優良駕駛，而從保險公司的角度來看，可選擇公司裡的優良客戶，藉此可降低公司的營運風險。

4. 保險理賠方面能有正確判斷  
    若駕駛人發生意外，這時保險公司就會進行理賠程序，在判斷哪位駕駛人應負的責任較大時，可使用我們所收集的資料來模擬駕駛人當時行車的狀況，因此在理賠方面做出最正確的判斷。
### 系統分析期末報告影片：
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/HLdQXPL2COs/0.jpg)](http://www.youtube.com/watch?v=HLdQXPL2COs)
### 系統分析Demo影片：
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/BnOATvSWMqE/0.jpg)](http://www.youtube.com/watch?v=BnOATvSWMqE)
### 工作分配表：
![Alt text](工作分配表.png)
