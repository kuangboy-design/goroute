# Day-A-GoGo 🎒

一站式生活＆旅遊小工具(放在 iPhone 主畫面當 App 用)。
總入口是 **hub.html**,所有服務從這裡進。

---

## 📦 服務清單

| 檔案 | 服務 | 說明 | 需要設定 |
|------|------|------|----------|
| `hub.html` | **Day-A-GoGo** | 總入口選單(主畫面從這裡進) | 無 |
| `index.html` | **GoRoute** | 定位・天氣・Google 地圖路線導航 | 無 |
| `howgo.html` | **HowGo 吃啥** | 依位置＋料理類型找附近餐廳(OSM) | 無 |
| `services.html` | **Kuang之客棧** | 訂餐廳/飯店/機票(連各大平台) | 無 |
| `gofind.html` | **GoFind 急啊!** | 找最近 廁所/超商/ATM/藥局/加油站 | 無 |
| `songyou.html` | **SongYou 爽旅** | AI 即興行程(依位置/天氣/旅伴/年齡) | **需 Groq 免費金鑰** |
| `tickets.html` | **GoTicket** | 演唱會/球賽售票快訊＋開賣倒數 | 無 |
| `gosplit.html` | **GoSplit 麥走!** | 分帳 AA・小費・各付各的 | 無 |
| `goexchange.html` | **GoExchange** | 即時匯率換算 | 無 |
| `wear.html` | **今天穿什麼** | 依天氣建議穿搭、帶傘提醒 | 無 |
| `air.html` | **AirGo 不臭** | 空氣品質 AQI・PM2.5・UV | 無 |
| `spin.html` | **吃什麼轉盤** | 隨機幫你決定吃什麼 | 無 |
| `gotime.html` | **GoTime 時差** | 台北 vs 各國即時時間/時差 | 無 |
| `goconvert.html` | **GoConvert** | 長度/重量/溫度/鞋碼尺寸換算 | 無 |
| `go2go.html` | **Go2Go 怎麼去** | 建立行程→存地點(加入時驗證地址)→AI 比較 A→B 交通(地鐵/公車/計程車/步行)+ Google 地圖實際路線;可**一鍵載入東京親子遊範例** | **需 Groq 金鑰**(與 SongYou 共用) |

輔助檔:`manifest.json`(PWA 設定,指向 hub)、`tw-districts.js`(GoRoute 縣市/區資料)。

---

## ⬆️ 上傳清單(全部上傳到 GitHub repo)

```
hub.html
index.html
howgo.html
services.html
gofind.html
songyou.html
tickets.html
gosplit.html
goexchange.html
wear.html
air.html
spin.html
gotime.html
goconvert.html
go2go.html
manifest.json
tw-districts.js
appicon-180.png
appicon-512.png
```

> README.md 可上傳也可不傳(不影響網站)。

---

## 🚀 部署(GitHub Pages)

1. 到 GitHub repo → **Add file → Upload files** → 拖入上面所有檔案 → **Commit changes**。
2. **Settings → Pages** → Source 選 **Deploy from a branch** → Branch `main` /(root)→ Save。
3. 等約 1 分鐘,網址會是:`https://<帳號>.github.io/<repo>/hub.html`

---

## 📱 加到 iPhone 主畫面

1. Safari 開 **`.../hub.html`**
2. 分享 □↑ → **加入主畫面** → 取名 Day-A-GoGo → 加入
3. 之後點圖示直接進總入口,所有服務一頁選。

---

## 🔑 SongYou 爽旅 的 AI 金鑰(每台裝置各自設定一次)

1. 到 **https://console.groq.com/keys** 註冊/登入(免費、免信用卡)
2. **Create API Key** → 複製(`gsk_` 開頭)
3. 在 SongYou「AI 設定」貼上 → 儲存(只存在該裝置瀏覽器,不在程式碼裡)

---

## ℹ️ 備註

- 多數服務 **免金鑰**:天氣/空品用 open-meteo、地點用 OpenStreetMap(Overpass/Nominatim)、匯率用 open.er-api.com、地圖與訂位/售票以連結方式開啟 Google 地圖或各官方平台。
- **隱私/儲存**:GoSplit、SongYou 金鑰、GoTicket 追蹤清單等都存在「該裝置的瀏覽器」,不會上傳、換裝置不同步。
- **定位**:iPhone Safari 需 HTTPS 才能取得位置(GitHub Pages 已是 HTTPS)。
- **法律**:GoTicket 僅查詢與開賣提醒,不自動搶票。
- 行程/搜尋結果為參考,實際營業時間、票價、交通與安全請再確認。
