# 03 — Individual Reflection

> Phạm Nguyên Việt — 2A202601547 — Nhóm A4

---

## Tôi đã tham gia vào phần nào?

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| Scan cá nhân | Scan 8 problems từ trải nghiệm thực tập (6) và học tập (2). Tự scan 6 trước, dùng AI gợi ý thêm góc nhìn | Có danh sách đa dạng 4 lăng kính. Bỏ 2 ý AI gợi ý vì không phải pain thật |
| Pitch Problem Card | Pitch Card V1 (CS ticket lặp lại) cho nhóm 3 phút: trình bày actor (2 CS agents, Intercom), workflow 6 bước, bottleneck (tìm KB Notion + soạn reply), metric 7.5'/ticket × 20-25 ticket = 150-187'/ngày | Bài được vào shortlist, cuối cùng gộp với L1 (Long) thành candidate chính. 4/4 đồng thuận chọn |
| Nhận challenge | Long hỏi: "7.5'/ticket ước lượng hay đo thật?". Hải hỏi: "Volume đủ justify AI không?". Phong hỏi: "Canned response khác gì AI?" | Trả lời được cả 3: cần validate (→ action item), Intercom Fin cost thấp, AI customize reply mà template không làm được |
| Challenge Phong | Hỏi Phong: "Metric 'không bỏ sót nội dung' đo thế nào?" và "20'/tuần impact có đáng deep dive?" | Phong chưa trả lời được cách đo quality → P1 tụt điểm. Phong đồng ý P3 impact nhỏ |
| Challenge Hải | Hỏi Hải: "Non-AI template AC có đủ chưa?" và "Bài H2 giống deliverable example, rủi ro bị trừ" | Hải nhận domain BA/PM niche, nhóm chưa đủ sâu. H2 bị loại khỏi shortlist |
| Challenge Long | Hỏi Long: "L2 bạn tự nói Rule đủ, deep dive sẽ kết luận 'không cần AI' ngay?" | Long đồng ý L2 không phù hợp deep dive. Nhưng L1 rất mạnh → gộp với V1 |
| Nhận ra convergence | Phát hiện card mình (V1) và Long (L1) cùng pattern → đề xuất gộp 2 góc nhìn | Convergence signal mạnh: 2 người độc lập nhìn ra cùng problem |
| Gom trùng / cluster | Đề xuất gom 12 cards thành 5 cluster: ticket lặp, report, debug, đọc tài liệu, phân loại/routing | Nhóm dùng 5 cluster này để đánh giá. Cluster A (ticket lặp) nổi bật nhất |
| Chọn candidate | Chấm điểm 3 shortlist. V1+L1: 34/35, H1: 27/35, P1: 26/35 | 4/4 đồng thuận chọn V1+L1 |
| Validation / research | Hỏi trực tiếp 2 bạn CS tại công ty thực tập (Hà và Trang). Research 3 tools: Zendesk AI, Intercom Fin, Freshdesk Freddy | Validation xác nhận 60-65% ticket lặp. Research cho thấy pattern AI draft + human review phổ biến |
| Workflow nhóm | Vẽ current workflow (6 bước) và future workflow (5 bước), gộp góc nhìn của mình (Intercom/Notion) với Long (version chính sách) | Nhóm dùng làm workflow bản cuối |
| Problem Statement | Viết draft PS v0, nhờ AI phản biện → phát hiện metric CSAT chưa có baseline → thêm CSAT 4.0 hiện tại | PS v0 → v1 cải thiện rõ |
| Rule / Workflow / Agent | Lập luận chọn Workflow, giải thích vì sao Rule chưa đủ (30-40%) và Agent quá rủi ro | Nhóm thống nhất Workflow |
| Decision | Đề xuất pilot scope: top 20 câu hỏi phổ biến nhất, thử 2 tuần, đo 4 metrics | Nhóm đồng ý Go với scope pilot nhỏ |

---

