# Training Example 01 — POC5 Defense → VP1 Reclaim → Expansion

## 1. Mục tiêu

Training example này ghi lại một chuỗi BTC để AI Trader học cách nhận diện:

**POC5 được test → giá trụ trên POC5 → CVD flip dương → Auction Line reclaim EMA20 → giá mở rộng lên VP1 → VP1 breakout.**

Trọng tâm là **quan sát phản ứng của giá tại POC5**, thay vì vào lệnh chỉ vì một chỉ báo đơn lẻ.

> Quy ước dữ liệu: Khi có `Giá + POC5 + VP1` thì POC5/VP1 được cập nhật. Khi chỉ có giá thì giữ nguyên POC5/VP1 gần nhất.

---

# 2. Chuỗi diễn biến

## Phase A — POC5 bắt đầu được defend

### Snapshot 01

**Giá: 64,153 | POC5: 64,106 | VP1: 64,513**  
**OI: 0% | Flow Type: BeI**  
**CVD: +400**  
**Agg Liq: Long 153K / Short 117K**  
**Auction Line: -333 | EMA20: +100**  
**RSI: 45**  
**VPIN: 0.92**

### Quan sát

Giá test POC5 rồi quay lại 64,153.

Điểm đáng chú ý:

- Giá vẫn nằm trên POC5.
- CVD tăng từ `+124 → +400` trong khi giá gần như không tăng.
- OI gần như flat.
- Auction Line vẫn âm nhưng đang cải thiện.
- EMA20 chuyển sang dương.

=> Đây là **absorption candidate**.

Không vào lệnh chỉ vì CVD dương; cần chờ thêm confirmation.

---

## Phase B — Giá test POC5 nhưng seller chưa phá được value

### Snapshot 02

**Giá: 64,214 | POC5: 64,106 | VP1: 64,513**  
**OI: -0.13% | Flow Type: BuO**  
**CVD: -43**  
**Agg Liq: Long 173K / Short 100K**  
**Auction Line: -187 | EMA20: -1.1K**  
**RSI: 49**  
**VPIN: 0.91**

Giá quay xuống gần POC5.

CVD từ `+391 → -43`, OI giảm.

=> Buyer momentum suy yếu.

Nhưng chưa có breakdown POC5.

**Kết luận:** chưa Short đuổi, chưa Long xác nhận. Chờ phản ứng thật sự tại POC5.

---

## Phase C — POC5 defense được xác nhận

### Snapshot 03

**Giá: 64,150 → 64,153 | POC5: 64,106 | VP1: 64,513**  
**OI: -0.01% | Flow Type: BuO**  
**CVD: +400**  
**Agg Liq: Long 153K / Short 117K**  
**Auction Line: -333 | EMA20: +100**  
**RSI: 45**  
**VPIN: 0.92**

Đây là vùng có thể bắt đầu xây dựng **POC5 Defense setup**, nhưng vẫn cần confirmation.

### Điều kiện Long cần chờ

1. POC5 không bị mất.
2. CVD flip từ âm → dương và tiếp tục tăng.
3. Auction Line co về 0 hoặc flip dương.
4. EMA20 cải thiện.
5. OI không tiếp tục giảm mạnh.

---

# 3. Điểm vào lệnh tốt nhất trong chuỗi

## LONG Setup A — POC5 Reclaim / Absorption

### Trigger

Giá test:

**64,106 POC5**

sau đó reclaim và giữ trên POC5.

Confirmation lý tưởng:

- CVD: âm → dương.
- Auction Line: âm → 0 → dương.
- EMA20: dương.
- OI: BuO → flat hoặc BuI.
- VPIN không tăng mạnh theo hướng panic.

### Entry zone

**64,120–64,180** sau khi POC5 được reclaim và có confirmation.

Không mua chỉ vì giá chạm POC5.

### Stop Loss

**SL: dưới POC5 khoảng 80–120 point**, hoặc dưới swing low thực tế của cú test.

Ví dụ:

**Entry 64,150 → SL khoảng 64,050–64,070.**

Lý do: nếu POC5 bị mất và reclaim thất bại, thesis absorption không còn hợp lệ.

### Take Profit

- **TP1: 64,300**
- **TP2: 64,450**
- **TP3: 64,513 VP1**

Ưu tiên chốt một phần tại TP1/TP2 và để phần còn lại chạy tới VP1 nếu flow tiếp tục xác nhận.

---

# 4. Confirmation thực tế xuất hiện

Sau khi test POC5, giá bật:

**64,450**

### Snapshot 04

**Giá: 64,450 | POC5: 64,206 | VP1: 64,513**  
**OI: -0.15% | Flow Type: BeO**  
**CVD: +90**  
**Agg Liq: Long 379K / Short 585K**  
**Auction Line: +1.4K | EMA20: +500**  
**RSI: 66**  
**VPIN: 0.18**

### Ý nghĩa

Đây là confirmation rất mạnh:

- CVD: `-440 → +90`
- Auction: `731 → 1.4K`
- Auction vượt EMA20.
- Giá phản ứng mạnh từ POC5.
- Short liquidation tăng.

=> **POC5 Defense → Expansion đã được xác nhận.**

### Lưu ý OI

OI vẫn `BeO`.

Vì vậy cú tăng có thành phần **short covering / short squeeze**.

Do đó:

> Đây là confirmation bullish về price/flow, nhưng chưa phải confirmation hoàn toàn của fresh long buildup.

**Không chase tại 64,450** vì VP1 chỉ còn khoảng 63 point.

---

# 5. VP1 Reclaim

### Snapshot 05

**Giá: 64,580 | POC5: 64,206 | VP1: 64,513**  
**OI: -0.16% | Flow Type: BeO**  
**CVD: +242**  
**Agg Liq: Long 475K / Short 1.25M**  
**Auction Line: +2.3K | EMA20: +700**  
**RSI: 68**  
**VPIN: 0.21**

Giá đã vượt VP1.

### Vai trò mới của VP1

**64,513 từ resistance → breakout pivot/support.**

Nếu giá retest 64,513 và giữ được:

=> continuation setup tốt hơn nhiều so với chase ở 64,580.

---

# 6. Value Migration

### Snapshot 06

**Giá: 64,790 | POC5: 64,697 | VP1: 64,513**  
**OI: -0.49% | Flow Type: BeO**  
**CVD: +1K**  
**Agg Liq: Long 792K / Short 2.95M**  
**Auction Line: +6.1K | EMA20: +1.7K**  
**RSI: 74**  
**VPIN: 0.75**

POC5 đã migrate:

**64,206 → 64,697**

Đây là dấu hiệu **value migration upward**.

Nhưng đồng thời:

- RSI 74.
- VPIN 0.75.
- Short liquidation 2.95M.
- OI -0.49%.

=> Bullish expansion rất mạnh nhưng đã nóng.

**Không chase Long tại 64,790.**

Chờ higher-value retest quanh POC5 mới.

---

# 7. Bài học quan trọng nhất

## Pattern cần ghi nhớ

```text
POC5 được test
      ↓
Giá không breakdown
      ↓
CVD âm → dương
      ↓
Auction Line cải thiện
      ↓
Auction Line reclaim EMA20
      ↓
Giá expansion
      ↓
VP1 reclaim
      ↓
POC5 migrate upward
```

Đây là pattern có chất lượng cao hơn việc:

> “Giá chạm POC5 → Long ngay.”

---

# 8. Những lúc CÓ THỂ vào lệnh

## 🟢 Entry Type 1 — POC5 Defense

**Điều kiện:**

- Giá test POC5.
- Không breakdown.
- CVD flip dương.
- Auction Line cải thiện.
- EMA20 hỗ trợ.
- OI không tiếp tục unwind mạnh.

**Entry:** sau reclaim POC5.

**SL:** dưới swing low/POC5 đủ rộng để tránh noise.

**TP:** TP1 local resistance → TP2 → VP1.

---

## 🟢 Entry Type 2 — POC5 Reclaim + Auction Confirmation

Đây là entry an toàn hơn.

Ví dụ:

**POC5 → bounce → CVD + → AL vượt EMA20 → price expansion.**

