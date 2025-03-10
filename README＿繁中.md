# 網路釣魚 (Phishing) 郵件範例

這份儲存庫收錄了我於 **2025 年 2 月 15 日**實際收到的一封 **釣魚郵件 (Phishing Email)**。該郵件自稱來自「Wintermute Trading」，並試圖攻擊我所屬的組織。我分享此範例供 **教育與資安研究參考**，請勿將其用於任何非法用途。

---

## 1. 概觀

- **聲稱寄件者：** Wintermute Trading `<partnerships@wintermute.com>`
- **實際寄送來源：** 不同網域 (例如： `srv1862.main-hosting.eu` 或 `wintermute.business`)
- **主旨：** **Wintermute & Scallop.io**
- **目的：** 誘導收件者相信這封郵件為專業的做市商邀請，進而點擊可疑連結或加入釣魚 Telegram 群組。

該郵件運用偽造的寄件地址、專業化的排版，以及對真實公司名稱的參考，來降低收件者的戒心。

---

## 2. 原始檔案

- [Wintermute & Scallop.io.eml](https://github.com/djchrisssssss/phishing-email-example/blob/main/Wintermute%20%26%20Scallop.io.eml)

可以使用任意郵件客戶端或文字編輯器，開啟此 `.eml` 檔案以檢視 **完整的郵件標頭** 與 **HTML 內容**。  
部分個人或機敏資訊可能已被隱藏以保護隱私。

---

## 3. 釣魚郵件關鍵跡象

1. **可疑的郵件標頭**  
   - **DMARC 驗證失敗：** 顯示標頭使用的網域 (`wintermute.com`) 與實際寄件網域不符。  
   - **SPF 通過但 DMARC 失敗：** 攻擊者透過中繼或 Google Groups 等方式，規避部分垃圾郵件篩選。

2. **品牌假冒**  
   - 郵件運用真實公司的 Logo 與名稱，讓外觀顯得專業且更具欺騙性。

3. **惡意連結**  
   - 郵件內附加邀請至 Telegram 群組 (`https://t.me/+xxxxxx`)，可能用於詐騙或收集個資。

4. **寄件網域與實際路徑不符**  
   - 表面上顯示 `@wintermute.com`，但實際郵件路徑（envelope sender 或中繼資訊）卻指向其他網域（例如 `main-hosting.eu`）。

---

## 4. 分析與識別方法

1. **檢查原始郵件標頭**  
   - 在 Gmail 或其他郵件客戶端中使用「顯示原始郵件」(或類似功能) 來比對：  
     - **「From」欄位** 與 **「Envelope-From」**  
     - **SPF、DKIM、DMARC** 等驗證結果  
   - 若發現不匹配或 DMARC 驗證失敗，即應提高警覺。

2. **驗證網域真實性**  
   - 若「From」欄位的網域與實際寄件伺服器不同，往往是重大警訊。

3. **謹慎面對連結**  
   - 千萬不要在未核實前就點擊 Telegram 邀請或不明網址，應透過官方管道或公司網站核實。

4. **注意假冒行為**  
   - 攻擊者時常複製官方品牌元素來提高可信度。若有疑問，務必透過該企業正式對外管道再次求證。

---

## 5. 延伸閱讀

- [Google 支援：如何處理釣魚郵件](https://support.google.com/mail/answer/8253)
- [Phishing.org：釣魚攻擊基礎](http://www.phishing.org/)
- [DMARC 官網](https://dmarc.org/) — 瞭解如何防止郵件網域被假冒

---

## 6. 聲明

本儲存庫與其中郵件範例僅供教學與資安研究使用，**請勿**將此內容或技術用於違法或不道德行為。處理任何可疑郵件時，務必遵循最佳實務及組織政策，確保資訊安全。
