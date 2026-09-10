# AI Trader — POC5 Acceptance & Fake Detection:

## 1. Nguyên tắc cốt lõi

> **POC5 gives location; Flow confirmation gives entry.**

POC5 là **vùng location/reference**, không phải nút BUY/SELL.

Giá đi xuyên qua POC5 **không tự động có nghĩa** là Reclaim, Acceptance, Breakout hay Reversal.

AI Trader phải phân biệt rõ:

- **POC5 Cross / Reclaim Event**
- **POC5 Acceptance**
- **POC5 Fake Reclaim / Fake Breakdown**
- **POC5 Rejection**

## 2. POC5 Là Một Vùng, Không Phải Một Đường Giá Tuyệt Đối

Giá có thể quét râu xuyên qua POC5, thậm chí đóng nến cao hơn/thấp hơn vài trăm giá rồi sau đó đảo chiều.

Vì vậy:

> **Không phân loại trạng thái POC5 chỉ từ một cây nến hoặc một mức giá đơn lẻ.**

Vùng quan sát POC5 thực tế có thể rộng vài trăm giá quanh reference, tùy volatility của BTC và điều kiện Auction hiện tại.

Khoảng tolerance nên được điều chỉnh theo bối cảnh thị trường, không nên coi là một con số cố định vĩnh viễn.

## 3. Reclaim ≠ Acceptance

### POC5 Reclaim

**Reclaim** chỉ là một Event:

> Giá di chuyển từ dưới POC5 lên trên POC5.

Điều đó **chưa phải Entry signal**.

Tương tự, giá đi từ trên POC5 xuống dưới POC5 chỉ là một **loss/breakdown event**, không tự động là SHORT signal.

### POC5 Acceptance"

Acceptance cần bằng chứng cho thấy thị trường thực sự đang thiết lập value ở phía mới của POC5.

Chuỗi xác nhận ưu tiên:

```text
Price crosses POC5
        ↓
Flow xác nhận
        ↓
OI participation đủ ý nghĩa
        ↓
CVD đi cùng hướng với Price
        ↓
Auction xác nhận
        ↓
Price giữ được phía mới
        ↓
POC5 retest
        ↓
POC5 giữ được
        ↓
Continuation
```

## 4. Bullish POC5 Acceptance

Một Bullish Acceptance chất lượng thường có:

1. Price crosses above POC5.
2. **OI ↑ + BuI** — Bull In / dòng Long-Bullish positioning đang vào.
3. **CVD ↑** — aggressive buying xác nhận.
4. **Auction Line > EMA20** — chất lượng Auction ủng hộ nhịp tăng.
5. Price giữ phía trên POC5 thay vì lập tức quay xuống.
6. Retest POC5 giữ được.
7. CVD tiếp tục cải thiện sau retest.

### Điều kiện LONG ưu tiên

```text
POC5 reclaim
+ meaningful BuI / OI ↑
+ CVD ↑ / positive
+ AL > EMA20
+ POC5 retest hold
→ LONG
```

Phiên bản mạnh nhất là:

```text
Reclaim → Hold → Retest → Flow continuation → LONG
```

## 5. Bearish POC5 Acceptance

Một Bearish Acceptance chất lượng thường có:

1. Price crosses below POC5.
2. **OI ↑ + BeI** — Bear In / dòng Short-Bearish positioning đang vào.
3. **CVD ↓** — aggressive selling xác nhận.
4. **Auction Line < EMA20** — chất lượng Auction ủng hộ nhịp giảm.
5. Price giữ phía dưới POC5.
6. Retest POC5 từ phía dưới bị reject.
7. CVD tiếp tục giảm.

### Điều kiện SHORT ưu tiên

```text
POC5 loss
+ meaningful BeI / OI ↑
+ CVD ↓ / negative
+ AL < EMA20
+ POC5 retest rejection
→ SHORT
```

Phiên bản mạnh nhất là:

```text
Breakdown → Hold → Retest → Flow continuation → SHORT
```

## 6. Fake Reclaim

**Fake Reclaim** xảy ra khi giá vượt POC5 nhưng không thiết lập được Bullish Acceptance.

Đặc điểm thường gặp:

- Price chỉ nằm trên POC5 trong thời gian ngắn.
- Wick quét lên trên vùng.
- Candle thậm chí có thể đóng trên POC5.
- OI rất nhỏ, flat hoặc thiếu nhất quán.
- Flow Type có thể là **BeO** hoặc **BuO**, thay vì BuI đủ mạnh.
- CVD không đi cùng Price.
- Auction Line không giữ được trên EMA20.
- Price quay trở lại dưới POC5.

### Điểm quan trọng

A move such as:

```text
Price ↑
OI +0.01 / +0.02
BuI
CVD flat
AL weak
```

không được tự động xem là Fresh Long.

The same applies if OI is declining:

```text
Price ↑ + OI ↓ + BeO
```

Điều này có thể là **short covering**, không phải fresh long participation.

## 7. Fake Breakdown

