# ATS — Indicator Ranking & Relationships

## 1. Triết lý cốt lõi

> **Indicator → Relationship → Context → Flow → Event → State → Reference → Quality → Decision**

ATS không nên đọc từng indicator như một tín hiệu Buy/Sell độc lập. Giá trị thực sự nằm ở **mối quan hệ giữa các chỉ số**, bối cảnh thị trường và vị trí giá đang tương tác.

---

# 2. Ranking tổng thể

## 🥇 S-Tier — Core Market Reading

### 1. Price + Reference
**Vai trò:** Where / Structure

Price cho biết thị trường đang làm gì. Reference cho biết thị trường đang làm gì **ở đâu**.

Reference chính:
- POC5
- VP1
- POC30 / VAH30 / VAL30
- EMA610 M5
- EMA200 M15
- EMA89 M30
- EMA89 H1
- EMA34 H4 / D1
- Orderbook liquidity zones
- Liquidation zones

Multi-timeframe EMA confluence đặc biệt quan trọng. Ví dụ 63980 ≈ EMA200 M30 + EMA89 H1 + gần EMA34 H4/D1 → đây là **Reference Zone**, không chỉ là một mức giá.

**Importance: S**

### 2. CVD
**Vai trò:** Aggressive Flow

CVD trả lời:
> **Aggressive buyers/sellers đang thực sự làm gì?**

Các relationship quan trọng:
- Price ↑ + CVD ↑ → bullish aggression được xác nhận
- Price ↓ + CVD ↓ → bearish aggression được xác nhận
- Price ↓ + CVD ↑/giữ dương → flow conflict, cần điều tra
- Price ↑ + CVD ↓ → bullish price nhưng aggressive flow không xác nhận

CVD cực mạnh khi đọc cùng Price và Reference.

**Importance: S**

### 3. Auction Flow
**Vai trò:** Auction Condition

Auction Flow không phải “CVD thứ hai”. Nó giúp đánh giá điều kiện của auction qua:
- Auction Line
- EMA20 của Auction
- POC5
- VP1
- volume xanh/đỏ
- CVD divergence triangles

Nó hữu ích để nhận biết momentum của auction, acceptance/rejection và deterioration.

Ví dụ:
> Auction +700 → +300 → +43 → -11 → -53 → -112

→ deterioration rõ ràng.

**Importance: S / A+**

---

# 3. A-Tier — Positioning & Quality

## 4. OI — Open Interest
**Vai trò:** Positioning

OI trả lời:
> **Positioning đang được thêm vào hay rút ra?**

OI rất hữu ích nhưng dễ bị diễn giải quá mức.

- Price ↑ + OI BuI → hỗ trợ giả thuyết fresh long participation.
- Price ↑ + OI BuO → không được tự động gọi short covering.
- OI giảm → chỉ cho biết open interest đang giảm, không xác định bên nào đang đóng.

> **OI = Positioning evidence, không phải directional trigger.**

**Importance: A+**

## 5. VPIN
**Vai trò:** Flow Quality / Stress

VPIN không nói trực tiếp Bull/Bear. Nó trả lời:
> **Flow hiện tại có orderly hay stressed/toxic?**

Ví dụ 0.16 → 0.23 cho thấy flow khá orderly; 0.23 → 0.81 là regime change đáng chú ý.

VPIN nên dùng như **Quality Filter**.

**Importance: A**

## 6. Agg Liquidation
**Vai trò:** Forced Flow / Event Confirmation

Liquidation hữu ích khi có displacement, giúp phân biệt:
- forced flow
- voluntary positioning
- long/short squeeze
- liquidation-driven displacement

Không đọc độc lập.

**Importance: A**

## 7. Orderbook Heatmap
**Vai trò:** Liquidity Reference

Cho biết thanh khoản nằm ở đâu.

Buy Wall / Sell Wall có thể làm Reference cho support/resistance, nhưng:
> **Wall ≠ guaranteed support/resistance.**