## Bảng dùng AI trong lab

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Sau khi tự scan 6 problems, hỏi AI gợi ý thêm theo role "intern tại startup EdTech" | Gợi ý thêm góc nhìn "notification fatigue" và "meeting quá nhiều" | 2 ý đó không phải pain thật của mình, AI đoán chung chung | Bỏ 2 ý AI. Giữ 2 ý tự scan thêm từ trải nghiệm ở trường (paper, báo cáo TT) |
| Problem Card | Dán Card #1 (CS ticket) cho AI phản biện theo prompt "skeptical PM" | AI chỉ ra: "metric CSAT chưa có baseline, bottleneck chưa nói rõ tại sao KB search chậm" | AI đề xuất luôn dùng Agent "để tự động hóa 100%" — nhảy sang solution quá nhanh | Thêm baseline CSAT 4.0/5, giải thích rõ Notion search chậm. Bỏ đề xuất Agent vì chưa đủ data |
| Workflow | Nhờ AI chuyển mô tả workflow thành ASCII art | Nhanh hơn tự format, giữ đúng cấu trúc | AI gộp bước "tìm KB" và "soạn reply" thành 1 bước | Tách lại vì bottleneck nằm ở cả 2 bước, gộp sẽ mất chi tiết |
| Research | Hỏi AI tìm tools giải bài tương tự (CS automation, AI support) | Gợi ý Zendesk AI, Intercom Fin, Freshdesk Freddy — đúng hướng | AI claim "Intercom Fin giảm 60% thời gian" nhưng không dẫn nguồn cụ thể | Chỉ giữ link chính thức của từng tool. Không dùng số liệu AI đưa ra mà không verify được |
| Problem Statement | Nhờ AI phản biện PS v0: "field nào mơ hồ, metric đo được chưa, boundary rõ chưa" | Chỉ ra: success metric cần baseline, boundary cần nói rõ "không xử lý loại ticket nào" | AI viết lại PS thay mình, văn phong corporate, không giống ngôn ngữ nhóm | Không dùng bản AI viết. Tự sửa PS v0 → v1 theo gợi ý, giữ ngôn ngữ nhóm |
| Decision | Không dùng AI cho bước quyết định | — | — | Nhóm tự thảo luận và chốt Go/Not Yet/No-Go |

---

## Reflection câu hỏi mở

**Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Phong pitch "Đọc slide trước assignment" — lúc đầu tôi nghĩ bài này hay vì nhiều SV gặp. Nhưng khi tôi hỏi "metric 'không bỏ sót nội dung' đo thế nào?" thì Phong chưa trả lời được. Tôi học được rằng problem phải có metric đo được cụ thể, không phải cứ nhiều người gặp là problem tốt.

Long pitch bài giống mình (ticket chính sách CSKH lặp lại) — 2 người độc lập nhìn ra cùng pattern là tín hiệu convergence mạnh. Long thêm insight mà mình chưa nghĩ: vấn đề version chính sách (bản cũ lẫn bản mới), và Rule (FAQ tập trung) cần làm nền tảng trước khi Workflow.

Hải pitch "Requirement → Jira task" — bài thú vị nhưng khi Phong hỏi "nhóm mình có ai tự làm BA/PM chưa?", cả nhóm nhận ra domain niche quá. Deep dive cần chọn bài mà nhóm thật sự hiểu, không chỉ "thấy ở chỗ thực tập".

**Nhóm có lúc nào bị solution-first không?**

Có. Lúc đầu khi thảo luận CS ticket, Hải nói ngay "dùng ChatGPT API tích hợp vào Intercom". Nhóm phải dừng lại, quay về vẽ workflow hiện tại trước, rồi mới bàn solution. Khi vẽ xong workflow mới thấy bottleneck nằm ở bước tìm KB + soạn reply, không phải ở bước phân loại — nếu nhảy vào solution sớm có thể giải sai bước.

Hải cũng chọn Agent cho card "Fix bug môi trường" (H3). Khi tôi hỏi "Agent cần tự lập kế hoạch, fix bug chỉ cần 1 bước tra cứu — Workflow có đủ không?", Hải nghĩ lại và đồng ý Workflow hợp lý hơn. Đây là ví dụ điển hình của việc chọn mức AI cao hơn cần thiết.

**Tôi có thay đổi ý kiến sau khi bị challenge không?**

Có. Long challenge: "7.5 phút/ticket ước lượng hay đo thật? Nếu thật ra chỉ 3-4 phút thì impact giảm nhiều." Tôi nhận ra mình cần validate bằng data thật, không chỉ ước lượng từ quan sát. Nhưng tôi cũng phản biện lại: kể cả 3-4 phút × 20-25 ticket = 60-100 phút/ngày vẫn đáng kể. Long đồng ý.

Sau khi interview 2 bạn CS (Hà và Trang), cả 2 xác nhận canned response phải edit nhiều vì user hỏi contextual → Rule chỉ cover 30-40%. Điều này củng cố quyết định chọn Workflow.

**Tôi đóng góp gì thật sự vào artifact cuối?**

- Pitch Card V1 (CS ticket) — được chọn làm candidate chính (gộp với L1 của Long).
- Challenge 5 cards của bạn khác: P1, P3 (Phong), H2, H3 (Hải), L2 (Long) — giúp nhóm loại bỏ H2, P3, L2 và sửa H3 từ Agent → Workflow.
- Phát hiện V1 và L1 cùng pattern → đề xuất gộp 2 góc nhìn.
- Hỏi trực tiếp 2 CS agents (Hà, Trang) để validate — bằng chứng chính giúp nhóm confirm pain thật.
- Vẽ current/future workflow bản đầu tiên (gộp góc nhìn với Long).
- Draft PS v0 → sửa thành v1 sau khi nhờ AI phản biện.

**Điều khó nhất khi viết Problem Statement là gì?**

