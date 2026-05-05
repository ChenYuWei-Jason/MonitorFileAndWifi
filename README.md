# MacOS管控軟體

### 專案簡介
1. 能有效做到管控wifi
2. 能偵測政策檔案ITProfile.ini變化

### 功能列表
- 可以偵測ITProfile.ini檔案, Wireless Deny的值變化
  * 如果是Y就是只允許關閉wifi
  * 如果是N就是只允許打開wifi
  * 如果是I就是什麼管控都不做，可開可關
 
### 使用技術
+ 使用`DispatchSourceFileSystemObject`協定，偵測檔案是否：
  + 寫入
  + 刪除
  + 改檔名
+ 使用`CWWiFiClient`:
  + 來變更wifi狀態
  + 偵測wifi狀態變化
+ 使用`SCDynamicStoreSetNotificationKeys`:
  + 使用者有登入有異動的偵測
+ 使用`SCDynamicStoreCopyConsoleUser`:
  + 偵測目前登入者是誰  
