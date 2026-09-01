# ATS — Trading Domain & AI Trader

## 0. Luật gốc — Flow Type của OI

- **BuI = Bull In** → Long/Bullish positioning đang vào
- **BuO = Bull Out** → Long/Bullish positioning đang ra
- **BeI = Bear In** → Short/Bearish positioning đang vào
- **BeO = Bear Out** → Short/Bearish positioning đang ra

**Không tự đổi nghĩa:** BuO không mặc định là short covering; BeO không mặc định là long closing. Các kết luận như fresh long, fresh short, short covering, long liquidation... phải được suy luận từ sự kết hợp nhiều dữ liệu.

---

# 1. Positioning Domain
## OI + Flow Type

### OI
- **OI tăng** → tổng vị thế đang được mở/thêm.
- **OI giảm** → tổng vị thế đang được đóng/bớt.

### Flow Type

| Flow Type | Ý nghĩa ATS |
|---|---|
| **BuI** | Bullish/Long positioning vào |
| **BuO** | Bullish/Long positioning ra |
| **BeI** | Bearish/Short positioning vào |
| **BeO** | Bearish/Short positioning ra |

### Đọc cấp 1
- **OI ↑ + BuI** → bullish positioning được build.
- **OI ↓ + BuO** → bullish positioning được unwind.
- **OI ↑ + BeI** → bearish positioning được build.
- **OI ↓ + BeO** → bearish positioning được unwind.

Positioning nói về **vị thế**, không trực tiếp mô tả aggressive market buying/selling.

---

# 2. Order Flow Domain
## CVD + Agg Liq

### CVD
Đọc aggressive execution / delta pressure.

- **CVD tăng** → aggressive buying chiếm ưu thế.
- **CVD giảm** → aggressive selling chiếm ưu thế.
- **CVD phẳng/gần 0** → aggressive flow tương đối cân bằng.

Quan trọng là **hướng và diễn biến**, không chỉ một snapshot.

### Agg Liq
- **L liquidation lớn** → long positions bị forced close/liquidate.
- **S liquidation lớn** → short positions bị forced close/liquidate.

### Kết hợp
- **Giá ↑ + CVD ↑ + S liq lớn** → bullish move có thể được hỗ trợ bởi short squeeze.
- **Giá ↓ + CVD ↓ + L liq lớn** → bearish move có thể được khuếch đại bởi long liquidation.

Liquidation là **fuel/forced flow**, không tự động xác nhận xu hướng mới.

---

# 3. Auction Domain
## Auction Line + EMA20 + Triangles

### Auction Line (AL)

**Dấu +/− của AL** cho biết trạng thái tuyệt đối:
- **AL > 0** → auction pressure positive.
- **AL < 0** → auction pressure negative.

Nhưng dấu +/− không nên được dùng một mình.

### AL so với EMA20

Đây là quan hệ rất quan trọng:

- **AL > EMA20** → auction hiện tại mạnh hơn baseline gần đây.
- **AL < EMA20** → auction hiện tại yếu hơn baseline gần đây.

Ví dụ:
- AL **+2k**, EMA20 **+1k** → positive và strengthening.
- AL **+500**, EMA20 **+1k** → vẫn positive nhưng cooling/weakening.
- AL **-3k**, EMA20 **-5k** → vẫn negative nhưng improving relative to baseline.
- AL **-6k**, EMA20 **-4k** → negative và deteriorating.

> **AL +/− = trạng thái tuyệt đối; AL vs EMA20 = trạng thái tương đối / momentum của auction.**

### Triangles
Các tam giác là event/confirmation markers. Không nên đọc một tam giác đơn lẻ như tín hiệu trade độc lập; cần đối chiếu AL, EMA20, price action, CVD/OI và Volume Profile.

---

# 4. Context Domain
## VPIN + RSI + Funding + L/S + F&G + Volume Profile

Context trả lời: **môi trường hiện tại thế nào và giá đang đứng ở đâu?**

### VPIN
- **Thấp** → flow tương đối bình thường/cân bằng hơn.
- **Cao** → imbalance/toxicity cao, biến động có thể nhanh.

VPIN cao không tự động bearish; VPIN thấp không tự động bullish.

### RSI
Đọc momentum/độ nóng:
- RSI thấp → momentum yếu / oversold tendency.
- RSI cao → momentum mạnh / overbought tendency.
- RSI trung tính → momentum cân bằng hơn.

Dùng thêm để tìm divergence, không dùng một mình để bắt đỉnh/đáy.

### Funding
- **Funding dương** → longs trả shorts.
- **Funding âm** → shorts trả longs.

Funding hữu ích để đánh giá crowding, không phải hướng giá tuyệt đối.

### Long/Short Ratio
Phân biệt:
- Global
- Top Accounts
- Top Positions

Chênh lệch giữa các nhóm có thể cho thấy positioning asymmetry; không mặc định nhóm nào chắc chắn đúng.

### Fear & Greed
- Fear → risk appetite thấp.
- Greed → risk appetite cao.

Đây là background regime, không phải trigger entry.

### Volume Profile
- **POC** → vùng value concentration nổi bật.
- **VAH** → upper value boundary.
- **VAL** → lower value boundary.
- **Profile High/Low** → biên của profile.

