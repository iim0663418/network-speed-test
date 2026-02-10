# GitHub Pages 部署指南

## 步驟 1：在 GitHub 創建儲存庫

1. 前往 [GitHub](https://github.com/new)
2. 儲存庫名稱：`network-speed-test`
3. 設定為 Public
4. 不要初始化 README（已有本地版本）
5. 點擊 "Create repository"

## 步驟 2：推送到 GitHub

在終端機執行：

```bash
cd /Users/chriswu/GitHub/network-speed-test

# 添加遠端儲存庫（替換 yourusername）
git remote add origin https://github.com/yourusername/network-speed-test.git

# 推送到 GitHub
git branch -M main
git push -u origin main
```

## 步驟 3：啟用 GitHub Pages

1. 前往儲存庫的 **Settings**
2. 左側選單點擊 **Pages**
3. Source 選擇：`Deploy from a branch`
4. Branch 選擇：`main` / `/ (root)`
5. 點擊 **Save**

## 步驟 4：等待部署

- 通常需要 1-3 分鐘
- 部署完成後會顯示網址：`https://yourusername.github.io/network-speed-test/`

## 步驟 5：在 Google Sites 嵌入

在 Google Sites 中：

1. 點擊 **插入** → **嵌入**
2. 選擇 **嵌入程式碼**
3. 貼上以下程式碼：

```html
<iframe 
  src="https://yourusername.github.io/network-speed-test/" 
  width="100%" 
  height="900" 
  frameborder="0"
  style="border: none; border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.1);">
</iframe>
```

## 更新網站

當你修改 `index.html` 後：

```bash
cd /Users/chriswu/GitHub/network-speed-test
git add .
git commit -m "更新描述"
git push
```

GitHub Pages 會自動重新部署（約 1-3 分鐘）。

## 自訂網域（選用）

如果你有自己的網域：

1. 在 GitHub Pages 設定中點擊 **Custom domain**
2. 輸入你的網域（如 `speedtest.yourdomain.com`）
3. 在你的 DNS 設定中添加 CNAME 記錄指向 `yourusername.github.io`

## 疑難排解

### 404 錯誤
- 確認 `index.html` 在根目錄
- 檢查 Branch 設定是否正確

### 樣式跑版
- 確認所有資源使用 HTTPS
- 檢查瀏覽器 Console 是否有錯誤

### WebSocket 連線失敗
- GitHub Pages 支援 WebSocket
- 檢查 M-Lab API 是否正常運作