Wall có thể bị hấp thụ, rút hoặc price chạy xuyên qua.

**Importance: A-**

---

# 4. B-Tier — Momentum & Context

## 8. RSI
**Vai trò:** Momentum / Regime Context

Hữu ích cho momentum acceleration/deceleration và reset.

> RSI 70 ≠ Short  
> RSI 30 ≠ Long

RSI không nên là driver của ATS.

**Importance: B**

## 9. Funding
**Vai trò:** Crowd / Leverage Context

Hữu ích khi cực đoan và kết hợp OI/positioning. Trong intraday flow, CVD + Auction + OI + Reference thường trực tiếp hơn.

**Importance: B- / C+**

## 10. Long/Short Ratio
**Vai trò:** Crowd Positioning Context

Global / Top Accounts / Top Positions giúp hiểu crowd positioning, nhất là khi cực đoan.

> **Crowd positioning ≠ market direction.**

**Importance: B-**

## 11. Fear & Greed
**Vai trò:** Broad Sentiment Context

Phù hợp cho sentiment tầng rộng, không nên làm trigger intraday.

**Importance: Context**

---

# 5. Core Stack đề xuất cho ATS

Nếu chỉ được giữ 5 thành phần:

> **Price + Reference + CVD + Auction + OI**

Sau đó:

> **VPIN + Agg Liquidation = Quality / Event Filter**

Sơ đồ:

```text
                    DECISION
                       │
                    STATE
                       │
              EVENT + FLOW
                       │
          ┌────────────┼────────────┐
          │            │            │
        CVD         Auction         OI
     Aggression     Condition    Positioning
          │            │            │
          └────────────┼────────────┘
                       │
                   REFERENCE
              POC / VP / EMA / OB
                       │
                 QUALITY FILTER
                 VPIN / Liq
                       │
                    CONTEXT
        Funding / L-S / RSI / F&G
```

---

# 6. Relationship Matrix

## Bullish Confirmation

> **Price ↑ + CVD ↑ + OI BuI + Auction ↑**

Price tăng, aggressive buying tăng, positioning bullish được thêm và auction cải thiện → **directional confirmation mạnh**.

## Bearish Confirmation

> **Price ↓ + CVD ↓ + OI BeI + Auction ↓**

Price giảm, aggressive selling tăng, bearish positioning được thêm và auction deteriorate → **bearish confirmation mạnh**.

## Price ↓ nhưng CVD ↑

> **Price ↓ + CVD ↑**

Đây là **Flow Conflict**, không tự động bullish/bearish.

Có thể liên quan đến absorption, lack of seller follow-through, positioning unwind hoặc forced activity. Cần OI + Auction + Reference + Liquidation.

## Price ↑ nhưng CVD ↓

> **Price ↑ + CVD ↓**

Price advance chưa được aggressive flow xác nhận. Có thể là weak continuation, short covering, passive absorption hoặc divergence.

## Price ↑ + OI ↓

Không được tự động gọi “Short covering”. OI giảm chỉ cho biết positioning đang rút ra.

## Price ↓ + OI ↓

Không được tự động gọi “Long liquidation”. Cần Agg Liquidation xác nhận nếu muốn dùng giả thuyết forced long unwind.

## Price gần như đứng yên + Flow tăng

> Price ≈ unchanged + OI ↑ + CVD ↑ + Auction ↑

Có thể là **flow build / absorption / positioning build**, đặc biệt đáng chú ý tại POC5, VP1 hoặc EMA confluence.

## Price giảm nhẹ nhưng CVD không giảm

> Price ↓ + CVD giữ dương/tăng + OI không tăng bearish + VPIN thấp

Có thể là **seller pressure không hiệu quả**. Chưa đủ gọi bullish reversal, nhưng đáng theo dõi.

---

# 7. Reference biến Flow thành Event

Một flow signal ở giữa range có thể ít ý nghĩa. Cùng signal đó tại Reference quan trọng có thể trở thành Event.

Ví dụ:

> CVD positive + Auction positive

