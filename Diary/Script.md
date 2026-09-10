# Hồ sơ cá nhân & Kịch bản mẫu huấn luyện AI

> File này gồm 2 phần: (1) bộ câu hỏi giúp AI hiểu rõ hơn về bạn, và (2) một kịch bản/khung mẫu để bạn tái sử dụng khi hướng dẫn AI trong các lĩnh vực khác nhau.
> Ở Phần 1, bạn có thể **bỏ qua hoặc xoá** bất kỳ câu hỏi nào bạn thấy nhạy cảm hoặc không cần thiết — không có câu nào bắt buộc.

---

## PHẦN 1 — HỒ SƠ NGƯỜI DÙNG

Điền trực tiếp câu trả lời ngay dưới mỗi câu hỏi. Bạn không cần trả lời hết trong một lần; có thể cập nhật dần theo thời gian.

### 1. Thông tin cơ bản
- Hãy gọi tôi là Sếp là được.
- Công việc chính hiện tại của tôi là làm thực tập thiết kế cho một công ty in ấn offset.
- Hiện tại công việc của tôi có thể xem là không có giai đoạn cụ thể vì làm thiết kế nên tôi sẽ làm theo từng đơn hàng một.

### 2. Mục tiêu
- Mục tiêu ngắn hạn (vài tuần–vài tháng tới) mà bạn muốn AI hỗ trợ là gì?
- Mục tiêu dài hạn (6 tháng–vài năm) liên quan đến công việc/dự án là gì?
- Bạn định dùng AI (Claude) chủ yếu cho việc gì? (viết lách, lập trình, phân tích dữ liệu, nghiên cứu, tư vấn chiến lược, học tập, khác...)
- Có KPI/thước đo thành công cụ thể nào bạn đang theo đuổi không?

### 3. Bối cảnh công việc / lĩnh vực
- Bạn đang làm việc trong lĩnh vực/ngành nào cụ thể? (VD: fintech, giáo dục, marketing, y tế...)
- Có thuật ngữ chuyên ngành, quy trình nội bộ, hoặc tiêu chuẩn nào AI cần biết để hỗ trợ đúng không?
- Đối tượng bạn phục vụ là ai? (khách hàng, sếp, đồng nghiệp, độc giả...)
- Bạn có đang làm việc trong một tổ chức/công ty có quy định riêng về cách trình bày, thương hiệu (tone, format) không?

### 4. Phong cách giao tiếp & làm việc ưa thích
- Bạn thích AI trả lời ngắn gọn, súc tích hay chi tiết, đầy đủ?
- Bạn thích văn phong trang trọng, chuyên nghiệp hay gần gũi, đời thường?
- Bạn có thích AI đặt câu hỏi làm rõ trước khi thực hiện, hay cứ chủ động đưa ra giả định hợp lý rồi làm luôn?
- Khi AI không chắc chắn về điều gì, bạn muốn AI nói rõ sự không chắc chắn đó, hay cứ đưa ra phương án tốt nhất có thể?
- Bạn có ngôn ngữ ưu tiên khi giao tiếp không? (tiếng Việt, tiếng Anh, hay pha trộn tuỳ ngữ cảnh)

### 5. Kiến thức nền & công cụ đang dùng
- Trình độ hiểu biết của bạn về lĩnh vực đang hỏi (mới bắt đầu / trung cấp / chuyên sâu)?
- Bạn đang dùng công cụ/phần mềm nào liên quan (Excel, Notion, Figma, ngôn ngữ lập trình, nền tảng cụ thể...)?
- Có tài liệu, dữ liệu, hoặc quy chuẩn nào bạn thường cần AI tham chiếu khi làm việc không?

### 6. Ràng buộc & sở thích cần lưu ý lâu dài
- Có điều gì bạn **không muốn** AI làm hoặc đề cập (chủ đề tránh, định dạng không thích...)?
- Có giới hạn về thời gian, ngân sách, hoặc nguồn lực bạn thường gặp phải không?
- Bạn có yêu cầu đặc biệt nào về bảo mật/quyền riêng tư dữ liệu khi làm việc với AI không?

### 7. Những chủ đề bạn muốn đánh dấu là nhạy cảm/không cần thiết
*(Bạn có thể liệt kê ở đây bất kỳ câu hỏi nào ở trên mà bạn muốn bỏ qua, hoặc thêm lý do nếu muốn.)*
-

