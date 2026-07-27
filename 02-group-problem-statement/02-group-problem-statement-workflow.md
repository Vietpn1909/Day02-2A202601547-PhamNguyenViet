# Workflow before/after

Nội dung workflow:

```text
CURRENT STATE — 7 bước, 90 phút

[1 Export Jira: 10']
→ [2 Lấy metrics từ Sheets: 10']
→ [3 Đọc Slack recap: 15']
→ [4 Tổng hợp vào Docs: 15']
→ [5 Viết narrative: 25']  <-- bottleneck
→ [6 Review + format: 10']
→ [7 Gửi email: 5']

FUTURE STATE — 5 bước, 21 phút

[1 Auto-pull Jira/Sheets: 2']  -- Rule/script
→ [2 AI cấu trúc input: 1']    -- Workflow step
→ [3 AI draft narrative: 1']   -- Workflow step
→ [4 PM review + edit: 15']    -- Human boundary
→ [5 PM gửi: 2']

Fallback:
AI draft sai hoặc nhạt → PM bỏ draft và tự viết lại.

Bottleneck mới:
PM review + edit. Đây là bottleneck chấp nhận được vì đó là điểm kiểm soát chất lượng.
```

Before/after impact:

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| Tổng thời gian | 90 phút | Dưới 30 phút | Target chính |
| Số bước | 7 | 5 | Không chỉ giảm bước, mà giảm effort ở bước viết |
| Bước thủ công | 7/7 | 2/5 | PM vẫn review và gửi |
| Bottleneck chính | Viết narrative | Review/edit | Human boundary |
| Risk mới | Không có AI hallucination | Có hallucination risk | Cần review trước khi gửi |
low không cần tự lập kế hoạch động.
