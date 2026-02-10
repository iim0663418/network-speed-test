# 網路診斷工具

基於 NDT7 協定的網路連線品質測試工具

## 功能特色

- 真實 TCP 指標：MinRTT、重傳率、抖動、緩衝延遲
- 雙向測試：下載與上傳速度完整分析
- 智能評分：綜合評估網路品質（A+ 到 D）
- 無障礙設計：符合 WCAG 2.2 Level AA 標準
- 全球節點：自動連接最近的 M-Lab 測試伺服器

## 線上使用

訪問：https://yourusername.github.io/network-speed-test/

## 技術架構

### 核心技術

- NDT7 協定：M-Lab 的 Network Diagnostic Tool v7
- WebSocket：即時雙向通訊
- TCP BBR：現代擁塞控制演算法

### 測試指標

| 指標 | 說明 |
|------|------|
| 下載/上傳速度 | 實際傳輸速率 (Mbps) |
| MinRTT | 物理延遲底線 (ms) |
| 重傳率 | 數據損耗百分比 |
| Jitter | 連線穩定度 (ms) |
| Buffer Bloat | 緩衝排隊延遲 (ms) |

## 評分標準

```
總分 100 分：
- 下載速度 (40%)
- 上傳速度 (20%)
- 延遲 (20%)
- 數據損耗 (20%)

評級：
A+ (90+) | A (80+) | B+ (70+) | B (60+) | C (50+) | D (<50)
```

## 本地開發

```bash
# 克隆專案
git clone https://github.com/yourusername/network-speed-test.git

# 開啟檔案
open index.html
```

## 特別感謝

此專案使用以下開源技術：

- NDT7 - Measurement Lab (M-Lab) - Apache License 2.0
- M-Lab Locate API - Measurement Lab - Apache License 2.0
- ipapi.co - IP 地理位置服務
- TCP BBR - Google - BSD/GPL v2

## 授權

MIT License

## 隱私聲明

- 測試資料由 M-Lab 收集並公開發布
- 不收集個人識別資訊
- 詳見 [M-Lab 隱私政策](https://www.measurementlab.net/privacy/)