Có thể vào sau khi AL xác nhận.

**SL:** dưới POC5 hoặc dưới retest low.

**TP:** VP1.

---

## 🟢 Entry Type 3 — VP1 Breakout Retest

Sau khi VP1 bị reclaim:

**64,513**

không nên FOMO mua ngay.

Chờ:

**Break VP1 → pullback → VP1 hold → flow vẫn bullish.**

**Entry:** retest VP1.

**SL:** dưới VP1/retest low.

**TP:** vùng value mới / POC5 mới / resistance tiếp theo.

---

# 9. Những lúc KHÔNG nên vào

### ❌ Không Long khi:

- RSI đã quá nóng.
- VPIN tăng mạnh.
- Short liquidation đang cực lớn.
- OI vẫn giảm mạnh.
- Giá đã chạy xa khỏi POC5.
- Risk/Reward tới VP1 quá nhỏ.

### ❌ Không Short chỉ vì:

- CVD âm một snapshot.
- OI BuO/BeO.
- Giá pullback về POC5.

Phải có:

**POC5 break + failed reclaim + flow confirmation.**

---

# 10. Rút kinh nghiệm cho AI Trader

### Rule 01 — POC5 là vùng phản ứng, không phải nút BUY/SELL

AI Trader phải quan sát **behavior tại POC5**.

### Rule 02 — CVD cần đọc theo chuỗi

Một giá trị CVD đơn lẻ ít có ý nghĩa.

Quan trọng hơn:

**CVD - → 0 → +**

hoặc:

**CVD + → 0 → -**

### Rule 03 — Auction Line + EMA20 là confirmation

Auction Line tăng nhưng chưa vượt EMA20:

→ chưa đủ.

Auction Line test/reclaim EMA20 rồi expansion:

→ confirmation mạnh hơn.

### Rule 04 — OI phải được tách khỏi price/flow

**Price ↑ + CVD ↑ + OI ↓**

không tự động = healthy long buildup.

Có thể là:

> **Short covering / short squeeze.**

### Rule 05 — Liquidation phải xác định bên nào bị ép

**Short liquidation lớn → bullish squeeze**

**Long liquidation lớn → bearish unwind**

nhưng không được dùng Agg Liq đơn độc.

### Rule 06 — VPIN cho biết mức độ stress

VPIN thấp:

→ reaction thường orderly hơn.

VPIN cao:

→ cần cảnh giác với liquidation/stress/exhaustion.

### Rule 07 — Value migration rất quan trọng

Nếu:

**giá tăng + POC5 migrate upward**

→ market đang chấp nhận value cao hơn.

Nếu:

**giá tăng nhưng POC5 không theo**

→ cần cảnh giác với price expansion chưa được market acceptance xác nhận.

### Rule 08 — POC5 cho ta LOCATION. Flow confirmation cho ta ENTRY.

---

# 11. Checklist Live cho AI Trader

Mỗi khi giá tiến vào POC5:

```text
Giá: ______ | POC5: ______ | VP1: ______
OI: ______ % | Flow Type: ______
CVD: ______
Agg Liq: Long ______ / Short ______
Auction Line: ______ | EMA20: ______
RSI: ______
VPIN: ______
```

Sau đó hỏi:

### A. Price

- Giá trên hay dưới POC5?
- POC5 đang giữ hay bị phá?
- POC5 có migrate không?

### B. Flow

- CVD đang tăng hay giảm?
- Auction Line đang tăng hay giảm?
- AL đang trên hay dưới EMA20?

### C. Positioning

- OI tăng hay giảm?
- Flow Type là BuI / BeI / BuO / BeO?
- Có phải fresh positioning hay liquidation/unwind?

### D. Stress

- VPIN thấp hay cao?
- Agg Liq bên nào bị ép?

### E. Entry

Chỉ vào khi:

**Level + Price Action + Flow + Positioning**

cùng tạo đủ confirmation.

---

# 12. Kết luận Training Example 01

### Setup chất lượng cao nhất

> **POC5 test → không breakdown → CVD flip → Auction reclaim EMA20 → price expansion.**

### Entry ưu tiên

**POC5 reclaim/retest**, không chase expansion.

### TP chính

**VP1**, sau đó đánh giá breakout và value migration.

### SL

Đặt dưới **POC5/swing low** và phải được xác định trước entry.

### Core lesson

> **Không dự đoán phản ứng tại POC5. Chờ market chứng minh POC5 đang được defend.**

---

# 02.md — Training Example 02
## BTC 5m — POC5 Defense → CVD Flip → Auction Expansion → POC5 Migration → VP1 Test

> Tổng kết chuỗi ATS bắt đầu từ 64,370 / POC5 64,416.
> Các mức SL bên dưới là training reference suy ra từ cấu trúc quan sát, không phải lệnh đã thực thi.

## 1. Chuỗi diễn biến

### 01 — Initial decision zone
- Giá 64,370 | POC5 64,416 | VP1 64,962
- OI +0.23% BeI | CVD -58
- Agg Liq Long 55K / Short 819K
- Auction Line -875 | EMA20 -900
- RSI 52 | VPIN 0.85

**Đọc:** Giá dưới POC5, CVD âm nhẹ, BeI nhỏ. Short liquidation lớn cho thấy short covering nhưng chưa phải fresh long. Auction chưa xác nhận.
**Action:** WAIT. Không Long trước POC5 reclaim; không Short đuổi khi squeeze/liquidation còn lớn.

### 02 — POC5 test lần 1
64,510 → test POC5 → 64,457.
- OI 0% BeI | CVD -174
- Agg Liq 57K / 1M
- Auction -500 / EMA20 -520
- RSI 57.5 | VPIN 0.86

**Đọc:** POC5 chưa acceptance; CVD xấu hơn nhưng OI gần như không tăng. Short liquidation rất lớn.
**Action:** WAIT.

### 03 — POC5 + Auction EMA20 defense
- Giá 64,490
- OI -0.01% BeO | CVD -172
- Agg Liq 22K / 830K
- Auction -416 / EMA20 -500
- RSI 62.5 | VPIN 0.86

**Đọc:** Giá test POC5 đồng thời Auction Line test EMA20; cả hai được giữ. BeO nhẹ, CVD cải thiện.
**Action:** Bullish Lean, nhưng WAIT CVD confirmation.

### 04 — Defense lần 2
64,440 → Auction Line test EMA20 -500 → 64,485.
- OI -0.09% BeO | CVD -247
- Agg Liq 14K / 826K
- Auction -400 / EMA20 -500
- RSI 60 | VPIN 0.79

**Đọc:** POC5 defense + Auction EMA20 defense lần 2. CVD vẫn là điểm chưa xác nhận; OI BeO và VPIN hạ nhiệt.
**Action:** Bullish Lean / WAIT CVD flip.

### 05 — Expansion bắt đầu
64,660 → POC5 migrate 64,630 → pullback 64,550 → 64,678.
- OI -0.53% BeO | CVD +847
- Agg Liq 170K / 1M
- Auction +1,300 / EMA20 -200
- RSI 78 | VPIN 0.88

**Đọc:** CVD flip mạnh; Auction reclaim EMA20; POC5 migrate lên. OI vẫn BeO nên move còn mang màu sắc short covering.
**Entry signal:** Long confirmation sớm quanh POC5 mới ~64,630 sau confirmation/retest, không chase.
**TP:** VP1 64,962.
**SL reference:** dưới POC5/đáy defense gần nhất; invalidation khi price acceptance dưới POC5.

### 06 — Continuation nhưng nóng
- Giá 64,740 | POC5 64,694
- OI -0.23% BeO | CVD +1,200
- Agg Liq 388K / 1.18M
- Auction +2,100 / EMA20 0
- RSI 81.6 | VPIN 0.92

**Đọc:** POC5 tiếp tục migrate; CVD và Auction tăng mạnh. OI vẫn BeO, short covering còn lớn.
**Action:** BULLISH HOLD / DO NOT CHASE. Entry mới ưu tiên retest POC5 64,694.