ở giữa range → bullish flow.

Nhưng:

> CVD positive + Auction positive + Price reclaim VP1

→ **VP1 Acceptance Event**.

Hoặc:

> Price reject MTF EMA + Auction deteriorate + CVD weaken

→ **MTF EMA Rejection Event**.

> **Reference biến dữ liệu flow thành market event.**

---

# 8. Quality không phải Direction

Một tín hiệu có thể bullish nhưng Quality thấp.

Ví dụ:
> Price ↑ + CVD ↑ + OI BuI

nhưng VPIN cực cao, liquidation spike và giá đang đâm vào major resistance → Direction bullish nhưng Quality continuation thấp hơn.

Ngược lại:
> Price ↑ + CVD ↑ + Auction ↑ + OI BuI

tại Reference vừa reclaim, VPIN thấp → Direction bullish + Quality tốt hơn.

ATS cần đánh giá:
> **Direction + Quality**

---

# 9. State không được lấy từ một indicator

Không dùng:
- RSI 70 → bearish State
- CVD dương → bullish State
- OI BuI → bullish State
- Auction âm → bearish State

State phải là kết quả của nhiều Relationship.

Ví dụ:
> Price rejection tại MTF EMA + Auction deteriorate + CVD vẫn dương + OI giảm + VPIN cao + POC5 được test và tạo reaction

Không nên gọi ngay “Bearish Expansion”.

State phù hợp hơn:
> **Bearish Rejection → POC5 Test → Recovery Attempt / Flow Conflict**

---

# 10. Quy tắc diễn giải ATS

## Không được:
> Indicator → Decision

## Phải là:
> Indicator → Relationship → Context → Flow → Event → State → Reference → Quality → Decision

### Nguyên tắc

1. Không suy diễn nguyên nhân từ một indicator.
2. OI giảm không đồng nghĩa Long đóng.
3. CVD dương không đồng nghĩa bullish.
4. Auction âm không đồng nghĩa bearish reversal.
5. RSI extreme không phải entry signal.
6. Wall không phải support/resistance chắc chắn.
7. Liquidation cần Event/Context để giải thích.
8. Reference phải được đưa vào trước khi đánh giá Event.
9. Flow conflict là một trạng thái thông tin, không phải lỗi dữ liệu.
10. Khi bằng chứng không đồng thuận, Decision nên là **WAIT / MONITOR** thay vì ép Buy/Sell.

---

# 11. Insight cốt lõi

Các công cụ không có cùng chức năng:

- **Price** = What
- **Reference** = Where
- **CVD** = Aggressive Who
- **Auction** = Auction Condition
- **OI** = Positioning
- **VPIN** = Quality / Stress
- **Liquidation** = Forced Flow
- **Orderbook** = Liquidity Map
- **RSI** = Momentum Context
- **Funding** = Leverage/Crowd Context
- **L/S Ratio** = Crowd Positioning
- **Fear & Greed** = Broad Sentiment

Vì vậy câu hỏi tốt nhất không phải:
> “Indicator nào mạnh nhất?”

Mà là:
> **“Indicator nào đang trả lời câu hỏi nào, và các câu trả lời đó có đồng thuận hay mâu thuẫn?”**

---

# 12. Kết luận

Core Stack:

> **Price + Reference + CVD + Auction + OI**

Quality / Event Filter:

> **VPIN + Agg Liquidation**

Context:

> **RSI + Funding + L/S Ratio + Fear & Greed**

Mục tiêu không phải dự đoán từ một indicator.

Mục tiêu là xây dựng chuỗi bằng chứng:

> **Indicator → Relationship → Context → Flow → Event → State → Reference → Quality → Decision**

Khi nhiều tầng cùng xác nhận, Quality tăng.

Khi các tầng mâu thuẫn, ATS phải **giảm conviction và chờ Event tiếp theo**.

Đó là nền tảng để biến một hệ thống nhiều indicator thành một **market-reading engine có logic**, thay vì một “indicator soup”.