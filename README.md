# Vercel Redirect-Only to ngrok

不含 public/ 靜態資源；所有路由（含 /callback）改寫到 /api/proxy，再代理到 NGROK_TARGET。

## 環境變數
- NGROK_TARGET = https://<你的-ngrok>.ngrok-free.dev

## 部署
1. 匯入到 Vercel 專案
2. 設定環境變數並 Deploy
3. 測試：
   - /callback → 代理到 NGROK_TARGET/callback
   - 其他路由 → 代理到 NGROK_TARGET/<同路徑>