### 07 — Áp sát VP1
- Giá 64,921 | POC5 64,914
- OI -0.04% BeO | CVD +2,300
- Agg Liq 660K / 2.55M
- Auction +4,800 / EMA20 +800
- RSI 84 | VPIN 0.81

**Đọc:** POC5 migrate liên tục 64,416 → 64,630 → 64,694 → 64,914. CVD +2.3K, Auction/EMA20 cùng migrate lên, VPIN hạ nhiệt.
**Action:** Bullish expansion nhưng không chase. VP1 chỉ còn ~41 điểm. Chờ VP1 acceptance hoặc retest POC5.

### 08 — VP1 test + BuI
- Giá chạm VP1 64,962 | POC5 64,914
- OI +0.35% BuI | CVD +2,400
- Agg Liq 860K / 3.57M
- Auction +6,500 / EMA20 +1,000
- RSI 87.1 | VPIN 0.16

**Đọc:** Price ↑ + CVD ↑ + OI ↑ + BuI: fresh long participation rõ hơn sau giai đoạn short covering. Auction tiếp tục expansion, VPIN giảm mạnh.
**Action:** Bullish / VP1 decision zone. Không chase tại điểm chạm; chờ acceptance.

### 09 — VP1 rejection/pullback về POC5
- Giá 64,848 | POC5 64,914
- OI +0.33% BuI | CVD +2,100
- Agg Liq 861K / 3.57M
- Auction +5,900 / EMA20 +1,500
- RSI 75.4 | VPIN 0.16

**Đọc:** Giá từ VP1 64,962 lùi về 64,848, hiện dưới POC5 ~66 điểm. Nhưng OI vẫn BuI, Auction vẫn bullish, VPIN thấp, RSI cooling.
**Action:** Bullish bias / WAIT POC5 reclaim. Chưa kết luận bearish reversal.

## 2. Điểm vào lệnh

### Entry A — POC5 Defense → CVD Flip
**Vùng tham chiếu:** POC5 mới ~64,630.
Điều kiện: POC5 defense lặp lại + Auction Line reclaim EMA20 + CVD flip -247 → +847 + POC5 migrate.
- **Entry:** sau confirmation/retest quanh 64,630.
- **TP:** 64,962 VP1.
- **SL reference:** dưới POC5/đáy defense gần nhất.

### Entry B — Continuation tại POC5 mới
**Vùng:** ~64,694.
Điều kiện: Price > POC5 + CVD tăng + Auction > EMA20.
- **Entry:** retest 64,694 và hold.
- **TP:** 64,962.
- **Lưu ý:** RSI 81.6 + VPIN 0.92 → không market chase.

### Entry C — Sau VP1 acceptance
**Trigger:** reclaim và acceptance trên 64,962.
Cần Price giữ VP1 + CVD dương/tăng + OI BuI + Auction giữ trên EMA20.
VP1 khi đó chuyển từ resistance → support/reference.

## 3. TP / SL framework

**TP chính:** VP1 64,962.

Nếu VP1 acceptance: theo dõi continuation bằng POC5/VP1 mới, không mặc định reversal.

**SL training reference:**
- Aggressive: dưới POC5 đang được defend.
- Structural: dưới đáy cụm POC5/Auction EMA20 defense.
- Hard invalidation: price acceptance dưới POC5 + CVD deterioration + Auction Line mất EMA20.

> ATS không ghi một mức SL thực tế, nên các mức trên chỉ là reference cho training.

## 4. Những chỗ cần tránh vào lệnh

- **64,370:** POC5 chưa reclaim, CVD âm, BeI; chưa có confirmation.
- **Các test POC5 đầu:** chưa có CVD flip; không Long chỉ vì “POC5 có vẻ giữ”.
- **Sau short squeeze khi OI còn BeO:** Price ↑ + CVD ↑ + OI ↓ có thể là short covering, chưa phải fresh long.
- **64,678–64,740:** RSI 78–81.6, VPIN cao → bullish nhưng R:R entry mới xấu; chờ retest.
- **64,921 sát VP1:** VP1 chỉ còn ~41 điểm → chờ acceptance/retest.
- **Short ngược trend chỉ vì RSI >80:** overbought không phải Short trigger.
- **Short ngay khi chạm VP1:** cần rejection được xác nhận bằng Price + CVD + OI + Auction.

## 5. Core Training Lessons

1. **POC5 Defense phải được chứng minh**, tốt nhất qua nhiều lần test/hold.
2. **Price test POC5 và Auction Line test EMA20 đồng thời** tạo confluence rất đáng chú ý.
3. **CVD Flip** là turning point: -247 → +847.
4. Phân biệt:
   - Price ↑ + CVD ↑ + OI ↓ + BeO → nghiêng short covering/deleveraging.
   - Price ↑ + CVD ↑ + OI ↑ + BuI → fresh long participation rõ hơn.
5. **POC5 Migration**: 64,416 → 64,630 → 64,694 → 64,914 = value migration upward.
6. **VP1 là decision zone**, không tự động là TP hay reversal.
7. **RSI >80 không phải Short signal**; dùng để tránh chase.
8. **VPIN đo intensity/stress, không tự xác định direction.**
9. Entry tốt hơn theo chuỗi: **Defense → Confirmation → Reclaim → Retest → Continuation.**

## 6. Pattern Name

### POC5 Defense → Auction EMA20 Defense → CVD Flip → Auction Expansion → POC5 Migration → VP1 Test → BuI Confirmation

**Core rule:**
> Không dự đoán POC5 sẽ giữ. Chờ POC5 được defend, Auction xác nhận, CVD flip và value migrate rồi mới nâng conviction.

**Anti-FOMO rule:**
> Expansion càng mạnh và RSI/VPIN càng nóng, càng ưu tiên retest/acceptance thay vì chase giá.

---

# 03.md — Training Example 03
## BTC 5m — POC5/VP1 Breakout → Extreme Expansion → Deleveraging → Auction Breakdown → Reset

> Phần tiếp nối sau Training Example 02. Tách thành 03.md vì đây là một market episode mới, có pattern riêng và có giá trị training độc lập.

## 1. Chuỗi diễn biến

### 01 — Breakout continuation
- Giá 64,955 | POC5 64,914 | VP1 64,962
- OI +0.39% BuI | CVD +1.3k
- Agg Liq Long 1.63M / Short 7.81M
- Auction +6.5k | EMA20 +2.7k
- RSI 71.4 | VPIN 0.30

**Đọc:** POC5 reclaim sau pullback; CVD recover; OI vẫn BuI; Auction mở rộng; VPIN cooling.
**Action:** Bullish continuation. Entry ưu tiên quanh POC5/retest, không chase sát VP1.

### 02 — VP1 breakout + POC5 migration
- Giá lên 65,200 → về 65,026
- POC5 mới 65,026
- OI 0% BuI | CVD +2.7k
- Agg Liq Long 3.93M / Short 11.48M
- Auction +8.5k | EMA20 +4.2k
- RSI 76 | VPIN 0.62

**Đọc:** VP1 64,962 đã breakout; POC5 migrate lên 65,026; giá retest đúng POC5. CVD tăng. OI chưa còn expansion nhưng chưa chuyển bearish.
**Action:** Bullish POC5 retest. Không chase 65,200; chờ POC5 hold.

### 03 — Expansion tiếp tục
- Giá 65,384 | POC5 65,026
- OI +0.81% BuI | CVD +1.7k
- Agg Liq Long 6.2M / Short 15.8M
- Auction +12.7k | EMA20 +7.2k
- RSI 74.7 | VPIN 0.74

**Đọc:** POC5 hold sau breakout; OI chuyển lại BuI mạnh; giá tiếp tục expansion. CVD giảm từ 2.7k xuống 1.7k nhưng vẫn dương. Liquidation và VPIN tăng.
**Action:** Bullish expansion, nhưng hạn chế chase do volatility tăng.

### 04 — Extreme expansion
- Giá 66,630 | POC5 mới 66,475
- OI +1.40% BuI | CVD +6.5k
- Agg Liq Long 81M / Short 139M
- Auction +42k | EMA20 +20k
- RSI 89.3 | VPIN 0.64