---

## PHẦN 2 — KỊCH BẢN MẪU ĐỂ HUẤN LUYỆN/HƯỚNG DẪN AI

### Nguồn tham khảo đã kiểm chứng

Phần này được xây dựng dựa trên tài liệu chính thức, mới nhất của Anthropic (đơn vị tạo ra Claude), cập nhật gần đây nhất vào tháng 11/2025 – 2026:
- "Prompt engineering best practices for 2026" — claude.com/blog/best-practices-for-prompt-engineering
- "Effective context engineering for AI agents" — anthropic.com/engineering/effective-context-engineering-for-ai-agents
- Tài liệu chính thức: platform.claude.com/docs/en/build-with-claude/prompt-engineering

Đây là nguồn gốc (nhà phát triển Claude), nên độ tin cậy cao hơn các blog thứ ba. Một điểm quan trọng cần lưu ý: **tài liệu này đã cập nhật quan điểm** so với các hướng dẫn cũ hơn (2023–2024) mà nhiều nguồn khác trên mạng vẫn đang lặp lại — cụ thể:
- Việc dùng **thẻ XML** để cấu trúc prompt và **role-prompting nặng nề** ("Bạn là chuyên gia hàng đầu thế giới...") **không còn cần thiết nhiều** với các model hiện đại — chỉ nên dùng khi prompt rất phức tạp hoặc cần ranh giới nội dung rõ ràng tuyệt đối.
- Nguyên tắc cốt lõi hiện nay là: **rõ ràng, cụ thể, và không dài dòng hơn mức cần thiết** — không phải prompt càng dài/càng nhiều kỹ thuật thì càng tốt.

### Khung 8 thành phần của một kịch bản huấn luyện AI hiệu quả

Những gì bạn đã biết (bối cảnh, vai trò, phạm vi kiến thức, kỹ năng cụ thể) là đúng nhưng chưa đủ. Dưới đây là khung đầy đủ hơn, tổng hợp từ nguồn đã kiểm chứng ở trên:

1. **Vai trò & bối cảnh nhiệm vụ (Task context)** — AI đóng vai gì, nhiệm vụ tổng quát là gì. *Lưu ý: không cần mô tả vai trò quá cầu kỳ; một vai trò đơn giản, rõ ràng thường hiệu quả hơn vai trò quá đặc thù.*
2. **Lý do/động cơ (Context & motivation)** — Giải thích *tại sao* yêu cầu này quan trọng, output sẽ được dùng để làm gì, cho ai xem. Điều này giúp AI đưa ra quyết định tốt hơn trong các tình huống chưa được nói rõ.
3. **Yêu cầu cụ thể (Specificity)** — Ràng buộc rõ: độ dài, định dạng, đối tượng đọc, các yêu cầu/hạn chế bắt buộc.
4. **Ví dụ mẫu (Examples / few-shot)** — Khi định dạng hoặc phong cách khó mô tả bằng lời, hãy đưa 1 ví dụ mẫu trước (rồi thêm nếu cần). AI hiện đại bám sát ví dụ rất chặt, nên ví dụ phải phản ánh đúng điều bạn muốn.
5. **Cho phép thể hiện sự không chắc chắn** — Luôn thêm dòng dạng: "Nếu dữ liệu không đủ để kết luận, hãy nói rõ thay vì suy đoán." Đây là cách hiệu quả nhất để giảm hiện tượng AI "bịa" thông tin (hallucination).
6. **Định dạng đầu ra mong muốn** — Nói AI **nên** làm gì thay vì chỉ nói **không nên** làm gì (VD: thay vì "đừng dùng gạch đầu dòng", hãy nói "viết thành đoạn văn liền mạch").
7. **Bước suy luận (nếu nhiệm vụ phức tạp)** — Với các tác vụ cần phân tích nhiều bước, có thể yêu cầu AI "suy nghĩ từng bước trước khi trả lời" hoặc chia nhỏ thành nhiều bước xử lý riêng (prompt chaining) nếu một lần yêu cầu duy nhất cho kết quả không ổn định.
8. **Tiêu chí đánh giá kết quả** — Trước khi dùng kịch bản cho một lĩnh vực mới, hãy tự hỏi: kết quả "tốt" trông như thế nào? Có tiêu chí nào để kiểm tra không? Điều này giúp bạn tinh chỉnh kịch bản qua từng lần dùng.