**Fake Breakdown** xảy ra khi giá xuyên xuống dưới POC5 nhưng không thiết lập được Bearish Acceptance.

- Price chỉ nằm dưới POC5 trong thời gian ngắn.
- Lower wick quét liquidity.
- Candle có thể đóng dưới POC5.
- OI rất nhỏ, flat hoặc thiếu nhất quán.
- Flow không cho thấy BeI đủ mạnh.
- CVD không tiếp tục giảm.
- Auction Line hồi lên trên EMA20.
- Price Reclaim POC5.

### Điểm quan trọng

Do not call a breakdown Fresh Short merely because:

```text
Price < POC5
```

Fresh Short cần participation:

```text
Price ↓ + OI ↑ + BeI + CVD ↓
```

with auction confirmation where possible.

## 8. Flow Type — Luật gốc

Các định nghĩa này là nền tảng và tuyệt đối không được nhầm lẫn:

- **BuI = Bull In → dòng Long/Bullish positioning đang vào**
- **BuO = Bull Out → dòng Long/Bullish positioning đang ra**
- **BeI = Bear In → dòng Short/Bearish positioning đang vào**
- **BeO = Bear Out → dòng Short/Bearish positioning đang ra**

Vì vậy:

→ Fresh Long / bullish participation.

→ Short Covering / bearish positioning exiting.

**Không tự động là Fresh Long.**

→ Fresh Short / bearish participation.

→ Long Unwind / Long Exit.

**Không tự động là Fresh Short.**

## 9. Low-OI POC5 Noise

Một hành vi thị trường thường gặp:

> Giá có thể dao động vài trăm giá quanh POC5 trong khi thay đổi positioning bên dưới vẫn rất yếu.

Ví dụ:

```text
Price crosses POC5
OI ≈ 0
CVD weak
AL weak
→ NO CONFIRMATION
```

hoặc:

```text
Price crosses POC5
OI slightly positive
Flow Type changes briefly
CVD does not follow
→ WAIT
```

Nên xem đây là **POC5 noise / unresolved auction**, không phải trade signal mang tính quyết định.

## 10. Không Overweight Candle Close

Một candle đóng trên POC5 là bằng chứng hữu ích, nhưng chưa đủ để kết luận Acceptance.

Thứ tự đánh giá:

```text
Location
   ↓
Price behavior
   ↓
Positioning / Flow Type
   ↓
CVD
   ↓
Auction confirmation
   ↓
Retest / Acceptance
   ↓
Entry
```

The exact sequence can vary, but **no single candle close should override contradictory flow evidence.**

## 11. POC5 Acceptance Test

Khi Price đi vào vùng POC5, AI Trader cần kiểm tra:

### A. Location

- Price đang dưới, trong hay trên POC5?
- Price đang tiếp cận POC5 từ trên hay từ dưới?
- Đây là lần test đầu tiên hay repeated test?

### B. Positioning

- OI có tăng đủ ý nghĩa không?
- Flow Type là BuI, BuO, BeI hay BeO?
- Positioning signal có đồng thuận với Price không?

### C. Aggressive Flow

- CVD đang tăng hay giảm?
- CVD có xác nhận hướng Price không?
- CVD đang tăng tốc hay suy yếu?

### D. Auction

- AL đang trên hay dưới EMA20?
- AL đang cải thiện hay suy yếu?
- Auction có xác nhận phía mới của POC5 không?

### E. Retest

- POC5 có giữ được sau lần Cross ban đầu không?
- Price có quay lại POC5 không?
- Flow có xác nhận Retest không?

### F. Decision

Chỉ khi các bằng chứng trên đồng thuận, Decision Engine mới xem xét:

- LONG
- SHORT

Nếu chưa đủ:

> **WAIT / HOLD**

## 12. Ví dụ: Bullish Fake Reclaim

```text
Price: 79,000
POC5: 78,775

Price moves:
78,700 → 79,100 → 79,300 → 78,700

At POC5 zone:
OI: +0.01
Flow: BuI
CVD: flat
AL: below EMA20
```

Diễn giải:

- Price crossed POC5.
- But participation is weak.
- CVD does not confirm.
- Auction does not confirm.
- Price returns below POC5.

State:

> **Fake Reclaim / Unresolved Auction**

Decision:

> **WAIT**

Không chase LONG.

## 13. Ví dụ: Bullish Acceptance

```text
Price crosses POC5
        ↓
OI ↑ + BuI
        ↓
CVD ↑
        ↓
AL > EMA20
        ↓
Price holds above POC5
        ↓
Retest POC5
        ↓
CVD ↑ again
        ↓
POC5 holds
        ↓
LONG
```

Đây là pattern chất lượng cao được ưu tiên.

## 14. Ví dụ: Bearish Fake Breakdown

```text
Price falls below POC5
        ↓
lower wick / liquidity sweep
        ↓
OI ≈ 0
        ↓
CVD stops falling
        ↓
AL recovers above EMA20
        ↓
Price reclaims POC5
```

