# 2019CVFX_Homework5_Team5

## multi-view images
## image alignment results
## multi-view 3D visual effects
## image processing
## bonus
### Live Photo

Live Photo 是 iphone 中一個有趣的功能，顧名思義就是一張 「活的照片」，它能夠呈現出宛如影片一般的效果。
它的產生方式是在按下快門的那個瞬間，自動連拍數張照片，如此一來除了可以從中挑選出滿意的照片，
更能製作成動態桌布，或轉成 GIF 方便分享給親朋好友。 <br>

在這次的作業中。我們總共使用三種不同的方式來實作這個特效。第一種是直接使用 iPhone 內建的 Live Photo 功能，
第二種是藉由 google 提供的 Motion Still App，第三種是直接用 feature matching 的方式實現。

我們利用 feature extraction 分別識別出多張照片中 「移動」 與 「靜止」 的物體，並將靜止的部分取全部照片的平均
(或使用第一張當作背景)，而移動的部分則逐張播放，如此一來就能製造出宛如影片一般的效果。 <br>

以下我們將比較用 Live Photo、Motion Still、和 Feature Matching 產生出來的結果，並進行一些分析比較。
我們總共使用四組不同的照片來進行實驗，他們彼此之間的差異性很大。
第一組照片是馬路上機車移動的畫面。照片中物體的移動速度很快、移動距離也很遠。 <br>
第二組照片是校園中樹木被風吹拂的樣子，前景、背景的輪廓不太明顯，不容易識別，且移動的幅度不大。 <br>
第三組是在室內取景，光線較為明亮，景物與相機的距離也很近，跟其他照片的差異在於，移動的是相機，而不是物體本身。 <br>
第四組同樣是在室內拍攝的，前景與背景的區別很大，容易分割。 <br>


| iPhone Live Photo    | <img src="./Images/lp1.gif" width="165" height="230"> | <img src="./Images/lp2.gif" width="165" height="230"> | <img src="./Images/lp3.gif" width="165" height="230"> | <img src="./Images/lp4.gif" width="165" height="230"> | 
| :--------:           | :--------:                                            | :--------:                                            | :--------:                                            | :--------:                                            |
| **Motion Still**     | <img src="./Images/ms1.gif" width="165" height="230"> | <img src="./Images/ms2.gif" width="165" height="230"> | <img src="./Images/ms3.gif" width="165" height="230"> | <img src="./Images/ms4.gif" width="165" height="230"> |
| **Feature Matching** | <img src="./Images/ms1.gif" width="165" height="230"> | <img src="./Images/ms2.gif" width="165" height="230"> | <img src="./Images/ms3.gif" width="165" height="230"> | <img src="./Images/ms4.gif" width="165" height="230"> |