**Đọc:** POC5 migrate 65,026 → 66,475; Price > POC5. Price ↑ + OI ↑ + BuI + CVD ↑ + Auction ↑ = fresh-long/aggressive-buying confirmation rất mạnh.
**Risk:** RSI 89.3 và liquidation cực lớn.
**Action:** Trend cực bullish nhưng không chase. Nếu có Long, ưu tiên quản trị lợi nhuận; entry mới chờ POC5 retest.

### 05 — Peak expansion / deleveraging
- Giá lên nhẹ 70,450 → sau đó 68,230
- POC5 mới 68,298
- OI -1.03% BeO | CVD +22.3k
- Agg Liq Long 338M / Short 378M
- Auction +64.3k | EMA20 +35k
- RSI 89 | VPIN 0.03

**Đọc:** POC5 migrate 66,475 → 68,298; giá chỉ thấp hơn POC5 68 điểm. CVD tăng cực mạnh nhưng OI chuyển từ +1.40 BuI sang -1.03 BeO.
**Interpretation:** Price/CVD/Auction vẫn bullish trong khi OI co mạnh. Phù hợp với deleveraging/short covering hơn là fresh-long expansion.
**Action:** Bullish structure vẫn còn; không Short chỉ vì BeO/RSI 89. Không chase; chờ POC5 68,298 hold/reclaim.

### 06 — Reset / Auction breakdown
- Giá 67,835
- POC5 mới 67,984 | VP1 mới 68,298
- OI -0.35% BuO | CVD +10.8k
- Agg Liq Long 273M / Short 263M
- Auction -900 | EMA20 +44.5k
- RSI 46.4 | VPIN 0.19

**Đọc:** Giá mất POC5 68,298 và nằm dưới POC5 67,984 lẫn VP1 68,298. RSI reset 89 → 46.4. CVD vẫn dương nhưng giảm 22.3k → 10.8k. OI đổi BeO → BuO, cho thấy positioning đang được đóng/release, chưa phải Bear In.
**Critical change:** Auction +64.3k → -900, trong khi EMA20 vẫn +44.5k. Auction breakdown rõ, nhưng nền EMA20 chưa reset.
**Action:** NEUTRAL/WAIT. Không bắt đáy tại 67,835. Chờ POC5 67,984 reclaim hoặc rejection được xác nhận.

## 2. Pattern chính
**POC5 Breakout → Value Migration → Retest → Fresh BuI Expansion → Extreme Expansion → Deleveraging → Auction Breakdown → Momentum Reset**

Đây là pattern khác với 02.md và nên giữ thành training example riêng.

## 3. Entry đáng chú ý
- **Entry A:** POC5 65,026 sau VP1 breakout, khi POC5 migrate và CVD/Auction xác nhận.
- **Entry B:** POC5 65,026–65,384 khi POC5 hold và OI BuI/CVD dương.
- **Entry C:** Không ưu tiên market entry tại 66,630; RSI 89.3 và liquidation cực lớn → chờ POC5 66,475 retest/hold.
- Sau khi Price mất POC5/VP1 và Auction breakdown: **WAIT**, không bắt đáy.

## 4. Những chỗ cần tránh
1. Chase 65,200 sau breakout.
2. Chase 66,630 khi RSI 89.3.
3. Short chỉ vì RSI 89.
4. Short chỉ vì OI BeO tại 68,230 khi Price/CVD/Auction vẫn bullish.
5. Long 67,835 khi Price dưới POC5 và VP1, Auction đã breakdown.
6. Long chỉ vì CVD vẫn dương tại 67,835.
7. Long/Short chỉ dựa trên OI flow mà bỏ qua Price structure.

## 5. Core Lessons
1. POC5 migration là evidence của value migration/acceptance khi được Price và CVD hỗ trợ.
2. Price ↑ + OI ↑ + BuI + CVD ↑ = fresh-long/aggressive-buying mạnh.
3. Price ↑ + CVD ↑ + OI ↓/BeO sau expansion lớn có thể là deleveraging/short covering, chưa tự động bearish reversal.
4. RSI 89 không phải Short signal; chủ yếu là cảnh báo không chase.
5. Auction Line có thể breakdown trước khi EMA20 reset.
6. Auction -900 trong khi EMA20 +44.5k = short-term flow breakdown nhưng nền EMA20 còn cao; cần chờ cấu trúc mới.
7. Price structure có quyền phủ nhận OI signal.
8. BuO không đồng nghĩa Bear In: BuO vẫn là OI giảm, thiên về đóng/release bull-side positions.
9. Khi Price < POC5 < VP1 và Auction mất EMA20, ưu tiên WAIT thay vì bắt đáy.
10. Sequence: **Breakout → POC5 migration → Retest → Confirmation → Expansion → Deleveraging → Reset → Reclaim/Reject decision.**

## 6. Pattern Rule
> Trong expansion, đi theo POC5 migration; khi expansion cực trị, không chase. Khi OI chuyển BeO nhưng Price/CVD/Auction vẫn tăng, ưu tiên diễn giải deleveraging trước khi gọi reversal. Khi Price mất POC5 + VP1 và Auction breakdown, chuyển sang WAIT cho đến khi cấu trúc mới được xác nhận.

> Các mức Entry/SL/TP trong file là training references, không phải lệnh đã thực thi.

---

# 04.md — Training Example: POC5 Reclaim → Acceptance → Bullish Expansion

**Thư mục:** Training examples  
**Mục đích:** Ghi nhận một chuỗi thực chiến để AI học cách nhận diện POC5 reclaim, acceptance, continuation, exhaustion/high-intensity và điều kiện vào/không vào lệnh.

> **Lưu ý dữ liệu:** Đây là kinh nghiệm rút ra từ chính chuỗi snapshot đã quan sát trong phiên. Các mẫu Entry/TP/SL bên dưới là **execution template để AI tham khảo**, không phải kết quả backtest hay tỷ lệ thắng đã được kiểm chứng. Chỉ những kết quả sau khi có thực tế xác nhận mới được nâng thành kinh nghiệm thống kê.

---

## 1. Bối cảnh chuỗi

Điểm bắt đầu của training example là vùng giá quanh **71.5k**, khi cấu trúc trước đó còn bearish và giá đang ở dưới POC5.

Snapshot mở đầu:

- Giá: **71,525**
- POC5: **72,366**
- VP1: **70,700**
- OI: **+0.21% BeI**
- CVD: **-1.9k**
- Auction Line: **-200**
- EMA20 Auction: **600**
- RSI: **43**
- VPIN: **0.24**

Đọc trạng thái:

- Bearish positioning còn hiện diện.
- CVD vẫn âm.
- Auction Line dưới EMA20.
- RSI dưới 50.
- Giá dưới POC5.
- Chưa có cơ sở Long.

**State:** Bearish Structure + CVD Absorption Attempt.

Không Long chỉ vì CVD bắt đầu hồi; cần chờ lực và cấu trúc cùng xác nhận.

---

# 2. Chuyển đổi quan trọng: Bearish → Bullish Reclaim

Sau đó xuất hiện displacement:

**71,300 → 72,610**

POC5 mới được kéo lên:

**72,295**

Snapshot:

- OI: **+0.08% BuI**
- CVD: **+361**
- Agg Liq: Long **8M**, Short **13.6M**
- Auction Line: **3.7k**
- EMA20: **1.2k**
- RSI: **60**
- VPIN: **0.40**

### Dấu hiệu chuyển regime

Đây là lần đầu chuỗi có sự đồng thuận rõ:

- Giá tăng mạnh.
- BeI → **BuI**.
- CVD âm → **dương**.
- Auction Line vượt EMA20.
- RSI vượt 50.
- Giá xuyên POC5 và tạo POC5 mới cao hơn.

**State:** Bullish Reclaim → Acceptance Test.

### Bài học cho AI

Không gọi đây chỉ là relief bounce khi đồng thời xuất hiện:

`Price ↑ + BuI + CVD > 0 + AL > EMA20 + RSI > 50 + POC5 được reclaim`

Short liquidation lớn có thể đóng góp vào displacement, nhưng nếu CVD và BuI cũng xác nhận thì không nên quy toàn bộ move cho short squeeze.

