# memes.com

丟一個迷因角色（迷因庫或自己上傳）＋ 比一個動作（鏡頭拍或上傳動作樣本）→ 角色做出同樣的動作。每個角色 × 每個動作各生成一張，可打包 zip 下載。

線上版：https://biangdang007.github.io/memes/

## 怎麼用
1. 貼上你的 Gemini API key（存在你自己的瀏覽器，不經任何伺服器）。取得方式：https://ai.google.dev/gemini-api/docs/api-key
2. 點迷因庫的圖或上傳角色。
3. 開鏡頭拍幾個動作，或上傳動作樣本照片。
4. 按「生成一連串」。

## 技術
- 純靜態單頁 `index.html`，GitHub Pages 部署。
- 角色庫：imgflip 公開 API。
- 人臉綠框：MediaPipe Tasks Vision FaceDetector（瀏覽器端）。
- 生成：Google Gemini `gemini-3.1-flash-image`，多張參考圖＋文字指令 → 新圖。影像輸出沒有免費額度（2026-10-01 查證：約 $0.045～$0.067 一張，看解析度）。
- 本機預覽：`python3 -m http.server 8000`
