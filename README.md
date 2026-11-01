<img width="1128" height="536" alt="螢幕擷取畫面 2026-11-01 171626" src="https://github.com/user-attachments/assets/ecd53295-0815-4c78-a855-af646aff453e" />

github 連結 
https://elearn2.fju.edu.tw/course/395232/learning-activity#/3168880

youtube 連結 
電腦測試︰https://youtu.be/_ujxnEbuqUk
手機測試：https://youtube.com/shorts/UxZueD0WQl0?feature=share

製作內容
1.	場景與模型： 匯入飛行器與牆面模型，以兩面牆組成一道障礙門，將三道門依序放在航線的中央、右側與左側。攝影機設在飛行器後上方，隨機體移動，讓玩家能看清下一道門的位置。

2.	飛行與碰撞： 使用 AircraftController 控制飛行器在固定高度前進，並以 Box Collider 偵測碰撞。撞牆時，飛行器會後退約半秒，玩家可趁這段時間調整方向，再嘗試穿門。

3.	導演物件與計分 UI： 在每道門中央設置感應區 PassZone。飛行器穿過時，`GateTrigger` 會通知導演物件 GameDirector 更新計數。每道門只計算一次，全部通過後顯示 Gates: 3/3。

4.	音效與輸出： 飛行時循環播放引擎聲，撞牆時播放撞擊聲，成功穿門時播放提示音。專案以 Web 格式建置並上傳至 Netlify，可透過瀏覽器遊玩。

【操作方式】

•	電腦： 按住鍵盤 ← 或 → 左右移動，也可用滑鼠按住遊戲畫面的左半邊或右半邊。

•	手機：按住畫面左半邊向左移動，按住右半邊向右移動。對準門中央後放開，飛行器便會直線前進。
