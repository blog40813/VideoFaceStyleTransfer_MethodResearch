# Training
  <br>
  
 **準備資料集** :利用DualStyleGAN所提供之find_face功能，從影片當中擷取人臉，建立資料庫，並使用waifu2x做Super-Resolution

<br> 

<img src = data/summerize1_0_006750_overview.jpg width = "30%" align= left >
<div style = ="text-align: center;">
  <img src = data/summerize2_0_006750_overview.jpg width = "30%" style="display: block; margin-left: auto; margin-right: auto;" >
  <p style = "text-align:center;"> 共準備了146張圖片作為dataset </p>
</div>

<br><br><br><br><br><br>

**漸進式訓練階段**：DualStyleGAN的訓練是分階段性，依據階段不同StyleTransfer的效果也不同
<br>
<img src = data/stage.png width = "35%" >
<br>

**訓練結果**：因設備GPU記憶體不足等問題，可以發現自行訓練結果較接近`stage 1`
<br><br>
<img src = data/training.png width = "35%" >
<br><br><br>

**對參數進行微調**：調整外部結構以及內部結構之參數，比較生成圖片之差異
`Ws = 結構參數 Wc = 顏色及細節參數 `
<br><br>
<img src = data/adjust.png width = "35%" >
<br><br><br>


# VideoFaceStyleTransfer_MethodResearch

Video1：DualStyleGAN 會針對每個frame的人臉做face alignment，可以看到右上方格中的人頭一直在變換角度。<br>
而右下方格轉換後的影片，髮流等細微結構一直在跳動，很不連續<br>

https://user-images.githubusercontent.com/99737139/196706791-2e826d98-f838-434c-846f-03105cff73b5.mp4

Video2：VToonify 的效果很流暢<br>

https://user-images.githubusercontent.com/99737139/202955691-52b22935-7c61-4301-99e1-ec6fe8e263d3.mp4


Video3：DualStyleGAN 轉換後的影片會忽略人臉周圍的其他部位（例如：手指、吸管）<br>

https://user-images.githubusercontent.com/99737139/196706941-c49d83f9-c788-4384-9412-7c5b05730d19.mp4

Video4：VToonify 保留了手和吸管（雖然有點透明化）<br>

https://user-images.githubusercontent.com/99737139/202954566-815955f1-ab6f-46d2-8c14-83969d82b68e.mp4


DualStyleGAN的轉換過程 <br>
<div align=center>
<img src="data/dualstylegan.jpg" width=1000>
</div>

<img src="data/dualstylegan_without_alignment.jpg" width=800>

結合 MediaPipe Selfie Segmentation 的功能：將人物與背景分離並換上其他背景，但我們發現邊緣處理不是很好

https://user-images.githubusercontent.com/99737139/202954740-b18e882a-8c18-4171-8bcf-0259931b8b70.mp4


https://user-images.githubusercontent.com/99737139/202955436-8382c872-90c4-4b31-8ce0-7d78229d313e.mp4




