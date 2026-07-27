# 03 — Individual Reflection

> Phạm Nguyên Việt — 2A202601547 — Nhóm A4

---

## Tôi đã tham gia vào phần nào?

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| Scan cá nhân | Scan 8 problems từ trải nghiệm thực tập (6) và học tập (2). Tự scan 6 trước, dùng AI gợi ý thêm góc nhìn | Có danh sách đa dạng 4 lăng kính. Bỏ 2 ý AI gợi ý vì không phải pain thật |
| Pitch Problem Card | Pitch vấn đề CSKH (Card D — CS trả lời ticket chính sách lặp lại) cho nhóm 13 người. Trình bày actor (2 CS agents, Intercom), workflow 6 bước, bottleneck (tìm KB Notion + soạn reply), metric 7.5'/ticket × 20-25 ticket = 150-187'/ngày | Bài được đưa vào 1 trong 3 vấn đề thảo luận chính của nhóm. Nhóm phản biện sâu nhưng cuối cùng chọn Discord farm (Card H) làm candidate |
| Nhận challenge từ nhóm | Phạm Trung Kiên hỏi: "Nhân viên đang dùng hệ thống nào tra cứu, bottleneck thật ở bước nào?". Phan Hoàng Long hỏi: "Non-AI đã đủ chưa? Metric có log không?". Đỗ Nhật Minh hỏi: "Ticket thật hay rác? Cập nhật chính sách xử lý thế nào?". Nguyễn Huy Anh hỏi: "Điều khoản conflict thì sao?". Trương Minh Hoàng hỏi: "AI có dùng lịch sử hội thoại không?". Hà Tấn Phong hỏi: "Hệ thống duyệt bảo hành tự động hay cần người?" | Trả lời được các câu hỏi. Nhận ra cần thu hẹp scope: không phải chatbot chung chung mà là "tìm chính sách đúng + draft reply" |
| Challenge vấn đề QA vỏ xe (#1) | Tham gia thảo luận khi nhóm bàn về Computer Vision cho rà soát bề mặt vỏ xe. Nhận xét: AI xử lý phần dễ (lỗi rõ) nhưng bottleneck thật (lỗi nhỏ/góc khuất) AI chưa chắc detect được | Giúp nhóm thu hẹp hướng: AI hỗ trợ đánh dấu vùng nghi vấn, QA vẫn xác nhận cuối. Không nên Agent tự động |
| Challenge vấn đề Discord farm (#3) | Hỏi: "Thế nào là bài chất lượng? Proxy độ dài/có code/có link có đáng tin không? Bài dài vẫn có thể copy-paste" | Giúp nhóm phân biệt: bài toán lọc spam (dễ) khác bài toán đánh giá chất lượng thật (khó). Cần Rule hỗ trợ trước |
| Tham gia chọn candidate | Tham gia chấm điểm shortlist 3 bài: Discord farm (48/50), CSKH ticket (42/50), QA vỏ xe (39/50). Bài mình pitch (CSKH) xếp thứ 2 | Đồng ý chọn Discord farm vì: text-based → dữ liệu sẵn, so sánh R/W/A rõ, cả nhóm đều là học viên nên hiểu domain |
| Đóng góp vào group report | Tham gia viết phần Validation, Research (rule/workflow/agent cho vấn đề CSKH), và phản biện PS v0 → v1 của bài Discord farm | Group report có đóng góp từ cả 13 thành viên |

---

## Bảng dùng AI trong lab

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Sau khi tự scan 6 problems, hỏi AI gợi ý thêm theo role "intern tại startup EdTech" | Gợi ý thêm góc nhìn "notification fatigue" và "meeting quá nhiều" | 2 ý đó không phải pain thật của mình, AI đoán chung chung | Bỏ 2 ý AI. Giữ 2 ý tự scan thêm từ trải nghiệm ở trường (paper, báo cáo TT) |
| Problem Card | Dán Card D (CSKH ticket) cho AI phản biện theo prompt "skeptical PM" | AI chỉ ra: "metric CSAT chưa có baseline, bottleneck chưa nói rõ tại sao KB search chậm" | AI đề xuất luôn dùng Agent "để tự động hóa 100%" — nhảy sang solution quá nhanh | Thêm baseline CSAT 4.0/5, giải thích rõ Notion search chậm. Bỏ đề xuất Agent vì chưa đủ data |
| Workflow | Nhờ AI chuyển mô tả workflow thành ASCII art | Nhanh hơn tự format, giữ đúng cấu trúc | AI gộp bước "tìm KB" và "soạn reply" thành 1 bước | Tách lại vì bottleneck nằm ở cả 2 bước, gộp sẽ mất chi tiết |
| Research | Hỏi AI tìm tools giải bài tương tự (CS automation, AI support) | Gợi ý Zendesk AI, Intercom Fin, Freshdesk Freddy — đúng hướng cho bài CSKH | AI claim "Intercom Fin giảm 60% thời gian" nhưng không dẫn nguồn cụ thể | Chỉ giữ link chính thức. Không dùng số liệu AI đưa ra mà không verify được |
| Problem Statement | Nhờ AI phản biện PS v0 của nhóm (Discord farm): "field nào mơ hồ, metric đo được chưa, boundary rõ chưa" | Chỉ ra: cần phân biệt rõ "lọc spam" vs "đánh giá chất lượng", success metric cần baseline | AI viết lại PS thay nhóm, văn phong corporate, không giống ngôn ngữ nhóm | Không dùng bản AI viết. Nhóm tự sửa PS v0 → v1 theo gợi ý, giữ ngôn ngữ nhóm |
| Decision | Không dùng AI cho bước quyết định | — | — | Nhóm tự thảo luận và chốt Workflow + Go |

---

## Reflection câu hỏi mở

**Tôi học được gì khi nghe problems của các bạn khác?**

Nguyễn Huy Anh pitch "Rà soát bề mặt vỏ xe VinFast bằng CV" — bài toán industry thật, có impact lớn (takt-time cả dây chuyền). Nhưng khi Trần Đức Thiện hỏi "lỗi nhỏ phụ thuộc góc chụp/ánh sáng, AI 2D có detect được không?", Nguyễn Văn Đại hỏi "nếu 9/10 lỗi con người xử lý nhanh, chỉ 1 lỗi AI không detect thì áp dụng để làm gì?" — nhóm nhận ra AI chưa chắc giải bottleneck khó nhất. Bài học: AI hay giải phần dễ, phần khó vẫn cần người.

Lục Minh Đức đưa ra problem Discord farm — ban đầu tôi nghĩ "đây chỉ là vấn đề policy, đổi rubric chấm điểm là xong". Nhưng khi Trần Đức Thiện phản biện: "proxy như độ dài/có code/có nguồn vẫn có thể là copy-paste", tôi hiểu rõ hơn rằng bài toán không chỉ là lọc spam mà là đánh giá chất lượng — phức tạp hơn Rule đơn giản.

**Nhóm có lúc nào bị solution-first không?**

Có. Khi thảo luận vấn đề QA vỏ xe, một số thành viên muốn nhảy vào "dùng Image Segmentation + overlay đánh dấu" ngay. Nhóm phải dừng lại, hỏi: "workflow hiện tại của nhân viên QA là gì? Bottleneck nằm ở bước nào?" Khi vẽ xong workflow mới thấy bottleneck ở lỗi nhỏ/góc khuất — AI 2D một góc có thể không detect được.

Tương tự, khi thảo luận Discord farm, cũng có ý kiến "xây Discord Bot auto-filter". Trương Minh Hoàng hỏi đúng: "Bước nào tốn thời gian nhất? Đọc bài, kiểm tra nguồn, hay nhập điểm?" — giúp nhóm focus vào bottleneck thật (đọc & đánh giá từng bài) thay vì giải bài toán sai.

**Tôi có thay đổi ý kiến sau khi bị challenge không?**

Có. Khi pitch CSKH, Phan Hoàng Long challenge: "Non-AI như Notion/highlight nhiều người đang làm rồi, AI tốt hơn bao nhiêu? Metric có log không?" — tôi nhận ra mình cần evidence thật, không chỉ ước lượng. Phạm Trung Kiên hỏi thêm: "Bottleneck thật ở bước nào: tìm nguồn, đọc chính sách, xác nhận hiệu lực hay soạn câu trả lời?" — giúp tôi thu hẹp problem từ "trả lời mọi ticket" thành "tìm đúng chính sách + draft reply".

Cuối cùng bài CSKH của mình xếp thứ 2 (42/50) sau Discord farm (48/50). Tôi đồng ý chọn Discord farm vì: dữ liệu text sẵn có (Discord message history), cả nhóm đều là học viên nên hiểu domain, và so sánh Rule/Workflow/Agent rõ ràng hơn.

**Tôi đóng góp gì thật sự vào artifact cuối?**

- Pitch vấn đề CSKH (#2) — không được chọn làm candidate cuối, nhưng phản biện giúp nhóm thấy pattern "tìm chính sách + draft reply" áp dụng được cho nhiều domain.
- Challenge cả 3 vấn đề thảo luận: QA vỏ xe (AI giải phần dễ, lỗi khó vẫn cần người), CSKH (tự pitch + nhận phản biện), Discord farm (proxy chất lượng có đáng tin?).
- Đóng góp vào nhận xét sau phản biện vấn đề #2 (CSKH): thu hẹp từ "chatbot chung chung" thành "Workflow/RAG có kiểm soát nguồn".
- Tham gia phản biện PS v0 → v1 của bài Discord farm: boundary "AI không tự chấm điểm cuối cùng".

**Điều khó nhất khi viết Problem Statement là gì?**

Viết success metric. Với bài Discord farm, nhóm ban đầu viết "giảm thời gian check Discord" — quá mơ hồ. Phải thêm: từ 30 phút → dưới 5 phút, Digest Recall ≥ 80%, Mentor time giảm ≥ 50%, False Negative < 5%. Mỗi metric cần baseline thật, không baseline thì metric vô nghĩa.

**Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?**

Tôi sẽ challenge nhiều hơn ở 2 chỗ:
1. "Thế nào là bài chất lượng?" — tiêu chí phân loại farm vs quality chưa rõ. Nhóm dùng proxy (độ dài, có code, có link) nhưng bài dài copy-paste vẫn pass → cần define rõ hơn trước khi build AI.
2. Bài mình pitch (CSKH) thua Discord farm một phần vì "nhóm chưa ai làm CSKH" — nếu mình chuẩn bị evidence thật (log Intercom, interview CS) trước khi pitch thì có thể thuyết phục hơn.

---

## Reflection tổng

```text
Bài lab này dạy tôi 4 bài học chính:

1. Problem first, not AI first — không phải khẩu hiệu. Khi nhóm suýt nhảy vào 
"Image Segmentation cho QA xe" hay "Discord Bot auto-filter" mà chưa vẽ workflow, 
phải dừng lại hỏi: "Bước nào tốn thời gian nhất?" Bottleneck thật không phải lúc 
nào cũng ở chỗ mình nghĩ.

2. Bài mình pitch không phải lúc nào cũng được chọn. CSKH ticket (42/50) thua 
Discord farm (48/50) vì: Discord có data sẵn (text message), cả nhóm đều hiểu 
domain (học viên), so sánh R/W/A rõ hơn. Tôi học được: chọn problem dựa trên 
feasibility + domain knowledge của nhóm, không chỉ vì pain lớn.

3. Challenge giúp nhóm chọn đúng. Câu hỏi phản biện từ 6 thành viên cho vấn đề 
CSKH giúp tôi thu hẹp problem (từ chatbot → RAG kiểm soát nguồn). Ngược lại, 
tôi challenge vấn đề Discord farm (proxy có đáng tin?) giúp nhóm phân biệt 
"lọc spam" vs "đánh giá chất lượng".

4. Rule không kém Agent. Cả 3 vấn đề đều kết luận Workflow. QA vỏ xe: AI đánh dấu, 
người confirm. CSKH: AI draft, người review. Discord: AI digest, mentor chấm. 
Pattern chung là AI hỗ trợ, người quyết định cuối.

Nếu làm lại, tôi sẽ chuẩn bị evidence thật (log, interview) trước khi pitch 
để bài CSKH có thể cạnh tranh tốt hơn. Và challenge rõ hơn về tiêu chí 
"bài chất lượng" trước khi nhóm build AI phân loại Discord.
```

---

## Tự kiểm cuối bài

- [x] [12đ cá nhân] Cá nhân có 5+ problems (8 problems) và top 3 Problem Cards.
- [x] [12đ cá nhân] Pitch rõ Card D (CSKH ticket) cho nhóm 13 người. Nhận challenge từ 6 thành viên (Kiên, Long, Minh, Anh, Hoàng, Phong) và trả lời được. Challenge cả 3 vấn đề thảo luận chính.
- [x] Nhóm có nhật ký hội tụ từ 8 candidates (A-H) → shortlist 3 → score → chọn Discord farm (48/50).
- [x] [15đ nhóm] Nhóm có workflow trước/sau: HV (30'/sáng → <5') + Mentor (giảm ≥50%).
- [x] [20đ nhóm] Nhóm có PS v0/v1 với metric (HV: 30'→<5', Recall ≥80%, Mentor -50%, False Neg <5%) và boundary (AI không tự chấm điểm, không xóa bài, không reply tự động).
- [x] [15đ nhóm] Nhóm có so sánh Rule (đổi rubric/upvote) / Workflow (AI Digest + Pre-screen) / Agent (Discord Bot auto) với lý do từng mức.
- [x] [10đ nhóm] Nhóm có Go (Workflow) với lý do, pilot scope (5 HV + 2 mentor, 1 tuần), implementation plan 7 bước.
- [x] [10đ cá nhân] Reflection có vai trò (pitch CSKH, challenge 3 vấn đề, đóng góp PS v1), cách dùng AI (scan, phản biện, research), bài học (problem first, bài pitch có thể thua, challenge giúp chọn đúng, Rule không kém Agent), và nếu làm lại sẽ chuẩn bị evidence trước khi pitch.
- [x] [6đ cá nhân] Tự giải thích được: Discord farm → workflow HV 5 bước + Mentor 5 bước → bottleneck "đọc & đánh giá từng bài" → metric 30'→<5', Recall ≥80% → boundary AI không tự chấm điểm → Workflow phù hợp vì Rule chưa giảm workload mentor, Agent overkill → Go Workflow.

---

*Reflection cá nhân — Phạm Nguyên Việt — Day 02 Lab*