### Reclaim
Một râu xuyên POC chưa nên coi là reclaim hoàn chỉnh. Reclaim chất lượng cao hơn khi:
1. Giá đóng nến trên/dưới level.
2. Các nến sau giữ được level.
3. Retest thành công.
4. Các domain khác bắt đầu đồng thuận.

---

# 5. Khi kết hợp 4 Domain

## Bullish alignment

**Positioning:** OI ↑ + BuI

**Order Flow:** CVD ↑; S liquidation có thể hỗ trợ squeeze.

**Auction:** AL ↑ và > EMA20; bullish markers được xác nhận.

**Context:** Giá reclaim/hold POC; RSI không quá cực đoan; VPIN không cho thấy panic bearish flow; funding/L-S chưa quá crowded long.

→ **Nhiều domain đồng thuận = xác suất continuation cao hơn.**

## Bearish alignment

**Positioning:** OI ↑ + BeI

**Order Flow:** CVD ↓; L liquidation có thể khuếch đại downside.

**Auction:** AL ↓ và < EMA20; bearish markers được xác nhận.

**Context:** Giá mất POC/support; RSI yếu; VPIN cao nếu có toxic sell imbalance; positioning có thể crowded long.

→ **Nhiều domain đồng thuận = bearish continuation đáng tin hơn.**

---

# 6. Divergence — nơi AI Trader cần chú ý

### Giá ↑ nhưng CVD ↓
Có thể là absorption, passive bid, short squeeze hoặc rally thiếu aggressive demand.

→ Không FOMO chỉ vì giá tăng.

### Giá ↓ nhưng CVD ↑
Có thể là selling exhaustion hoặc absorption.

→ Cần xác nhận thêm từ OI + AL + VP.

### Giá ↑ + OI ↓
Positioning đang giảm trong lúc giá tăng.

→ Không tự kết luận bullish fresh positioning; xem Flow Type, CVD và liquidation.

### AL dương nhưng dưới EMA20
> **AL > 0 nhưng AL < EMA20**

Auction vẫn positive tuyệt đối nhưng yếu hơn baseline → cooling.

### AL âm nhưng trên EMA20
> **AL < 0 nhưng AL > EMA20**

Auction vẫn negative tuyệt đối nhưng đang cải thiện → bearish pressure giảm.

---

# 7. AI Trader — workflow đề xuất

### Step 1 — Market Structure
Xác định giá so với POC/VAH/VAL/VP1/POC5 và level vừa test/reclaim/fail.

### Step 2 — Positioning
OI tăng/giảm + Flow Type.

### Step 3 — Order Flow
CVD direction + liquidation imbalance + squeeze/forced unwind.

### Step 4 — Auction
AL direction + AL +/- + AL vs EMA20 + triangles.

### Step 5 — Context
VPIN + RSI + Funding + L/S + F&G + Volume Profile.

### Step 6 — Alignment
Phân loại:
- Strong Bullish
- Bullish
- Neutral / Rotation
- Bearish
- Strong Bearish

### Step 7 — Trigger / Invalidation
Không trade chỉ vì bias. Xác định:
- **Trigger:** level + domain confirmation.
- **Invalidation:** level bị mất/reclaim thất bại.
- **Next target:** POC/VAH/VAL/liquidity/structure kế tiếp.

---

# 8. State ≠ Trigger

Một chỉ báo có thể mô tả **state**, nhưng chưa chắc là entry trigger.

- RSI 37 ≠ Long ngay.
- VPIN 0.9 ≠ Short ngay.
- CVD -1k ≠ Short ngay.
- BuI ≠ Long ngay.
- AL > EMA20 ≠ Long ngay.

Một setup tốt thường cần:

**Location + Trigger + Confirmation + Invalidation**

---

# 9. Mental Model

| Domain | Câu hỏi |
|---|---|
| **Positioning** | Ai đang vào/ra vị thế? |
| **Order Flow** | Ai đang thực sự đẩy lệnh/aggress? |
| **Auction** | Auction đang mạnh lên hay yếu đi? |
| **Context** | Chuyện đó xảy ra ở đâu và trong môi trường nào? |

**Positioning = Intent / Inventory**

**Order Flow = Execution**

**Auction = Acceptance / Rejection**

**Context = Environment / Location**

→ **AI Trader = tổng hợp cả 4, tìm alignment và divergence.**

---

# 10. Checklist mỗi snapshot

- [ ] Price location
- [ ] Key POC / VAH / VAL / VP1 / POC5
- [ ] OI direction
- [ ] Flow Type
- [ ] CVD direction
- [ ] Liquidation imbalance
- [ ] AL absolute value (+/-)
- [ ] AL vs EMA20
- [ ] Triangles / auction events
- [ ] VPIN
- [ ] RSI
- [ ] Funding
- [ ] Global L/S
- [ ] Top Accounts L/S
- [ ] Top Positions L/S
- [ ] Fear & Greed
- [ ] Bull/Bear/Neutral alignment
- [ ] Divergence
- [ ] Trigger
- [ ] Invalidation
- [ ] Next target

---

## Ghi chú

Đây là **framework sơ bộ**, chưa phải hệ thống tín hiệu định lượng hoàn chỉnh. Có thể tiếp tục bổ sung scoring, hierarchy giữa các domain, reversal vs continuation, absorption/squeeze/liquidation và điều kiện xác nhận M5/M15/M30.