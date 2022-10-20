# VideoFaceStyleTransfer_MethodResearch




Video1：DualStyleGAN 會針對每個frame的人臉做face alignment，可以看到右上方格中的人頭一直在變換角度。<br>
而右下方格轉換後的影片，髮流等細微結構一直在跳動，很不連續<br>

<div align=center>
  <img src="https://user-images.githubusercontent.com/99737139/196706791-2e826d98-f838-434c-846f-03105cff73b5.mp4" height="500">
</div>

Video2：VToonify 的效果很流暢<br>
<div align=center>
  <img src="https://user-images.githubusercontent.com/99737139/196706870-2e5b9d0d-e2cc-422f-b4ea-2e95582bb913.mp4" height="500">
</div>





DualStyleGAN 轉換後的影片會忽略人臉周圍的其他部位（例如：手指、吸管）<br>
<div align=center>
  <img src="https://user-images.githubusercontent.com/99737139/196706941-c49d83f9-c788-4384-9412-7c5b05730d19.mp4" height="500">
</div>

VToonify 保留了手和吸管（雖然有點透明化）<br>
<div align=center>
  <img src="https://user-images.githubusercontent.com/99737139/196707020-6a8c4ccb-54d6-47ee-9ea8-72131abfc3f2.mp4" height="500">
</div>

DualStyleGAN的轉換過程 <br>
<div align=center>
<img src="data/dualstylegan.jpg" width=800>
</div>

<img src="data/dualstylegan_without_alignment.jpg" width=800>
