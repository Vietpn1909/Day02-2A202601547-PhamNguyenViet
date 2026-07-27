# 01 — Individual Problem Scan

> Phạm Nguyên Việt — 2A202601547 — Nhóm A4

## Bối cảnh

Sinh viên năm 3 ngành CNTT, đang thực tập tại một startup EdTech (~30 người). Vị trí: intern developer trong team Product. Công việc hàng ngày gồm fix bug, làm feature nhỏ, viết test, tham gia standup và sprint review. Ngoài ra vẫn đang học ở trường, có seminar và báo cáo thực tập hàng tuần.

---

## Phase 1 — Scan rộng (8 problems)

### Bảng scan

| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Mỗi sáng viết daily standup trên Slack: Yesterday / Today / Blockers. Phải mở Jira nhớ lại hôm qua, nghĩ plan hôm nay, viết thành đoạn text. | Developer, intern, cả team 6 người | 10-15 phút/ngày × 5 ngày = 50-75 phút/tuần. Ai cũng phải viết, format giống nhau. |
| 2 | Tốn thời gian | Khi nhận bug report từ CS, mô tả thường thiếu steps to reproduce, version, screenshot. Dev phải hỏi lại CS → CS hỏi lại user → chờ reply → mới reproduce được. | Developer nhận bug, CS agent | 3-5 bugs/tuần cần hỏi lại, mỗi round chờ 2-4 tiếng. Mỗi bug mất thêm 20-30 phút chỉ để hiểu vấn đề. |
| 3 | Lặp lại | Team CS (2 người) trả lời 30-40 tickets/ngày qua Intercom. 60-70% là câu hỏi lặp lại: reset password, cách export data, upgrade plan, cách dùng feature X. Mỗi ticket lặp vẫn phải tìm KB → soạn reply. | 2 CS agents, gián tiếp ảnh hưởng user chờ reply | ~20-25 ticket lặp/ngày × 7.5 phút/ticket = 150-187 phút/ngày. First response trung bình 15-20 phút, user mong đợi < 5 phút. |
| 4 | Tốn thời gian | Đọc paper/tài liệu kỹ thuật 15-25 trang trước buổi seminar ở trường. Mỗi lần mất 2-3 tiếng để đọc + ghi chú + chuẩn bị slide tóm tắt. | Sinh viên chuẩn bị seminar | 1-2 lần/tháng, mỗi lần 2-3 tiếng. Hay trì hoãn vì dài và khô. |
| 5 | AI có thể tốt hơn | Review PR/code: với PR lớn (200+ dòng, 5+ files), reviewer mất 30-45 phút đọc diff + hiểu context + viết inline comments. Dễ miss edge cases, null check, security issues. | Senior dev / tech lead làm reviewer, dev chờ review | 3-5 PR reviews/tuần, PR lớn mất 30-45 phút. Bugs miss ở review → phát hiện ở production cost cao hơn. |
| 6 | Pain từ người khác | Intern mới setup dev environment theo doc trên Notion nhưng doc bị outdated: sai version Node, thiếu env variables, link DB đổi. Mất 1-2 ngày setup thay vì 2-3 tiếng. Mentor phải ngồi debug cùng. | Intern mới + mentor | 2-3 intern/quý gặp lỗi setup. Mình lúc mới vào cũng mất 1.5 ngày. Doc sửa rồi nhưng vẫn thiếu. |
| 7 | Lặp lại | Viết báo cáo thực tập hàng tuần cho trường: tổng hợp công việc, learning, challenges. Phải gom từ Jira, Slack, notes cá nhân rồi viết lại theo format trường. | Sinh viên thực tập | 30-45 phút/tuần × 12 tuần = 6-9 tiếng tổng. Format giống nhau mỗi tuần. |
| 8 | Pain từ người khác | PM tạo Jira ticket nhưng description mơ hồ: thiếu acceptance criteria, không có edge cases, reference design link hỏng. Dev phải hỏi lại 2-3 lần mới hiểu rõ scope. | Developer + PM | 30-40% tickets cần clarify, mỗi lần chờ nửa ngày. Sprint velocity bị ảnh hưởng. |

