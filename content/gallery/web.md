---
title: "My Personal Web"
date: 1999-11-14
draft: false
description: "just record web devlog for myself......"
not_show_date: true
---
## Project goals & milestones
利用免費資源發布自己的網頁，結合cursor和chatGPT發展自己vibe code的技巧，同時透過視覺化和動態展現物理模擬、計算機圖學、以及動畫相關作品。

<br>

## Progress updates
20250405：完成物理和動畫的專案分開放、搜尋、標籤等功能，中英文頁面切換。但目前在顯示post list的地方和tag還沒有將中英文分開。

20250621：將模板換成Hugo，並且將主頁的work experience和education background系統化，並將個人社群頁面加入

20250622：更換experience.html內容以簡化工作經驗，找到更改字體的檔案（themes/erblog/static/self/css/default.css)

20250623：了解各個post的架構，並且上架publication(包含conference的部分）。把work、research、education複製一份到about也沒問題

20250624：解決問題「不知道為什麼journal的部分不能會出問題，再調整看看」（右上角的分頁必須要有對應的content/資料夾/_index.md才可以正常運
作，就算該分頁內的東西放在別的資料夾也一樣），可將three.js檔案內嵌在網頁內。

20250625-27：先決定文字description +內文的字體，設計一下single.html的排版（暫時不用管右邊），撰寫moonshine poster	

20250628：將履歷的專案連接至對應的網頁（利用true “連結” 可以連過去），撰寫moonshine osc

20250629：釐清圖片要如何放進專案裡面。程式在編譯過後會在public裡面開啟一個md file對應的資料夾，內部會有index.html以及其所用到的所有圖片（或是其他檔案）。因此，檔案在html內如果需要被讀取，不論在原始的程式碼內存在哪裡都可以，但檔案的位置就是./<檔名>

20250630-20250701：可以將three.js專案獨立成一個js檔（並且成功import!!）。靜態的物件全部改放至/self/底下。動畫頁面目前完成。新增two stream instability頁面並且從research製作超連結

-20250708：計物導內容完成、計算機圖學內容完成

20250709：Gaussian beam、omniverse

20250710：fdtd、雙眼雙輪平衡車、溫度分析、hhg小年會、泡泡膜實驗、double pendulum、筆記的模板

-20250714：首頁照片和文字完成，插入google analytics tag分析網頁。將projects合併成一頁，並且post前面的顏色代表不同的系列

20250715：新增others（activities, awards, scholarships）、拿掉首頁的categories tags、把focus area 放上三個three.js的框框

20250716：web 3dgs（靜態的、冰箱）、list.html裡面的blog標題在大部分的tags下要拿掉（只留下all, physics, cg, animation有大框框）、Urban fractional是內容的部分、skills

20250727：新增物理和cg的範例專案

20250729：成功把walk cycle放上去

20250730：透過chatGPT分析解決了三個專案的效率問題（物理問題最大：雖然數據沒有無止盡增加，但line跟sphere在loop裡面不斷移除又新增一直在增加storage的使用；cg的還好，微調整理而已；animation的則是先降低fps後）。上架後測試可以正常運行至少10分鐘仍然順暢可控。

-20250804：修復大量bug：heic檔直接改成jpg照片會無法顯示、eular to rk4、cg intensity map to 0~1、animation add light、adjust orbit control、整理tag跟skills以後檢查skills裡面的超連結，對應出去的專案數量是否正確、把pdf的側邊欄收起來、single.html裡面的recent posts拿掉、add 3d to 2d pipeline、備註保密協定、Note照片補上並且確認沒有壞掉

-20250805：新增畫畫的照片

20250807：畫畫、音樂、devlog部分完成。利用not_show_date這個參數隱藏不想設定日期的專案，但依然可以設定date參數使程式按照時間序列排列。修改手機版的nav bar會看不到字的問題（layui-nav-child 的left:0改成right:0）。新增一個map的專案，但要將map放在gallery首頁還是分頁內可以再想想。

20250810：新增去過國家

-20250901：新增四軸直升機動畫和理論、新增games103筆記

20250915：新增ITRI2 playcanvas web viewer的工作項目

20251214：根據fall2026申請資料更新網頁

20251215：冰箱動畫、無人機專案更新

20251223：新增拉塞福散射three.js demo

20260102：新增PIC publication
<br>

## Lessons learned
structure:
layouts
	index.html 首頁
	_default
		baseof.html 首頁初始定義內容
		list.html 用來條列式顯示發佈文章（目前針對不同的分頁已利用if有對應出去不同的模板）
		single.html 每個文章的模板
	partials
		about.html 
		experience.html
		projects_*.html
		publications.html
		head.html <head>
		info.html 用來顯示時間和tags的
		nav.html 最上面的bar

<br>

## Features added, bugs fixed, etc.
1. gallery放照片以及潛水！！！！！超級重要！！
2. Urban fractional 網頁
3. 待PoP論文發表後可以思考一下要如何整合envolope模擬（電漿與雷射交互作用的envolope模擬（optic express, aapps），以及pic模擬（pic模擬（epoch、mai paralleized）），在physics project中。或是乾脆就拿掉放在Publication就好。
4. 物理相關專案（以及研究上的專案）：大三計物導、碩非線性動力學
5. Cg相關專案（以及工作上的專案）：games101筆記、games103筆記
6. 新增網頁點閱人數和地圖上的地點(by google console and google analytics）
7. 瓦力的模型眼睛的地方壞掉，並且打光問題難以處理到一個比較和諧的狀態，因此仍然以maya渲染出來的結果為主
8. 感覺PDE的整理可以在更詳細（參考計物導課本chp 6-9）