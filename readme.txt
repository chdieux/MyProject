===僅適用Windows 7以上作業系統===
*當前版本編譯平台對象為Windows 10 TH2 (1511)，若安裝於Windows 7/8/8.1/10上可能會有不預期的問題。

===版本1.2===

1. 檔案內容：
.\Dictionary
- array30_27489.dic（常用漢字含Unicode擴充A字元）
- array30_ExtB.dic（Unicode擴充B字元）
- array30_ExtCD_V2012A.dic（Unicode擴充C/D字元）
- array30_Ext E_V2016A.dic（Unicode擴充E字元）
- array30_phrases.dic（詞輸入）
- array30_shortcodes.dic（一、二級簡碼）
- array30_specialcodes.dic（特別碼提示）
- array30_symbols.dic（符號表）
- array30_tips.dic（關聯字詞）
- array30_kana.dic(日文假名)
.\X64
- Array30IME.dll
- Array30Prop.exe
- PhraseEditor.exe
.\X86
- Array30IME.dll
- Array30Prop.exe
- PhraseEditor.exe
.\
- history.txt
- Install.exe
- readme.txt
- vcredist_x64.exe
- vcredist_x86.exe

2. 安裝說明：
需具備系統管理者權限。
由於安裝程式無數位簽章，可能會被防毒軟體擋下或干擾安裝過程，建議先關閉防毒軟體再進行安裝。
========
首次安裝
========
執行Install.exe。若系統內無Visual C++ 2015 Update 2 runtime，則會先行安裝runtime後再註冊輸入法。
安裝後若工作列沒有顯示本輸入法，從控制台中的地區和語言設定選項進行新增。

========
解除安裝
========
從控制台中的地區和語言設定選項移除本輸入法後，再執行Install.exe反註冊登錄。
若無法正確解除安裝導致無法重新安裝成功（登錄項目被鎖定），可手動刪除下列機碼後再執行安裝程式：
HKEY_CLASSES_ROOT\CLSID\{20542D44-31FC-4662-A561-0722A33FC823}

====
更新
====
進行上述解除安裝步驟後，登出使用者再重新登入，執行Install.exe進行安裝。
若無法順利進行安裝，重新開機後再執行Install.exe完成安裝。
安裝後若工作列沒有顯示本輸入法，從控制台中的地區和語言設定選項進行新增。

