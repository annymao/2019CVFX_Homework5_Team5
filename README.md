# 2019CVFX_Homework6_Team5

## multi-view images
## image alignment results
## multi-view 3D visual effects
## bonus
### Live Photo

Live Photo 是 iphone 中的一個常用的功能，與其說它是照片，我覺得稱它為一個3秒的小短片應該更加恰當。
它的效果是可以在按下快門的那個瞬間，自動記錄下3秒內的內容，如此一來除了可以從中挑選出滿意的照片，
更能製作成動態桌布，或轉成 GIF 方便分享給親朋好友。 <br>

在這次的作業中。我們總共使用三種不同的方式來實作這個特效。第一種是直接使用 iphone 內建的 Live Photo 功能，
第二種是藉由 google 提供的 Motion Still App，第三種是直接用 feature matching 的方式實現。

我們利用 feature extraction 分別識別出多張照片中「移動」與「靜止」的物體，並將靜止的部分取全部照片的平均
(或使用第一張當作背景)，而移動的部分則逐張播放，如此一來就能製造出宛如影片一般的效果。 <br>

以下我們將比較用 Live Photo、Motion Still、和 OpenCV 產生出來的結果，並進行一些分析比較。
我們總共使用三組不同的照片來進行實驗，他們彼此之間的差異性很大。第一組照片是馬路機車移動的景觀。
照片中物體移動的速度很快、距離也很遠、前景與背景的分界也不太明顯。
第二組照片是校園中樹木被風吹拂的樣子，前景的輪廓明顯，容易識別，但移動的幅度不大。
第三組是在室內取景，光線較為明亮，景物與相機的距離也很近。


|iPhone|<img src="./Images/motion_still1.gif" width="207" height="276">|<img src="./Images/live_photo2.gif" width="207" height="276">|<img src="./Images/live_photo3.gif" width="207" height="276">|
| -------- | -------- | -------- | -------- |
| **Motion Still**  | <img src="./Images/motion_still1.gif" width="207px" height="276px"> | <img src="./Images/motion_still2.gif" width="207px" height="276px"> | <img src="./Images/motion_still3.gif" width="207px" height="276px"> |
| **Ours**          | <img src="./Images/motion_still1.gif" width="207px" height="276px"> | <img src="./Images/motion_still2.gif" width="207px" height="276px"> | <img src="./Images/motion_still2.gif" width="207px" height="276px"> |