### Ghi chú scan

- Tự scan trước 6 problems từ trải nghiệm thực tập (1, 2, 3, 5, 6, 8) và 2 problems từ trải nghiệm học tập (4, 7).
- Sau đó dùng AI gợi ý thêm góc nhìn: AI đề xuất "notification fatigue" và "meeting quá nhiều" nhưng không phải pain thật của mình nên bỏ.
- Problem 3 (CS ticket) ban đầu mình không nghĩ tới, nhưng ngồi cạnh bạn CS thấy bạn ấy hay than nên thêm vào.

---

## Phase 2 — Top 3 Problem Cards + Draft Workflow

### Chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | CS trả lời ticket hỗ trợ lặp lại (#3) | Workflow rõ nhất, metric thời gian rõ, impact lớn (150-187 phút/ngày), có thể so sánh Rule/Workflow/Agent | "Đủ tốt" đo thế nào? CSAT có thay đổi không? |
| 2 | Bug report thiếu context (#2) | Pain cá nhân thấy rõ, dev team ai cũng gặp | Giải pháp non-AI (template) có thể đã đủ? |
| 3 | Review PR/code (#5) | AI có thể giúp, reviewer đang quá tải | Quality metric khó đo, "miss bugs" khó đếm |

---

### Problem Card #1 — CS trả lời ticket hỗ trợ lặp lại

**Problem 1 câu:**
Team CS tại startup mất trung bình 150-187 phút/ngày soạn reply cho ticket hỗ trợ lặp lại, dù 60-70% câu hỏi đã có câu trả lời trong knowledge base.

**Actor:**
2 CS agents phụ trách trả lời ticket người dùng qua Intercom.

**Thời điểm / bối cảnh:**
Hàng ngày trong giờ làm việc. Cao điểm sau release tính năng mới hoặc đầu năm học (sản phẩm EdTech).

**Current workflow 3-7 bước:**
1. User gửi câu hỏi qua Intercom (chat hoặc email)
2. CS đọc và phân loại: how-to / bug / billing / feature request
3. CS mở Notion tìm bài KB phù hợp
4. CS soạn reply: lấy nội dung KB, customize cho context user cụ thể
5. CS gửi reply
6. Nếu user hỏi follow-up → quay lại bước 2

**Bottleneck:**
Bước 3-4: CS phải switch giữa Intercom và Notion, tìm đúng bài KB (Notion search chậm), rồi rewrite cho phù hợp context từng user. Mất 5-10 phút/ticket dù câu trả lời core giống nhau.

**Impact:**
2 CS × ~12-13 ticket lặp/người/ngày × 7.5 phút = 150-187 phút/ngày cho toàn team. First response time trung bình 15-20 phút, user kỳ vọng < 5 phút. Reply chậm → user churn, NPS giảm.

**Success metric:**
Giảm thời gian xử lý ticket lặp từ 7.5 phút xuống 2-3 phút. First response time từ 15 phút xuống < 5 phút. CSAT giữ nguyên hoặc tăng (hiện tại 4.0/5, target ≥ 4.2/5).

**Non-AI alternative:**
Canned responses (template reply có sẵn) + cải thiện FAQ page + auto-suggest KB article khi user gõ. Có thể giải 30-40% câu hỏi cơ bản, nhưng user thường hỏi cụ thể hơn template.

**AI hypothesis:**
AI đọc ticket + tìm KB → draft reply phù hợp context user → CS review + edit → gửi. AI chỉ hỗ trợ bước soạn reply, không tự gửi.

**Quick gut:**
[x] Workflow

#### Draft current workflow

```text
CURRENT STATE — 7.5 phút/ticket lặp

[1 User gửi ticket qua Intercom]
→ [2 CS đọc + phân loại: 1']
→ [3 CS tìm KB trên Notion: 2-3']     <-- tốn thời gian
→ [4 CS soạn reply customize: 3-4']   <-- bottleneck
→ [5 CS gửi reply: 0.5']
→ [6 Follow-up? → quay lại bước 2]
```

#### Draft future workflow

```text
FUTURE STATE — 2-3 phút/ticket lặp

[1 User gửi ticket qua Intercom]
→ [2 AI đọc ticket + phân loại + tìm KB: <1']   -- Workflow step
→ [3 AI draft reply customize: <1']               -- Workflow step
→ [4 CS review + edit draft: 1-2']                 -- Human boundary
→ [5 CS gửi: 0.5']

Fallback: AI draft sai hoặc không liên quan → CS bỏ draft, tự soạn reply từ đầu.
```

---

### Problem Card #2 — Bug report thiếu context

**Problem 1 câu:**
Developer mất thêm 20-30 phút/bug và delay 2-4 tiếng chỉ để hiểu bug vì report từ CS thiếu steps to reproduce, version, screenshot.

**Actor:**
Developer nhận bug từ CS team.

**Thời điểm / bối cảnh:**
Mỗi khi CS forward bug report, 3-5 bugs/tuần.

**Current workflow 3-7 bước:**
1. User báo lỗi cho CS qua Intercom
2. CS tạo Jira ticket (copy paste mô tả user, thường thiếu thông tin)
3. Dev đọc ticket, không đủ context
4. Dev hỏi lại CS trên Slack
5. CS hỏi lại user → chờ reply 2-4 tiếng
6. CS forward thêm thông tin
7. Dev reproduce → bắt đầu debug

**Bottleneck:**
Bước 3-6: vòng hỏi lại lặp 2-3 lần, mỗi round chờ 2-4 tiếng. Dev mất 20-30 phút đọc hiểu mô tả rời rạc.

**Impact:**
3-5 bugs/tuần × (20-30 phút hiểu + 4-8 tiếng delay) = delay đáng kể. Sprint velocity giảm, release bị trễ.

**Success metric:**
Giảm số vòng hỏi lại từ 2-3 xuống 0-1. Giảm thời gian hiểu bug từ 20-30 phút xuống 5-10 phút.

**Non-AI alternative:**
Bug report template bắt buộc (structured form: steps to reproduce, expected vs actual, version, screenshot, severity). Đây là cách đơn giản và có thể đủ.

**AI hypothesis:**
AI parse mô tả user → gợi ý structured fields → flag khi thiếu thông tin bắt buộc trước khi CS submit ticket.

**Quick gut:**
[x] Rule (template form có thể đủ)

#### Draft current workflow

```text
CURRENT — 20-30' hiểu + 2-4h delay/bug

[User báo lỗi]
→ [CS copy paste vào Jira: 2']
→ [Dev đọc, thiếu info: 5']
→ [Dev hỏi lại CS: chờ 1-2h]
→ [CS hỏi user: chờ 2-4h]
→ [Dev reproduce: 15-20']
→ [Debug]
```

#### Draft future workflow

```text
FUTURE — 5-10' hiểu, gần 0 delay

[User báo lỗi]
→ [CS dùng structured form: steps/version/screenshot/severity: 3-5']
→ [Form validate: flag nếu thiếu field bắt buộc: tự động]
→ [Dev đọc ticket đủ thông tin: 5-10']
→ [Reproduce → Debug]

Fallback: User không điền đủ form → CS manually fill, hỏi user qua chat trước khi tạo ticket.
```

---

### Problem Card #3 — Review PR/code

**Problem 1 câu:**
Code reviewer mất 30-45 phút review PR lớn (200+ dòng) và thường miss edge cases, null handling, security issues vì cognitive load cao.

**Actor:**
Senior developer / tech lead làm reviewer. Dev chờ review.

**Thời điểm / bối cảnh:**
Hàng ngày, 3-5 PR reviews/tuần. PR nhỏ (< 50 dòng) không đau, PR lớn rất tốn thời gian.

**Current workflow 3-7 bước:**
1. Dev tạo PR + viết description
2. Reviewer nhận notification trên GitHub
3. Reviewer đọc PR description
4. Reviewer đọc diff file by file
5. Reviewer viết inline comments cho từng issue
6. Reviewer approve hoặc request changes
7. Dev fix → re-request review

**Bottleneck:**
Bước 4-5: đọc diff + viết comment mất 30-45 phút cho PR lớn. Reviewer phải hiểu business context + code context, cognitive load cao → dễ bỏ sót.

**Impact:**
3-5 PR reviews/tuần × 30-45 phút/PR lớn = 1.5-3.75 tiếng/tuần cho reviewer. Bugs miss ở review → phát hiện production → cost gấp 5-10x sửa.

**Success metric:**
Giảm review time từ 30-45 phút xuống 15-20 phút cho PR lớn. Giảm bugs escaped review (khó đo chính xác).

**Non-AI alternative:**
PR template bắt buộc + review checklist + linting + automated tests + giới hạn PR size < 200 dòng. Đã có linting và tests nhưng chưa đủ cho logic review.

**AI hypothesis:**
AI pre-review: tóm tắt changes, highlight tiềm năng issues, suggest test cases → Reviewer đọc summary trước khi đọc diff, có focus hơn.

**Quick gut:**
[x] Workflow

#### Draft current workflow

```text
CURRENT — 30-45' cho PR lớn

[Dev tạo PR]
→ [Reviewer đọc description: 2-3']
→ [Đọc diff file by file: 15-25']    <-- bottleneck
→ [Viết inline comments: 10-15']
→ [Approve / request changes]
```

#### Draft future workflow

```text
FUTURE — 15-20' cho PR lớn

[Dev tạo PR]
→ [AI tóm tắt changes + flag potential issues: <1']   -- Workflow step
→ [Reviewer đọc AI summary: 3-5']
→ [Đọc diff có focus vào flagged areas: 8-12']         -- Human boundary
→ [Viết comments: 3-5']
→ [Approve / request changes]

Fallback: AI summary miss context quan trọng → Reviewer bỏ qua summary, review full diff như cũ.
```

---

### Card muốn pitch nhất

```text
Card #1 — CS trả lời ticket hỗ trợ lặp lại
```

Vì sao:

```text
- Workflow tuyến tính, rõ ràng nhất trong 3 cards.
- Có baseline metric cụ thể: 7.5 phút/ticket, 20-25 tickets/ngày.
- Impact đo được bằng thời gian (150-187 phút/ngày).
- Có thể so sánh Rule (canned response) / Workflow (AI draft + CS review) / Agent (auto-reply).
- Mình ngồi cạnh bạn CS nên hiểu pain thật, không phải đoán.
```

Câu hỏi tôi muốn nhóm challenge:

```text
- Canned responses (non-AI) có đủ không? Có cần AI không?
- Nếu AI draft sai thông tin và CS không catch → user bị mislead → rủi ro thế nào?
- Startup nhỏ 30 người, có đủ ticket volume để justify đầu tư Workflow/AI không?
```

---

## Tham gia pitch + challenge trong nhóm

### Tôi pitch thế nào

Pitch Card #1 (CS trả lời ticket lặp lại) cho nhóm trong 3 phút:

```text
"Ở chỗ mình thực tập có 2 bạn CS ngồi bàn cạnh. Mỗi ngày 2 bạn nhận khoảng 
30-40 ticket qua Intercom, mà 60-70% là câu hỏi lặp: reset password, cách export data, 
hỏi pricing. Câu trả lời đã có sẵn trên Notion KB nhưng mỗi lần vẫn phải mở Notion, 
search tìm đúng bài, rồi viết lại cho phù hợp context user. Mỗi ticket lặp mất 7-8 phút, 
nhân lên 20-25 ticket/ngày → team mất 150-187 phút/ngày chỉ cho câu hỏi lặp.

Bottleneck nằm ở bước 3-4: tìm KB trên Notion (search chậm) + soạn reply customize.
Template canned response chỉ cover 30-40% vì user hay hỏi kèm context riêng.

Quick gut: Workflow — AI draft reply dựa trên KB, CS review rồi gửi."
```

### Nhóm challenge tôi — tôi trả lời thế nào

| Người hỏi | Câu challenge | Tôi trả lời |
|---|---|---|
| Long | "7.5'/ticket là con số ước lượng hay đo thật? Có log không?" | "Ước lượng từ quan sát khi ngồi cạnh, chưa có log chính xác. Cần validate bằng cách hỏi trực tiếp 2 bạn CS." → Nhóm ghi nhận cần validate ở Phase 4. |
| Hải | "Startup 30 người, 2 CS, ticket volume có đủ để justify đầu tư AI không?" | "30-40 tickets/ngày với 2 người là áng chừng. Nếu chỉ cần integrate Intercom Fin (đã dùng Intercom) thì cost thấp, không cần build from scratch." |
| Phong | "Canned response đã có rồi, thêm AI có khác gì nhiều không?" | "Canned response chỉ cover 30-40% câu hỏi cơ bản. 60% còn lại user hỏi kèm context (gói nào, thanh toán gì, mua lúc nào) → AI customize reply, template tĩnh không làm được." |

### Tôi challenge bạn khác

| Tôi hỏi ai | Card bị challenge | Câu challenge | Kết quả |
|---|---|---|---|
| **Phong** | P1 — Đọc slide trước assignment | "Metric 'không bỏ sót nội dung quan trọng' — đo bằng cách nào? Ai kiểm tra AI tóm tắt đúng hay sai?" | Phong chưa trả lời được cách đo cụ thể. Nhóm nhận ra quality metric mơ hồ → P1 tụt điểm so với V1/L1. |
| **Phong** | P3 — Tìm deadline nhiều nền tảng | "20 phút/tuần — impact này có đáng deep dive không? Google Calendar + When2meet đã giải phần lớn rồi." | Phong đồng ý impact nhỏ, card này yếu nhất trong 3 cards của Phong. |
| **Hải** | H3 — Fix bug môi trường | "Bạn chọn Agent — Agent cần tự lập kế hoạch, quyết định bước tiếp theo. Fix bug thường chỉ cần 1 bước tra cứu, Workflow có đủ không?" | Hải nghĩ lại và đồng ý Workflow hợp lý hơn Agent. Agent hơi quá cho bài toán này. |
| **Hải** | H2 — Báo cáo sprint | "Bài này giống Weekly Report trong deliverable example quá. Giảng viên có thể nghĩ nhóm copy pattern?" | Hải nhận ra rủi ro. Nhóm đồng ý loại H2 khỏi shortlist. |
| **Long** | L2 — Báo cáo cuối ngày | "Bạn tự nói Rule (template/form) đã đủ. Nếu Rule đủ thì deep dive sẽ kết luận 'không cần AI' ngay — có gì để so sánh R/W/A?" | Long đồng ý. L2 tốt để minh họa "Rule đủ" nhưng không phù hợp deep dive. |

### Kết quả pitch + challenge

```text
- Card tôi pitch (V1) vào shortlist và cuối cùng được nhóm chọn (gộp với L1 của Long).
- Challenge giúp loại bỏ: P3 (impact nhỏ), H2 (giống example), L2 (Rule đủ, không cần AI).
- Challenge giúp sửa: H3 từ Agent → Workflow, P1 nhận ra metric quality mơ hồ.
- Bản thân nhận challenge từ Long: cần validate số liệu 7.5'/ticket → ghi vào action item Phase 4.
```