3. 功能說明
- 包含所有行列定義的輸入方式：
  行列字根顯示
  Unicode中日韓統一表意文字擴充A/B/C/D/E字元(Unicode 8.0)
  *?查詢鍵（查詢功能不含擴充B/C/D/E字元及少數非擴充B/C/D/E字元的罕用字）
  詞輸入
  符號輸入（W+數字鍵）
  關聯片語（直接以數字鍵選擇）
  日文假名輸入（Alt+`切換）
  顏文字輸入（日文假名輸入模式下鍵入KAO）
  絵文字輸入（WW+數字鍵1~8）(Unicode 8.0)
- 按Shift或Ctrl+Space（Windows內建）鍵切換中英輸入。
- 按Shift+Space鍵切換全形半形。
- 按Space／'鍵代表該字／詞的按鍵已輸入完畢。
  出現重複字／詞時，再加按Space鍵，即將第一個重複字／詞送上。
  若選單超過一頁，則按Space鍵為換頁。選單支援方向鍵/PageUp/PageDown/Home/End鍵操作。
  發生上述情況，可以Enter鍵送上目前選取的重複字（僅查詢鍵或符號輸入會有這種情形）。
  關聯片語可設定Space鍵為換頁或上字。
- 按照行列輸入法的規格，查詢鍵為左邊Shift+8(*)或/(?)鍵，按右邊Shift+8或/仍會正常輸出英數的*或?。
  *跟?不併存。如果已用了*，後面就不接受?，如果已用了?，後面就不接受*。
  問號可以有好幾個，但星號規定只能用一個。
  *放在前面的意義是，使用者接下來所敲的1到3個字根鍵，不管次序都合於期望。
  *放在前面之外的位置，所代表的意義是多種未確定鍵位查詢，當然有時也可能僅代表一種查詢。
  ?可以用來代替四個字根鍵的任何一個，也可以同時用多個?，最多可以連續打四個問號。
- 關聯片語只能以數字鍵選擇，若繼續輸入或是按Space（候選詞未超過一頁時）/Enter鍵則會忽略該字的關聯片語。
- Windows 8內建之（新）細明體、微軟正黑體可正常顯示大部份字元，Windows 7需替換為Windows 8字型檔，否則無法正常顯示Unicode擴充C/D字元。
  目前所有版本的Windows均尚未內建Unicode擴充E字元，請自行下載安裝。
- 可使用內附的使用者造詞工具自行建立詞庫，並可在控制台內設定欲使用的詞庫。
- 可使用內附的使用者造詞工具自行編輯相關字詞。自訂相關字詞至少要有一個項目，否則本輸入法將自動使用內建的相關字詞。若不需要相關字詞功能，請從設定對話視窗中清除該選項。
- Windows 10下新版控制台無法設定非內建輸入法，請使用舊版控制台（視窗鍵上點選滑鼠右鍵，從右鍵選單中選取控制台），或於工作列右側的中英輸入狀態圖示上點選右鍵選單進行設定。

***Dvorak鍵盤選項使用時機：
- 使用Dvorak實體鍵盤
- 手動或以程式修改Scancode Map登錄：
  HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layout機碼下的Scancode Map機碼值
- 以下列方式更改正體中文（適用所有正體中文的輸入法）的預設鍵盤對應方式：
  執行regedt32.exe，
  找到HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts\00000404機碼，將Layout File機碼值由KBDUS.DLL更改為：
  - Dvorak雙手鍵盤：KBDDV.DLL
  - Dvorak右手鍵盤：KBDUSR.DLL
  - Dvorak左手鍵盤：KBDUSL.DLL
  重新開機。
配合更改鍵盤對應方式後仍可以原鍵位（盲打）使用行列輸入法，其他情況勿更改為Dvorak鍵盤對應方式。

4. 已知問題
- 注音查詢功能不支援不以COM啟用本輸入法的應用程式。
  此功能由作業系統內建的Microsoft輸入法提供，必須使用COM。
- 在暗黑破壞神III中輸入無法自動上字。
  這是該遊戲的問題，請使用Space鍵、Enter鍵或數字鍵選擇輸出字元後再繼續輸入。
- 在不使用輸入法內建候選清單的應用程式中，若輸入鍵組合並無候選字／詞，候選清單不會關閉且內容維持前一個輸入鍵組合的候選字／詞。
- 輸入中鍵入非行列輸入法使用的其他符號鍵時行為不一致。某些應用程式會導致輸入視窗關閉並取消未確定的輸入內容，其他應用程式則維持輸入狀態。
- 在Windows 8.1/10下，部份遊戲會不正確地同時顯示輸入法內建候選清單視窗與遊戲自繪候選清單，或兩者均不顯示。
  這是Windows 8.1/10的問題，Microsoft表示日後會修正。
- 使用者造詞工具僅適用於Windows 8以上的作業系統，在Windows Vista/7下無法顯示圖示。
  這是因為Ribbon UI在這些作業系統上不支援32-bit的圖示，而為了降低執行檔大小，程式並未包含32-bit以外的圖示。
  儘管如此，所有編輯功能仍可正常使用。
- 關閉DWM(Windows 7)時候選清單會造成殘影。
- Windows 10下，若前景應用程式為市集應用程式（如Microsoft Edge瀏覽器）時，工作列右側的中英輸入狀態圖示右鍵選單中的使用者造詞／設定／關於選項無法作用。
- 目前僅有少數應用程式（如Microsoft Word及Microsoft Edge瀏覽器）及作業系統（Windows 8.1及Windows 10）支援彩色絵文字，且仍不支援少部份字元。
  Windows內建的字型中僅Segoe UI Emoji字型可顯示彩色絵文字。