---

# 3. Không Long ngay sau displacement

Sau cú kéo 71,300 → 72,610, giá lùi:

**72,100**

với:

- BuI +0.08%
- CVD +361
- AL 3.7k > EMA20 1.2k
- RSI 60
- VPIN 0.40

Kết luận đúng:

**Bullish, nhưng không chase.**

Lý do:

- Displacement đã lớn.
- Giá đang cách xa vùng origin.
- VPIN bắt đầu cao.
- POC5 mới 72,295 là vùng có thể dùng để kiểm tra acceptance.

### Quy tắc training

> **Sau breakout mạnh, ưu tiên chờ POC5 retest/acceptance thay vì mua đuổi.**

---

# 4. Bullish reclaim bị stress — nhưng chưa bearish

Giá về **71,990**.

Snapshot:

- OI: **-0.18% BeO**
- CVD: **-728**
- AL: **3.5k**
- EMA20: **1.8k**
- RSI: **54**
- VPIN: **0.42**

### Điểm quan trọng

CVD:

**+361 → -728**

Nhưng OI:

**BuI → BeO**

Không được đọc BeO giống BeI.

- **BeI:** bearish positioning vào.
- **BeO:** bearish positioning thoát.

Vì vậy đây là:

**Bullish Reclaim Under Stress**, chưa phải Bearish Continuation.

Auction vẫn trên EMA20 và RSI vẫn trên 50.

### Bài học

Một CVD âm đơn lẻ không đủ đảo state nếu:

- cấu trúc chưa mất POC5,
- Auction chưa mất EMA20,
- RSI chưa mất 50,
- OI đang BeO thay vì BeI.

---

# 5. Reclaim được xác nhận lần hai

Giá lên **72,681**.

Snapshot:

- OI: **+0.27% BeI**
- CVD: **+600**
- AL: **7.3k**
- EMA20: **7.0k**
- RSI: **55**
- VPIN: **0.46**
- Short liquidation: **11M**

Đây là trạng thái đối kháng:

### Bullish

- Giá trên POC5.
- CVD dương.
- AL > EMA20.
- RSI >50.

### Cảnh báo

- BeI xuất hiện ngay vùng cao.
- VPIN tăng.
- Short squeeze còn hiện diện.

**State:** Bullish Acceptance + Bear In Counterflow.

### Bài học

Khi `Price ↑ + CVD ↑ + BeI ↑`, không được tự động kết luận bearish. Phải quan sát xem Bear In có thắng được giá/flow hay bị hấp thụ.

---

# 6. POC5 retest: setup quan trọng nhất

Giá:

**72,950 → POC5 72,295**

Snapshot tại vùng test:

- OI: **-0.07% BuO**
- CVD: **+350**
- AL: **6.2k**
- EMA20: **6.5k**
- RSI: **41**
- VPIN: **0.43**

### Ý nghĩa

Giá quay lại POC5 từ phía trên.

Đây là **Acceptance Test**.

Tại test:

- BuO thay BeI → bearish positioning không tiếp tục mở.
- CVD vẫn dương.
- AL chỉ vừa dưới EMA20.
- RSI yếu mạnh → chưa được Long ngay.

### Quy tắc

**POC5 retest không tự động = Long.**

Cần có phản ứng xác nhận:

1. Giá giữ trên POC5.
2. CVD không chuyển âm sâu.
3. OI không chuyển sang BeI mạnh.
4. Auction Line reclaim/giữ EMA20.
5. RSI phục hồi về trên 50 hoặc có recovery rõ.

---

# 7. Confirmation sau POC5 retest

Giá bật lên:

**73,250**

Snapshot:

- OI: **-0.04% BeO**
- CVD: **+1k**
- AL: **8.2k**
- EMA20: **6.3k**
- RSI: **69**
- VPIN: **0.88**

### Confirmation

POC5 **72,295 giữ được**.

Đồng thời:

- BuO/BeO thay vì BeI.
- CVD +350 → +1k.
- AL 6.2k → 8.2k và vượt EMA20.
- RSI 41 → 69.

**State:** Bullish Acceptance → Bullish Expansion.

### Nhưng không chase

VPIN **0.88** và RSI **69** cho thấy move đã rất nóng.

Direction bullish ≠ entry tốt tại market.

---

# 8. POC5 tiếp tục nâng giá trị — Bullish Expansion

Giá:

**73,300**

POC5 mới:

**73,185**

Snapshot:

- OI: **+0.26% BuI**
- CVD: **+2k**
- Agg Liq: Long **12M**, Short **11M**
- AL: **10.1k**
- EMA20: **6.9k**
- RSI: **72**
- VPIN: **0.83**

### Đây là confirmation mạnh nhất của chuỗi

Value đã dịch chuyển:

**POC5 72,295 → 73,185**

Giá đứng ngay trên POC5 mới.

Đồng thời:

- BuI.
- CVD +2k.
- AL > EMA20 rõ.
- RSI >70.
- POC5 được nâng lên.

**State:** Bullish Expansion — High Intensity.

---

# 9. Chữ ký tín hiệu Bullish POC5 Reclaim

AI nên ghi nhớ chữ ký sau:

```text
Bearish/weak structure
        ↓
CVD bắt đầu hồi
        ↓
Price displacement
        ↓
POC5 bị reclaim
        ↓
BuI xuất hiện
        ↓
CVD > 0
        ↓
Auction Line > EMA20
        ↓
RSI > 50
        ↓
POC5 được giữ trong retest
        ↓
CVD tiếp tục tăng
        ↓
POC5 nâng lên
        ↓
Bullish Acceptance / Expansion
```

Đây là mẫu **high-quality bullish continuation** khi các tầng đồng thuận.

---

# 10. Dấu hiệu có thể vào LONG

## Setup A — POC5 Reclaim

### Điều kiện

- Giá reclaim POC5.
- CVD chuyển từ âm → dương hoặc tăng rõ.
- BuI xuất hiện hoặc bearish positioning không tăng thêm.
- Auction Line vượt EMA20.
- RSI >50.
- Break được giữ thay vì rejection.

### Entry

Ưu tiên:

**POC5 retest từ phía trên + reaction xác nhận.**

Không ưu tiên market-buy ngay sau một displacement lớn.

### SL

Ưu tiên đặt **dưới vùng POC5/retest low**, hoặc dưới cấu trúc đã xác nhận nếu khoảng cách hợp lý.

Không đặt SL máy móc ngay sát POC5 nếu volatility/VPIN đang cao.

### TP

Ưu tiên theo cấu trúc:

- **TP1:** recent high / liquidity phía trên.
- **TP2:** high mới nếu breakout được xác nhận.
- **TP3:** vùng giá trị mới nếu POC5 tiếp tục dịch lên.

Trong chính case này:

- POC5 72,295 → recent high 72,950.
- Sau đó 73,250.
- POC5 mới 73,185 → 73,300 và vùng high tiếp theo.

### Quản trị

Khi TP1 đạt và cấu trúc vẫn Acceptance/Continuation:

- giảm rủi ro,
- dời SL theo cấu trúc,
- không đóng toàn bộ chỉ vì RSI cao nếu flow vẫn đồng thuận.

---

## Setup B — Breakout Continuation

Chỉ cân nhắc khi:

- Giá phá recent high.
- CVD tiếp tục tăng.
- BuI giữ/tăng.
- AL vẫn > EMA20.
- POC5 không bị bỏ lại quá xa hoặc value tiếp tục nâng.

### Entry

Có thể vào theo breakout nếu confirmation đủ mạnh, nhưng chất lượng thường thấp hơn POC5 retest khi VPIN/RSI đã quá nóng.

### Không chase khi

- RSI >70.
- VPIN rất cao.
- Short squeeze đã diễn ra lớn.
- Giá cách POC5 quá xa.

Trong case này, vùng **73,250–73,300** là ví dụ điển hình: bullish direction rất mạnh nhưng chase-risk cao.

---

# 11. Khi KHÔNG vào LONG

## Không vào 1 — Chỉ có CVD hồi