State:

> **Fake Breakdown**

Decision:

> **WAIT**

If the reclaim then develops into:

```text
OI ↑ + BuI
CVD ↑
AL > EMA20
POC5 retest hold
```

→ LONG becomes eligible.

## 15. Ví dụ: Bearish Acceptance

```text
Price loses POC5
        ↓
OI ↑ + BeI
        ↓
CVD ↓
        ↓
AL < EMA20
        ↓
Price remains below POC5
        ↓
Retest POC5 from below
        ↓
Rejection
        ↓
CVD ↓ again
        ↓
SHORT
```

## 16. Kết hợp với Volume Profile

POC5 nên luôn được đọc cùng các reference level lớn hơn khi có:

- VP1
- POC30
- VAH30
- VAL30
- Profile High
- Profile Low

Một POC5 Reclaim ngay bên dưới resistance lớn như POC30 hoặc VAH **không tự động có nghĩa** upside sẽ tiếp tục không giới hạn.

Tương tự, POC5 Breakdown ngay phía trên VAL30 **không tự động có nghĩa** downside sẽ tiếp tục không giới hạn.

Use:

> **POC5 = local location**  
> **VP1 / POC30 / VAH / VAL = bối cảnh Auction lớn hơn**  
> **Flow = participation**  
> **CVD = aggressive confirmation**  
> **Auction Line vs EMA20 = chất lượng Auction**

## 17. Kết hợp với VPIN

VPIN là thước đo stress/toxicity, không phải directional signal.

### High VPIN

Means:

- execution quality có thể kém hơn,
- liquidity có thể chịu stress,
- sweep và displacement có thể mạnh hơn,
- chase trở nên kém hấp dẫn hơn.

Nó **không có nghĩa**:

> High VPIN = SHORT

hoặc:

> High VPIN = LONG

Vì vậy:

```text
High VPIN + POC5 cross
→ require stronger confirmation
```

## 18. Kết hợp với RSI

RSI là context, không phải trigger chính của POC5.

RSI >70 không tự động có nghĩa SHORT.\nRSI <30 không tự động có nghĩa LONG.

Khi RSI extreme và VPIN cao:

> Prefer retest/acceptance rather than chasing displacement.

## 19. AI Trader — Decision Rules

### LONG

```text
IF
Price crosses above POC5
AND meaningful OI participation
AND Flow Type = BuI
AND CVD confirms ↑
AND AL > EMA20
AND POC5 holds/retest succeeds
THEN
LONG
```

### SHORT

```text
IF
Price crosses below POC5
AND meaningful OI participation
AND Flow Type = BeI
AND CVD confirms ↓
AND AL < EMA20
AND POC5 retest fails
THEN
SHORT
```

### WAIT

```text
IF
Price crosses POC5
BUT
OI is weak/flat
OR Flow Type is ambiguous
OR CVD does not confirm
OR AL does not confirm
OR price immediately returns through POC5
THEN
WAIT
```

### NO CHASE

```text
IF
Price đã displacement xa khỏi POC5
AND RSI/VPIN/liquidation conditions are stressed
THEN
DO NOT CHASE
WAIT FOR RETEST
```

## 20. Key Rule cho Trading Domain

> **POC5 gives location; Flow confirmation gives entry.**

Cụ thể hơn:

> **Crossing POC5 là một Event. Giữ được POC5 cùng Flow/CVD/Auction đồng thuận mới là Acceptance. Acceptance cộng Retest là cấu trúc Entry được ưu tiên.**

Vì vậy:

**Một candle trên/dưới POC5 = chưa đủ.**

**Vài trăm giá quanh POC5 = có thể chỉ là Auction noise bình thường.**

**Low OI / Flow yếu quanh POC5 = unresolved.**

**OI + Flow Type + CVD + Auction + Retest đồng thuận = actionable.**

## 21. Operational Checklist

Before entering at POC5:

- [ ] Đã xác định POC5 location
- [ ] Đã xác định hướng tiếp cận
- [ ] OI participation đủ ý nghĩa
- [ ] Đã xác định đúng Flow Type
- [ ] CVD xác nhận
- [ ] AL vs EMA20 xác nhận
- [ ] Price giữ được phía mới
- [ ] Đã quan sát hành vi Retest
- [ ] Không có liquidation/chase risk rõ ràng
- [ ] Đã kiểm tra context Volume Profile lớn hơn
- [ ] Đã xác định Entry / SL / TP
- [ ] Đã xác định Invalidation
- [ ] Nếu confirmation chưa đầy đủ → **WAIT**

# Nguyên tắc cuối cùng

> **Không trade theo đường POC5. Hãy trade theo **behavior quanh POC5**.**

> **Location cho biết nơi cần chú ý. Flow cho biết ai đang tham gia. CVD cho biết bên nào đang aggressive. Auction cho biết move có đang được Acceptance hay không. Retest cho biết value mới có giữ được hay không.**

> **Chỉ khi đó AI Trader mới nên Entry.**