### Kịch bản mẫu (điền vào chỗ trống)

```
VAI TRÒ & NHIỆM VỤ:
Bạn đang hỗ trợ tôi trong vai trò [vai trò cụ thể, VD: trợ lý phân tích dữ liệu marketing].
Nhiệm vụ chính: [mô tả ngắn gọn, rõ ràng việc cần làm].

BỐI CẢNH & LÝ DO:
Kết quả này sẽ được dùng để [mục đích sử dụng, VD: trình bày cho ban lãnh đạo / đăng lên website / dùng nội bộ].
Đối tượng nhận kết quả là [ai].
Lý do việc này quan trọng: [giải thích ngắn gọn].

PHẠM VI KIẾN THỨC / BỐI CẢNH NGÀNH:
Lĩnh vực: [ngành/lĩnh vực cụ thể].
Các thuật ngữ/quy trình/tiêu chuẩn cần biết: [liệt kê nếu có].
Dữ liệu/tài liệu đính kèm liên quan: [liệt kê nếu có].

YÊU CẦU CỤ THỂ:
- Độ dài: [VD: khoảng 300 từ / 1 trang A4]
- Định dạng: [VD: bảng, đoạn văn, danh sách, JSON...]
- Văn phong: [VD: trang trọng / gần gũi / kỹ thuật]
- Ràng buộc bắt buộc: [VD: không dùng thuật ngữ chuyên ngành, phải có ví dụ minh hoạ...]

VÍ DỤ MẪU (nếu có):
[Dán 1 ví dụ ngắn thể hiện đúng định dạng/phong cách mong muốn]

XỬ LÝ KHI KHÔNG CHẮC CHẮN:
Nếu thông tin không đủ để đưa ra kết luận chắc chắn, hãy nói rõ điều đó thay vì suy đoán hoặc bịa thông tin.

BƯỚC SUY LUẬN (nếu nhiệm vụ phức tạp):
Trước khi đưa ra câu trả lời cuối cùng, hãy suy nghĩ từng bước: [gợi ý các bước cụ thể nếu cần].

TIÊU CHÍ THÀNH CÔNG:
Kết quả được xem là đạt khi: [mô tả tiêu chí, VD: đúng số liệu, đúng tone, không thiếu ý chính...].
```

### Mẹo áp dụng khi chuyển sang lĩnh vực mới
- Không cần dùng hết mọi thành phần trong khung ở trên — chỉ chọn phần nào thật sự cần cho tác vụ đó.
- Bắt đầu đơn giản, chỉ thêm chi tiết/kỹ thuật khi thấy kết quả chưa đạt.
- Sau mỗi lần dùng, ghi chú lại: kết quả có đúng ý không, cần chỉnh gì ở kịch bản — để lần sau viết kịch bản tốt hơn (đây chính là quá trình lặp/iterate mà tài liệu gốc nhấn mạnh).

---

## Câu hỏi cần bạn làm rõ (từ phía AI)

*(Không nằm trong 2 phần trên — đây là các điểm mình chưa chắc chắn về nhu cầu thực tế của bạn, ghi ra để tránh đoán mò.)*

1. File này bạn định dùng cho **chính bạn tự điền và dùng lại**, hay dùng để **đưa cho AI khác đọc trực tiếp** (như một system prompt)? Nếu là mục đích thứ hai, Phần 1 nên được viết lại thành đoạn văn mô tả thay vì dạng câu hỏi.
2. "Huấn luyện AI ở các lĩnh vực khác nhau" — bạn đang nói đến việc **viết prompt/hướng dẫn** cho AI (điều mình đã làm ở Phần 2), hay bạn muốn nói đến việc **fine-tuning/training model** theo nghĩa kỹ thuật máy học? Hai việc này rất khác nhau — mình đã giả định là vế đầu.
3. Kịch bản ở Phần 2 nên tổng quát cho mọi loại tác vụ, hay bạn có 1–2 lĩnh vực cụ thể muốn mình ưu tiên tối ưu trước (VD: viết nội dung, lập trình, phân tích dữ liệu)?