Ví dụ đầu chuỗi:

- CVD -2.5k → -1.9k.
- Giá chưa reclaim POC5.
- BeI vẫn giữ.
- AL dưới EMA20.
- RSI <50.

=> **Không Long.**

CVD divergence/absorption chỉ là cảnh báo, chưa phải entry.

---

## Không vào 2 — Breakout nhưng chưa acceptance

Giá vượt POC5 nhưng:

- CVD không giữ được.
- AL dưới EMA20.
- RSI suy yếu.
- BeI tăng.

=> **WAIT**, chờ retest.

---

## Không vào 3 — POC5 retest nhưng momentum chưa xác nhận

Case:

- Giá về POC5.
- CVD còn dương nhưng giảm.
- AL < EMA20.
- RSI 41.

=> Không mua chỉ vì giá chạm POC5.

Phải chờ reaction.

---

## Không vào 4 — Quá nóng

Các dấu hiệu:

- RSI >70.
- VPIN >~0.8 trong case này.
- Displacement lớn.
- Liquidation/short squeeze vừa xảy ra.
- Giá cách xa POC5.

=> **Không chase.**

Direction có thể vẫn bullish nhưng execution quality thấp.

---

## Không vào 5 — Bullish/Bearish conflict quá lớn

Ví dụ:

- Price ↑
- CVD ↑
- nhưng BeI tăng mạnh.
- AL bắt đầu mất EMA20.
- RSI giảm.

=> Không tự động Long.

Chờ xem Bear In bị hấp thụ hay thắng.

---

# 12. Khi nào chuyển sang SHORT / Bearish Failure

Không Short chỉ vì RSI cao.

Cần có chuỗi xác nhận:

```text
POC5 mất
   ↓
CVD giảm mạnh / âm
   ↓
Auction Line < EMA20
   ↓
RSI < 50
   ↓
BeI xuất hiện/tăng
   ↓
Retest POC5 từ dưới bị rejection
   ↓
Bearish Continuation
```

Đây mới là **bullish acceptance failure** có chất lượng.

Nếu POC5 chỉ bị xuyên nhẹ nhưng CVD/AL/Flow chưa xác nhận bearish → **WAIT**, không Short ngay.

---

# 13. Execution Template cho AI

## LONG — POC5 Acceptance

```text
Scenario:
Bullish Reclaim → POC5 Retest → Acceptance

Entry:
POC5 retest + price reaction + flow confirmation

Confirmation:
CVD ↑ / >0
BuI hoặc không có BeI mới
AL > EMA20
RSI >50 hoặc recovery rõ

SL:
Dưới retest low / cấu trúc invalidation

TP1:
Recent High

TP2:
Breakout High / liquidity phía trên

TP3:
Value expansion / POC5 mới

Avoid:
RSI/VPIN quá nóng + giá quá xa POC5
```

## SHORT — POC5 Failure

```text
Scenario:
Bullish Acceptance Failure

Trigger:
POC5 mất + rejection

Confirmation:
CVD ↓ / âm
AL < EMA20
RSI <50
BeI tăng

SL:
Trên rejection high / cấu trúc invalidation

TP1:
Impulse origin / liquidity gần nhất

TP2:
VP1

Avoid:
Short khi chỉ có một tín hiệu bearish đơn lẻ
```

---

# 14. Thứ tự ưu tiên tín hiệu

AI không được đếm tín hiệu kiểu máy móc. Phải đánh giá mức độ đồng thuận.

## Tier 1 — Cấu trúc

1. POC5 reclaim.
2. POC5 acceptance.
3. POC5 nâng lên.
4. Break + retest.

## Tier 2 — Động lượng

1. CVD direction/change.
2. Auction Line vs EMA20.
3. BuI/BeI/BeO/BuO.
4. RSI.

## Tier 3 — Chất lượng/rủi ro

1. VPIN.
2. Liquidation imbalance.
3. Khoảng cách giá tới POC5.
4. Độ nóng của move.

**Một tầng mạnh không đủ tạo Chất lượng cao; chất lượng cao cần sự đồng thuận giữa các tầng.**

---

# 15. Bài học quan trọng nhất cho AI

## Lesson 01

**Lực thay đổi trước; cấu trúc xác nhận sau.**

CVD/AL/Flow có thể đổi trước khi POC5 được reclaim. Không được gọi đảo chiều chỉ từ momentum.

## Lesson 02

**POC5 reclaim chưa đủ; acceptance mới quan trọng.**

Breakout + retest + giữ POC5 có giá trị hơn một cú wick vượt POC5.

## Lesson 03

**BeI khác BeO.**

- BeI = bearish positioning vào.
- BeO = bearish positioning thoát.

Không được gộp hai trạng thái thành “bearish”.

## Lesson 04

**BuI + CVD dương + AL > EMA20 là tổ hợp bullish rất đáng chú ý khi POC5 đã được reclaim.**

## Lesson 05

**CVD divergence là cảnh báo, không phải entry tự động.**

Case đầu chuỗi cho thấy CVD hồi trong khi giá còn yếu; phải chờ price/structure confirmation.

## Lesson 06

**RSI >70 không tự động là Short.**

Trong bullish expansion, RSI cao có thể phản ánh trend mạnh. Nó chủ yếu cảnh báo execution risk khi kết hợp VPIN cao/displacement lớn.

## Lesson 07

**VPIN cao làm giảm chất lượng của việc chase, không tự động đảo bias.**

## Lesson 08

**Short squeeze có thể khởi động move, nhưng CVD + BuI + Auction expansion giúp phân biệt squeeze đơn thuần với bullish participation tiếp tục.**

## Lesson 09

**POC5 dịch chuyển lên là dấu hiệu value acceptance đang nâng cao.**

Trong case:

**72,295 → 73,185**

đi cùng BuI/CVD/AL expansion → bullish structure được củng cố.

## Lesson 10

**Entry tốt nhất thường là lúc cấu trúc vừa được xác nhận và risk còn kiểm soát được; không nhất thiết là lúc tín hiệu mạnh nhất.**

---

# 16. Chữ ký cần lưu cho các lần sau

```text
SIGNATURE: POC5_RECLAIM_BULLISH_ACCEPTANCE

Precondition:
Bearish/weak structure dưới POC5

Transition:
CVD hồi → Price displacement → POC5 reclaim

Confirmation:
BuI
CVD > 0
AL > EMA20
RSI > 50

Structure:
POC5 acceptance
Retest holds

Expansion:
CVD ↑
AL ↑
POC5 ↑
Price makes new high

Execution:
Prefer POC5 retest
Avoid chase after large displacement

Invalidation:
POC5 loss + CVD deterioration + AL < EMA20 + BeI + RSI <50
```

---

# 17. Execution Decision Tree cho AI

AI cần ưu tiên đọc theo trình tự, không được nhảy thẳng từ một chỉ báo sang quyết định Entry.

```text
                    PRICE / STRUCTURE
                          │
                          ▼
                   POC5 RECLAIM?
                    /          \
                  NO            YES
                  │              │
                  ▼              ▼
              WAIT        POC5 ACCEPTANCE?
                                /       \
                              NO         YES
                              │           │
                              ▼           ▼
                            WAIT     CHECK FLOW
                                         │
                 ┌───────────────────────┼──────────────────────┐
                 │                       │                      │
                 ▼                       ▼                      ▼
               CVD ↑                   OI FLOW                AUCTION
               /  \                    /    \                 /    \
             YES   NO                BuI   BeI              >EMA20 <EMA20
              │     │                 │      │                │      │
              │     └──────► WAIT     │      └──────► WAIT    │      └──► WAIT
              │                       │
              ▼                       ▼
        CHECK RSI              CHECK PRICE
              │                       │
              ▼                       ▼
          >50 / recovery?       ABOVE POC5?
            /       \             /       \
          YES       NO           YES       NO
           │         │            │         │
           ▼         ▼            ▼         ▼
       LONG BIAS    WAIT      LONG BIAS   FAILURE WATCH
```

## Quy tắc quyết định

🟢 LONG

Chỉ nâng lên Long Quality khi:

* POC5 đã reclaim.
* POC5 giữ được trong retest.
* CVD xác nhận.
* OI Flow không chống lại cấu trúc.
* Auction Line xác nhận.
* RSI hỗ trợ.
* Risk/Reward còn hợp lý.

🟡 WAIT

WAIT khi:

* Có tín hiệu bullish nhưng cấu trúc chưa xác nhận.
* POC5 vừa bị reclaim nhưng chưa retest.
* CVD và OI Flow xung đột.
* AL chưa reclaim EMA20.
* RSI/VPIN cho thấy move quá nóng.
* Giá đã đi quá xa POC5.

🔴 SHORT / FAILURE

Chỉ xem xét khi:

* POC5 mất.
* Retest từ dưới thất bại.
* CVD suy yếu rõ.
* AL < EMA20.
* BeI tăng.
* RSI <50.

---

# 18. Kết luận Training Example

Chuỗi này cho AI một mẫu rất rõ về quá trình:

**Bearish Structure
→ CVD Absorption Attempt
→ Bullish Reclaim
→ POC5 Acceptance Test
→ Acceptance Confirmation
→ Bullish Expansion
→ POC5 nâng lên
→ High-Intensity Trend.**

Kinh nghiệm cốt lõi:

> **Không mua vì giá tăng. Không mua chỉ vì CVD dương. Không mua chỉ vì POC5 được chạm.**
> 
> **Ưu tiên khi Price + POC5 + CVD + OI Flow + Auction Flow + RSI cùng xác nhận, sau đó chờ POC5 retest để tối ưu execution.**
> 
> **Khi move đã quá nóng (RSI/VPIN cao, displacement lớn), bias vẫn có thể bullish nhưng hành động đúng có thể là WAIT thay vì chase.**

---

# 19. Case Summary — AI Memory

```text
CASE:
POC5 Reclaim → Retest → Acceptance → Expansion

Initial:
Price dưới POC5
CVD âm
BeI
AL < EMA20
RSI <50

Transition:
Price displacement
CVD → dương
BeI → BuI
AL > EMA20
RSI >50
POC5 reclaim

Retest:
Price quay về POC5
CVD vẫn còn dương
BuO / BeO
Không có Bear In expansion
→ WAIT for confirmation

Confirmation:
POC5 giữ
CVD ↑
AL > EMA20
RSI ↑
→ Bullish Acceptance

Expansion:
BuI
CVD +2k
AL 10.1k > EMA20 6.9k
POC5 72,295 → 73,185
Price 73,300

Final State:
Bullish Expansion — High Intensity

Execution Lesson:
Direction bullish ≠ chase bullish.

Best execution:
POC5 retest + confirmation.

Invalidation:
POC5 loss + CVD deterioration + AL loss + BeI + RSI <50.
```

---

# 20. Checklist trước khi LONG

```text
[ ] Price đã reclaim POC5?
[ ] POC5 đã được acceptance?
[ ] Retest có giữ được không?
[ ] CVD đang tăng hay giảm?
[ ] CVD có >0 không?
[ ] OI Flow là BuI / BuO / BeI / BeO?
[ ] Có Bear In mới không?
[ ] Auction Line đang trên hay dưới EMA20?
[ ] RSI >50 hay <50?
[ ] VPIN có quá cao không?
[ ] Liquidation đang nghiêng bên nào?
[ ] Giá cách POC5 bao xa?
[ ] Đang ở breakout đầu tiên hay đã chạy quá xa?
[ ] Có vùng liquidity/recent high cho TP không?
[ ] SL nằm ở đâu nếu thesis sai?
[ ] R:R có còn hợp lý không?
```

**Quy tắc cuối

Nếu chưa trả lời được câu hỏi “Nếu sai thì cấu trúc sai ở đâu?”, không vào lệnh.

Nếu chỉ có một chỉ báo đẹp nhưng các tầng khác chưa xác nhận, WAIT.

Nếu cấu trúc + flow + momentum cùng xác nhận nhưng VPIN/RSI quá nóng, bias có thể giữ nguyên nhưng execution phải chuyển từ CHASE → WAIT FOR RETEST.**

---

# Status

**Training Example 04 — Draft từ một case thực chiến; chưa phải thống kê backtest.**

Khi có thêm kết quả thực tế sau các setup tương tự, có thể cập nhật:

- số mẫu,
- win/loss,
- MFE/MAE,
- TP đạt được,
- SL bị quét,
- điều kiện nào làm setup thất bại,
- và độ tin cậy của từng chữ ký tín hiệu.

---

# Training Example 05 — POC5 Rejection → Bearish Flow Confirmation

## Mục tiêu

Đây là mẫu thứ 5, tách riêng khỏi 4 pattern đã có trong `01.md` → `04.md`.

Core pattern:

> **POC5 bị reject + flow chuyển bearish**

Mẫu này đặc biệt quan trọng vì nó cho AI Trader biết cách chuyển từ:

> **“Giá chỉ đang test POC5”**

sang:

> **“POC5 đã thực sự bị reject và bearish flow đã xác nhận.”**

---

# 1. Pattern Structure

Chuỗi mẫu điển hình:

```text
Giá hồi lên POC5
        ↓
POC5 test từ phía dưới
        ↓
Không reclaim được POC5
        ↓
Giá bị reject
        ↓
CVD + → 0 → -
        ↓
OI chuyển sang Bear In / bearish positioning
        ↓
Auction yếu / breakdown
        ↓
RSI mất 50
        ↓
Bearish continuation
```

### Core principle

> **POC5 cho ta LOCATION.**
>
> **Reaction cho ta INFORMATION.**
>
> **Bearish flow confirmation cho ta ENTRY.**

---

# 2. Case Study

Chuỗi thực tế:

**76,540 → 77,355 → POC5 77,856 → 76,868**

Trước khi test POC5:

```text
76,540
↓
77,355
↓
test POC5 77,856
```

Sau test:

```text
77,856
↓
76,868
```

=> Giá đã test POC5 từ phía dưới nhưng **không reclaim được**.

Đây mới chỉ là:

> **POC5 rejection candidate**

Chưa đủ để Short ngay.

---

# 3. Flow trước rejection

Snapshot trước khi test:

```text
Price: 77,355
POC5: 77,856

OI: -0.30%
Flow Type: BeO

CVD: +2.2K

Agg Liq:
Long 13.5M
Short 12.6M

Auction Line: 26K
EMA20: 24.6K

RSI: 56
VPIN: 0.16
```

Đọc:

- Price đang hồi.
- CVD tăng.
- AL > EMA20.
- RSI > 50.
- VPIN thấp.
- OI giảm + BeO.

=> Đây là **bullish recovery / short covering**.

Quan trọng:

> Chưa được gọi là healthy long buildup.

Vì:

**Price ↑ + CVD ↑ + OI ↓ + BeO**

có thể là short covering.

Do đó AI Trader phải chờ phản ứng tại POC5.

---

# 4. POC5 Rejection

Giá chạm POC5:

**77,856**

sau đó:

**→ 76,868**

Đây là dấu hiệu đầu tiên:

> **POC5 failed reclaim.**

POC5 đang nằm phía trên giá.

Vì vậy POC5 chuyển từ:

> potential support

thành:

> **resistance / rejection location**

Nhưng chưa được phép Short chỉ dựa trên location.

---

# 5. Flow chuyển bearish

Snapshot sau rejection:

```text
Price: 76,868
POC5: 77,856

OI: +0.03%
Flow Type: BeI

CVD: +25

Agg Liq:
Long 9.8M
Short 8.1M

Auction Line: 24.3K
EMA20: 26K

RSI: 37
VPIN: 0.08
```

Đây là phần quan trọng nhất của training example.

## CVD

Trước:

**+2.2K**

Sau:

**+25**

Chuỗi:

> **CVD + → gần 0**

Buyer flow gần như bị triệt tiêu.

Nếu tiếp tục:

> **+ → 0 → -**

thì bearish confirmation mạnh hơn nữa.

---

## OI

Trước:

> **-0.30% BeO**

Sau:

> **+0.03% BeI**

Đây là regime change:

```text
Short covering
      ↓
OI bắt đầu tăng
      ↓
Bear In
```

=> bắt đầu có evidence của bearish positioning mới.

---

## Auction Line vs EMA20

Trước:

**AL 26K > EMA20 24.6K**

Sau:

**AL 24.3K < EMA20 26K**

Auction momentum đã yếu đi.

Không diễn giải:

> AL < EMA20 = Short

một cách máy móc.

Đúng hơn:

> **Auction confirmation cho bullish continuation đã mất.**

Nếu AL tiếp tục giảm/breakdown cùng CVD và price:

→ bearish confirmation tăng mạnh.

---

## RSI

**56 → 37**

Đây là momentum deterioration rất rõ:

> bullish recovery → bearish momentum.

RSI 37 chưa phải extreme oversold.

Vì vậy vẫn còn room cho bearish continuation.

---

## VPIN

**0.16 → 0.08**

VPIN vẫn thấp.

Điều này rất quan trọng:

> Đây chưa phải panic sell.

Do đó bearish move hiện tại có thể là:

> **controlled bearish transition**

thay vì liquidation cascade.

---

# 6. Entry Quality

## ❌ Không Short ngay tại 76,868

Sau rejection:

**77,856 → 76,868**

giá đã giảm gần 1K.

Short ngay đây có nguy cơ:

> **chase the move**

Location tốt nhất đã ở phía trên.

---

# 7. 🥇 A+ Short Entry — POC5 Retest

Setup tốt nhất:

```text
POC5 77,856
       ↓
Rejection
       ↓
Price giảm
       ↓
Pullback
       ↓
Retest POC5 từ dưới
       ↓
Reject lần nữa
       ↓
Bearish flow confirmation
       ↓
SHORT
```

### Điều kiện ưu tiên

Trong retest POC5:

- Price không reclaim được POC5.
- CVD không phục hồi rõ.
- CVD có thể đi **+ → 0 → -**.
- OI giữ/tăng theo BeI.
- Auction tiếp tục yếu hoặc breakdown.
- RSI không reclaim 50.
- VPIN vẫn orderly hoặc tăng theo stress nếu breakdown bắt đầu.

Đây là:

> **Location + rejection + flow confirmation + retest**

→ chất lượng entry cao.

---

# 8. Entry B — Aggressive

Có thể cân nhắc entry sớm hơn nếu:

- POC5 rejection rất rõ;
- CVD đã mất mạnh;
- OI chuyển BeI;
- Auction breakdown;
- RSI < 50;
- price vẫn gần POC5;
- R:R còn tốt.

Nhưng:

> Entry aggressive phải có risk nhỏ hơn entry A+.

---

# 9. Khi nào KHÔNG vào Short?

## No Entry #1 — Chỉ chạm POC5

```text
Price → POC5
```

nhưng:

- chưa reject;
- CVD vẫn tăng;
- OI không bearish;
- Auction vẫn expansion.

→ **WAIT**

---

## No Entry #2 — Rejection nhưng flow chưa xác nhận

Ví dụ:

```text
POC5 reject
CVD vẫn + mạnh
OI flat
AL > EMA20
RSI > 50
```

→ chưa đủ.

> **Location có, confirmation chưa có.**

→ WAIT.

---

## No Entry #3 — Giá đã dump quá xa

```text
POC5
↓
↓
↓
large dump
```

Nếu đã cách xa POC5:

→ không chase Short.

Chờ pullback/retest.

---

## No Entry #4 — Panic liquidation

Nếu xuất hiện:

- Long liquidation cực lớn;
- VPIN cực cao;
- price dump nhanh;
- RSI extreme.

→ không tự động Short.

Có thể đã ở cuối liquidation leg.

Chờ:

> reset → retest → confirmation.

---

# 10. TP Framework

Không cố định một TP duy nhất.

## TP1

**76,200**

Là reaction low trước đó.

Nếu Short từ vùng retest POC5:

→ TP1 là logical first target.

## TP2

**VP1 = 74,631**

Đây là value reference quan trọng tiếp theo.

Nếu price mất 76,200 và bearish flow tiếp tục:

→ VP1 trở thành target chính.

## TP3

Nếu VP1 cũng bị phá:

→ tìm:

- lower value;
- prior swing;
- Profile Low;
- liquidation/value reset zone.

---

# 11. SL Framework

SL phải đặt tại **invalidation**.

## Short từ POC5 retest

Invalidation:

> **POC5 được reclaim và hold lại.**

SL có thể nằm:

> trên failed-reclaim / rejection high.

Không đặt SL quá sát khiến noise kích hoạt.

Không nới SL khi thesis đã invalidated.

---

# 12. Risk/Reward

Trước entry:

```text
Entry = POC5 rejection retest

SL = trên POC5 / rejection high

TP1 = prior low

TP2 = VP1
```

Chỉ vào khi:

> **Expected R:R đủ tốt.**

Nếu entry đã quá thấp:

> **Không cố Short chỉ vì bearish thesis đúng.**

Thesis đúng không có nghĩa entry ở mọi giá đều tốt.

---

# 13. AI Trader State Machine

```text
STATE 1
Price below POC5
        ↓
WAIT

STATE 2
Price approaches POC5
        ↓
OBSERVE

STATE 3
POC5 rejected
        ↓
WATCH FLOW

STATE 4
CVD + → 0
OI → BeI
AL weak
RSI < 50
        ↓
BEARISH CONFIRMATION

STATE 5
Retest POC5
        ↓
Reject
        ↓
SHORT CANDIDATE

STATE 6
Price reaches TP1
        ↓
Protect position

STATE 7
Price reaches VP1
        ↓
Partial / exit / trail

STATE INVALID
POC5 reclaimed + accepted
        ↓
EXIT SHORT
```

---

# 14. Pattern Recognition Formula

AI Trader có thể nhận diện mẫu bằng logic:

```text
POC5 Test
+
Failed Reclaim
+
CVD Deterioration
+
Bearish OI/Flow
+
Auction Weakening
+
Momentum Weakening
=
Bearish Setup
```

Nhưng:

```text
Bearish Setup
≠
Immediate Market Order
```

Cần thêm:

```text
Good Location
+
Good R:R
+
Retest / Confirmation
=
Entry
```

---

# 15. Checklist cho AI Trader

Trước khi Short pattern này:

- [ ] Giá đang ở dưới POC5?
- [ ] POC5 đã được test?
- [ ] Test từ phía dưới?
- [ ] Reclaim thất bại?
- [ ] Giá đã reject khỏi POC5?
- [ ] CVD có **+ → 0 → -**?
- [ ] OI có chuyển sang BeI?
- [ ] Có bearish positioning mới hay chỉ liquidation?
- [ ] Agg Liq bên nào đang bị ép?
- [ ] Auction đang yếu/breakdown?
- [ ] AL/EMA20 được đọc theo behavior?
- [ ] RSI đã mất 50?
- [ ] VPIN có quá cao không?
- [ ] Giá có đang quá xa POC5 không?
- [ ] Có retest POC5 để entry không?
- [ ] TP1 rõ?
- [ ] VP1/TP2 rõ?
- [ ] SL nằm tại invalidation?
- [ ] R:R đủ tốt?

Nếu chưa đủ:

> **WAIT.**

---

# 16. Training Lesson

Mẫu này phải dạy AI Trader một distinction cực quan trọng:

### Location only

> **Giá chạm POC5**

→ chưa vào.

### Location + reaction

> **POC5 bị reject**

→ bắt đầu chú ý.

### Location + reaction + flow

> **POC5 bị reject + CVD suy yếu + OI chuyển BeI + Auction yếu + RSI mất 50**

→ **bearish setup**.

### Location + reaction + flow + retest

> **POC5 bị reject → bearish flow → retest POC5 → reject lần nữa**

→ **A+ Short candidate**.

---

# Core Rule

> ## **POC5 bị reject + flow chuyển bearish.**

Nhưng phiên bản đầy đủ cho AI Trader là:

> ## **POC5 cho LOCATION → Rejection cho SIGNAL CONTEXT → Bearish Flow cho CONFIRMATION → Retest cho ENTRY.**