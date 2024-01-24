# 維京崛起輔助器

## 重要 !!!

```
resource/static 的測試環境為 1920 x 1080，模擬器採全螢幕
不同環境可能會導致抓取圖片失敗
建議使用 ui.exe 的功能重新抓取圖片
```

## 使用說明

1. 點擊 game.exe
2. 點擊 ui.exe
3. 設定好後點選開始


## 相關檔案

* game.exe
    * 負責操作模擬器，玩家可透過 log 進行偵錯
* ui.exe
    * 負責設定遊戲操作方式，操作方式請見下方 `ui.exe 介面說明`
* resource
    * 圖片讀取處，若自行截圖，請放置於此
    * static
        * 此處放置預先抓取的圖片

## game.exe

* 接收來自 ui.exe 的訊息，並迴圈運行欲操作之指令
    * e.g. 
        * 欲操作指令
            自動登入、產兵、貢獻
        * 模擬器
            自動登入 -> 產兵 -> 貢獻 -> 自動登入 -> 產兵 ...

## ui.exe 介面

### 遊戲頁面

* 模擬器選單
    * 選擇欲控制之模擬器，目前支援`雷電、逍遙、bluestacks`
* 控制方式
    * 前台: 模擬器不可背景運作 (支援模擬器: `雷電、逍遙、bluestacks`)
    * 後台: 模擬器可於背景運作 (支援模擬器: `雷電`)
* 模擬器標題
    * 填入欲控制之模擬器視窗名稱 (e.g: 雷電模擬器)
* 抓圖
    * 跳轉至抓圖頁面
* 自動
    * 採集: 獲取資源 (ObtainResource.bmp)
    * 收取: 
    * 幫助3: 協助公會成員建設 (TribeAssist.bmp)
    * 產兵3: 自動產兵 (不限兵種)
    * 打怪(第一隊): 
    * 公會捐獻4: 公會 -> 科技 -> 選有金色讚的 -> 貢獻 (1次)
* 被登出時自動登入
    * 不用: 不自動登入
    * Google:
    * IGG:
    * FB:
* 採集
    * 伐木場:
    * 採石場:
    * 金礦場:
* 下一次採集等待時間
* 派出/滿隊
* 戰鬥失敗 line 通知
    * Token:
* 目前狀態
* 開始時自動抓圖
    * 點擊開始後，會自動抓取所有圖片 (只會執行一次)
* 上一頁
    * 跳轉至上一個模擬器設定
* 開始
    * 通知 game.exe 開始控制模擬器
* 暫停
    * 通知 game.exe 停止控制模擬器
* 下一頁
    * 跳轉至下一個模擬器設定
* 新建
    * 新建一個模擬器設定，並跳轉至該設定頁面
* 刪除
    * 刪除當下模擬器設定，並跳轉至下一個設定頁面

### 抓圖頁面

* 返回
    * 返回至遊戲頁面
* 截圖 (1)
    * 功能:
        * 玩家可自行選擇擷取範圍
    * 保存路徑:
        * 截圖結果保存路徑，支援相對路徑和絕對路徑
            * 相對路徑的起始位置為 game.exe 所在位置
    * 使用方式:
        1. 輸入保存路徑
        2. 點擊截圖
        3. 滑鼠點選欲擷取範圍之左上及右下
* 截圖 (2)
    * 功能:
        * 擷取圖片並保存至 resource
        * 選單名稱與 resource 下的圖片名稱一一對應
        * 保存格式: bmp
    * 使用方式
        1. 選擇欲擷取之圖片
        2. 將遊戲畫面跳轉至該圖片所在之畫面，詳情請見下方`圖片說明`
        3. 點擊截圖

### 圖片說明

* profile
* home
* setting
* manageCharacter
* createCharacter
* redConfirm
* blueCancel
* guideAndHelp
* recruit
* train
* tribeAssist
* obtainResource
* obtainResourceOK
* tribe
* technology
* goldGood
* donateChances
* exit
* exit2
* exit3
* exit4
* back
* back2
* back3
* speedup
* gameIcon
* restartIcon

### 聯絡方式

email: kruztw@gmail.com