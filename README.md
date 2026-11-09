# HTML 小測溫習

學生溫習用的靜態網頁，有 50 題選擇題。

- **溫習 50 題**：每題下面有「顯示答案」按鈕，可以看答案和解析。最上面有「顯示全部答案」按鈕。
- **隨機刷 20 題**：每次從題庫隨機抽 20 題，每題 A–D 的次序也會隨機排列，並自動計時。交卷後會顯示答對題數、用時，以及每道錯題的正確答案和解析。之後可以「再刷 20 題」或「重做錯題」。

網頁是響應式設計，電腦、平板和手機（最窄 320px）都可以正常瀏覽和刷題。

## 檔案

```
index.html      網頁本身（題目資料已經寫在檔案裏面）
images/         第 11–20 題的圖片（q11.png … q20.png）
```

## 用 GitHub Pages 發佈

1. 在 GitHub 新增一個 repository，例如 `html-quiz`，設定為 Public。
2. 把 `index.html` 和整個 `images` 資料夾上傳到 repository 的最上層。可以在網頁版按 **Add file → Upload files**，然後把檔案拖進去。
3. 打開 **Settings → Pages**。
4. 在 **Build and deployment** 的 Source 選擇 **Deploy from a branch**，Branch 選擇 `main`，資料夾選擇 `/ (root)`，然後按 **Save**。
5. 等一至兩分鐘，網址會顯示在同一頁，格式是 `https://你的帳戶名.github.io/html-quiz/`。

直接連到 `…/html-quiz/#practice`，網頁會一打開就進入刷題模式。

## 修改題目

題目資料在 `index.html` 裏 `const QUESTIONS = [...]` 這一行。每題的格式如下：

- `n`：題號
- `q`：題目，用反引號包住的文字會顯示成程式碼
- `img`：圖片路徑，沒有圖片就寫 `null`
- `opts`：A–D 四個選項
- `ans`：正確答案，0=A，1=B，2=C，3=D
- `exp`：解析
