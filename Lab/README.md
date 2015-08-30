# AIS3 Lab

#### 讓 MT7681 連上 [MediaTek Cloud Sandbox](https://mcs.mediatek.com/oauth/zh-TW/signup)
##### 1. 註冊 MCS 帳號
前往 [MCS 註冊頁面](https://mcs.mediatek.com/oauth/zh-TW/signup) 申請一個帳號

##### 2. 建立產品原型
- 點擊畫面上方的 開發
- 在產品原型清單頁面中，點擊創建按鈕來新增一個新的產品原型。

![](https://img.mediatek.com/1500/mtk.linkit/mcs-resources/zh-TW/2.8.5/LinkIt_Connect/img_linkitconnect7681_01.png)

- 輸入自訂產品原型名稱，版本，並選擇產業別。硬體平台請選擇 MT7681，之後點擊儲存按鈕。
![](https://img.mediatek.com/1500/mtk.linkit/mcs-resources/zh-TW/2.8.5/LinkIt_Connect/img_linkitconnect7681_02.png)

##### 3. 為產品原型建立資料通道
- 點擊剛新建好的產品原型下方的詳情按鈕。
![](https://img.mediatek.com/1500/mtk.linkit/mcs-resources/zh-TW/2.8.5/LinkIt_Connect/img_linkitconnect7681_03.png)

- 點擊資料通道分頁，並點擊新增按鈕。
![](https://img.mediatek.com/1500/mtk.linkit/mcs-resources/zh-TW/2.8.5/LinkIt_Connect/img_linkitconnect7681_05.png)

- 建立資料通道，資料通道 ID 請輸入 `GPIO_00`，資料通道名稱輸入 `GPIO 00`，並且選擇 GPIO 資料型態並儲存
![](https://img.mediatek.com/1500/mtk.linkit/mcs-resources/zh-TW/2.8.5/LinkIt_Connect/img_linkitconnect7681_06.png)

- 接著以同樣步驟新增第二個資料通道，這次資料通道 ID 請輸入 `GPIO_01`，資料通道名稱輸入 `GPIO 01` ，選擇 GPIO 資料型態並儲存

##### 4. 更新晶片上的韌體
- 開啟我的電腦->右鍵內容->裝置管理員，找到 COM 連接埠的編號 (例如下圖為 COM3)
![](http://i.imgur.com/e3gd0kW.png)

若找不到，請下載並安裝 [VCP Driver](http://www.ftdichip.com/Drivers/VCP.htm)

- 執行提供的 mt7681_uploader.py 或 mt7681_uploader.exe，依照上個步驟所找到的 COM 編號，輸入對應參數，例如 `mt7681_uploader.exe -c COM3 -f MT7681_sta_header.bin` 來更新韌體
![](http://i.imgur.com/JdAGs4J.png)

等待韌體更新完畢，若過程中出現 Enter Recovery Mode Failed 相關訊息，請手動按一下晶片上的重置按鈕，再按下鍵盤上的任意鍵繼續執行