Viết success metric. Lúc đầu viết "giảm thời gian xử lý ticket" — quá mơ hồ. Phải thêm: từ bao nhiêu → xuống bao nhiêu, đo bằng gì, khi nào coi là thành công. Metric CSAT cũng khó vì phải có baseline (4.0) và target (≥ 4.2). Không có baseline thì metric vô nghĩa.

**Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?**

Tôi sẽ challenge nhiều hơn ở 2 chỗ:
1. Bước pilot: "20 câu hỏi phổ biến nhất" chọn bằng cách nào? Dựa vào frequency tag trên Intercom? Hay hỏi CS team? Nếu chọn sai 20 câu hỏi thì pilot không đo được đúng impact.
2. Data của Long (15-20 ticket/ngày) là từ bạn ở e-commerce, chưa phải data trực tiếp. Nên validate cả 2 nguồn (của mình và Long) trước khi gộp metric.

---

## Reflection tổng

```text
Bài lab này dạy tôi 4 bài học chính:

1. Problem first, not AI first — không phải khẩu hiệu. Khi Hải nói "dùng ChatGPT API" 
mà chưa vẽ workflow, nhóm dừng lại vẽ trước → thấy bottleneck ở bước tìm KB + soạn reply, 
không phải ở phân loại. Nếu nhảy vào solution sớm sẽ giải sai bước.

2. Convergence signal. Mình và Long độc lập nhìn ra cùng 1 pattern (ticket lặp) 
→ tín hiệu mạnh hơn 1 người nói. Khi gộp 2 góc nhìn (EdTech + e-commerce), 
problem statement chặt chẽ hơn.

3. Challenge giúp nhóm chọn đúng. Tôi challenge P1 (metric quality mơ hồ), 
H2 (giống example), L2 (Rule đủ) → giúp nhóm loại nhanh. Ngược lại, Long challenge 
metric 7.5'/ticket của tôi → tôi ghi nhận cần validate bằng data thật.

4. Rule không kém Agent. Rule (canned response) đã giải 30-40%. Long thêm: 
Rule (FAQ tập trung + version hóa) cần làm nền tảng trước. Workflow chỉ cần vì phần 
customize reply — và người thật vẫn review.

Nếu làm lại, tôi sẽ dành thêm thời gian cho validation: hỏi thêm user xem họ 
có thấy reply chậm là vấn đề không, xem log Intercom để lấy data thật, 
và validate cả data của Long (15-20 ticket từ bạn ở e-commerce) chứ không chỉ 
data ước lượng của mình.
```

---

## Tự kiểm cuối bài

- [x] [12đ cá nhân] Cá nhân có 5+ problems (8 problems) và top 3 Problem Cards.
- [x] [12đ cá nhân] Pitch rõ Card V1 (CS ticket, được chọn gộp với L1 Long). Challenge 5 cards: P1 (metric mơ hồ), P3 (impact nhỏ), H2 (giống example), H3 (Agent → Workflow), L2 (Rule đủ). Nhận challenge từ Long, Hải, Phong và trả lời được.
- [x] Nhóm có nhật ký hội tụ từ 12 candidates (V1-V3, P1-P3, L1-L3, H1-H3) → 5 clusters → 3 shortlist → score → chọn V1+L1.
- [x] [15đ nhóm] Nhóm có workflow trước/sau (current 6 bước 7.5'/ticket → future 5 bước 2-3'/ticket).
- [x] [20đ nhóm] Nhóm có Problem Statement v0/v1 với metric (7.5' → 2-3', CSAT 4.0 → ≥ 4.2) và boundary (chỉ ticket lặp, CS review, không tự gửi).
- [x] [15đ nhóm] Nhóm có so sánh No AI / Rule / Workflow / Agent với lý do từng mức.
- [x] [10đ nhóm] Nhóm có Go (pilot nhỏ) với lý do, pilot scope (top 20 câu hỏi, 2 tuần), exit criteria (>30% viết lại → rollback, CSAT <3.8 → tắt).
- [x] [10đ cá nhân] Reflection có vai trò (pitch V1, challenge 5 cards, validate 2 CS, gộp V1+L1, vẽ workflow, viết PS), cách dùng AI (scan, phản biện, research), bài học (problem first, convergence signal, challenge giúp chọn đúng, Rule làm nền tảng), và nếu làm lại sẽ validate thêm data cả 2 nguồn.
- [x] [6đ cá nhân] Tự giải thích được: CS ticket lặp (gộp V1+L1) → workflow 6 bước → bottleneck tìm KB + soạn reply → metric 7.5' → 2-3' → boundary chỉ ticket lặp, CS review → Workflow phù hợp vì Rule chưa đủ (30-40%), Agent quá rủi ro → Go pilot nhỏ.

---

*Reflection cá nhân — Phạm Nguyên Việt — Day 02 Lab*
