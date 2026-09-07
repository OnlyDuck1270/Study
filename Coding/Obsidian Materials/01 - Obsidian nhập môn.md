---
title: "Obsidian nhập môn"
aliases:
  - "Obsidian cơ bản"
tags:
  - learning/obsidian
  - guide/beginner
level: beginner
status: reference
created: 2026-08-19
updated: 2026-08-19
description: "Làm quen với vault, giao diện, Markdown, phím tắt và quy trình ghi chú đầu tiên."
---

# 01 — Obsidian nhập môn

> [!abstract] Mục tiêu
> Sau bài này, bạn có thể tạo và tìm note, trình bày nội dung bằng Markdown, dùng các phím tắt quan trọng và hiểu cách dữ liệu trong vault được lưu trữ.

> [!tip] Cách học hiệu quả
> Đừng chỉ đọc. Hãy mở song song một note mới và gõ lại từng ví dụ. Bạn có thể dùng `Ctrl+E` để chuyển giữa chế độ chỉnh sửa và chế độ đọc nếu phím này đang được gán trong **Settings → Hotkeys**.

## 1. Hiểu đúng về Obsidian

Obsidian không phải một cơ sở dữ liệu đóng. Một **vault** chỉ là một thư mục trên máy tính, còn mỗi note chủ yếu là một file văn bản có đuôi `.md` viết bằng Markdown.

Điều này đem lại ba lợi ích:

- Bạn sở hữu file và có thể mở chúng bằng nhiều trình soạn thảo khác.
- Thư mục có thể được sao lưu, đồng bộ và quản lý như dữ liệu thông thường.
- Liên kết giữa các note biến một tập file rời rạc thành mạng lưới kiến thức.

> [!warning] Đồng bộ không hoàn toàn giống sao lưu
> Đồng bộ có thể truyền cả thao tác xóa hoặc sửa nhầm sang thiết bị khác. Hãy duy trì thêm một bản sao định kỳ của toàn bộ vault. **File recovery** hữu ích khi gặp sự cố, nhưng không nên là bản sao lưu duy nhất.

## 2. Bản đồ giao diện

### Thanh bên trái

- **File explorer**: xem thư mục, tạo, đổi tên và di chuyển file.
- **Search**: tìm nội dung trong toàn bộ vault.
- **Bookmarks**: ghim note, tiêu đề hoặc truy vấn thường dùng.

### Khu vực giữa

Mỗi note mở trong một tab. Obsidian có ba cách hiển thị đáng biết:

- **Live Preview**: vừa viết vừa thấy phần lớn định dạng; phù hợp hằng ngày.
- **Reading view**: chỉ đọc kết quả đã render; phù hợp kiểm tra note hoàn chỉnh.
- **Source mode**: thấy toàn bộ cú pháp Markdown/YAML; hữu ích khi sửa template hoặc tìm lỗi định dạng.

### Thanh bên phải

Bạn có thể mở các bảng như:

- **Backlinks**: note nào đang trỏ tới note hiện tại.
- **Outgoing links**: note hiện tại đang trỏ tới đâu.
- **Outline**: mục lục tự động từ các tiêu đề.
- **Properties**: dữ liệu có cấu trúc của note.

Bạn có thể kéo biểu tượng hoặc tab để sắp xếp lại không gian làm việc.

## 3. Năm thao tác cần thuộc trước tiên

### Tạo note

Nhấn `Ctrl+N`, đặt một tên mô tả đúng nội dung, ví dụ `Nguyên lý thị giác Gestalt` thay vì `Ghi chú 1`.

### Mở nhanh note

Nhấn `Ctrl+O`, gõ một phần tên hoặc alias, rồi nhấn `Enter`. Nếu chưa có note trùng tên, Quick switcher cũng có thể tạo note mới.

### Đổi tên an toàn

Đổi tên từ **File explorer** trong Obsidian. Khi tùy chọn **Settings → Files and links → Automatically update internal links** được bật, các liên kết trỏ tới file sẽ được cập nhật theo.

### Di chuyển note

Kéo file vào thư mục khác trong File explorer. Không cần chia thư mục quá nhỏ ngay từ đầu; tìm kiếm và liên kết thường quan trọng hơn một cây thư mục hoàn hảo.

### Xóa và khôi phục

Trước khi dọn dẹp lớn, kiểm tra **Settings → Files and links → Deleted files**. Nên chọn chuyển file vào thùng rác hệ thống nếu bạn muốn có cơ hội khôi phục.

## 4. Phím tắt thiết yếu trên Windows

| Phím | Công dụng | Khi nên dùng |
| --- | --- | --- |
| `Ctrl+P` | Mở Command palette | Khi biết việc muốn làm nhưng không nhớ nút ở đâu |
| `Ctrl+O` | Mở Quick switcher | Mở hoặc tạo note theo tên |
| `Ctrl+N` | Tạo note mới | Ghi nhanh một ý mới |
| `Ctrl+Shift+F` | Tìm trong toàn vault | Tìm một ý, tag, task hoặc property |
| `Ctrl+F` | Tìm trong note hiện tại | Note dài |
| `Ctrl+B` | In đậm vùng chọn | Nhấn mạnh từ khóa |
| `Ctrl+I` | In nghiêng vùng chọn | Thuật ngữ hoặc sắc thái |
| `Ctrl+;` | Thêm property | Gắn metadata cho note |
| `Ctrl+W` | Đóng tab hiện tại | Dọn không gian làm việc |
| `Ctrl+S` | Lưu file | Obsidian tự lưu, nhưng phím này vẫn quen thuộc và an toàn |
| `Ctrl+Z` / `Ctrl+Y` | Hoàn tác / làm lại | Sửa thao tác nhầm |

> [!info] Phím tắt có thể tùy biến
> Vào **Settings → Hotkeys** để xem phím đang được gán trên thiết bị của bạn. Bạn có thể thêm hotkey cho `Templates: Insert template`, `Open today's daily note`, `Toggle reading view` và `Open local graph` sau khi đã dùng chúng thường xuyên.

## 5. Markdown căn bản

### Tiêu đề và cấu trúc

```markdown
# Tiêu đề cấp 1
## Tiêu đề cấp 2
### Tiêu đề cấp 3
```

Mỗi note thường chỉ cần một tiêu đề cấp 1. Dùng cấp 2 cho các phần chính và cấp 3 cho phần con. Bảng **Outline** sẽ tự biến chúng thành mục lục.

### Nhấn mạnh văn bản

```markdown
**in đậm**
*in nghiêng*
***vừa đậm vừa nghiêng***
==đánh dấu nổi bật==
~~gạch bỏ~~
`đoạn mã hoặc tên lệnh`
```

Kết quả: **in đậm**, *in nghiêng*, ==đánh dấu nổi bật==, ~~gạch bỏ~~ và `inline code`.

> [!tip] Đẹp nhờ tiết chế
> Một đoạn có quá nhiều chữ đậm, highlight và emoji sẽ làm mất thứ bậc thị giác. Chỉ highlight kết luận hoặc câu cần ôn lại.

### Danh sách và công việc

```markdown
- Ý chính
  - Ý phụ
  - Ý phụ khác

1. Bước đầu tiên
2. Bước tiếp theo

- [ ] Việc chưa làm
- [x] Việc đã hoàn thành
```

Bạn có thể bấm trực tiếp vào checkbox trong Reading view. Dùng `Tab` và `Shift+Tab` để tăng hoặc giảm cấp của mục danh sách.

### Trích dẫn và đường phân cách

```markdown
> Đây là một trích dẫn.
>
> Dòng thứ hai vẫn thuộc trích dẫn.

---
```

### Liên kết ngoài và ảnh

```markdown
[Obsidian Help](https://obsidian.md/help)
![Mô tả ảnh](https://example.com/image.png)
```

Với ảnh nằm trong vault, dùng cú pháp nhúng của Obsidian:

```markdown
![[ten-anh.png]]
![[ten-anh.png|500]]
```

Số `500` là chiều rộng theo pixel; ảnh tự giữ tỉ lệ.

### Khối mã

Một dấu backtick dùng cho `mã nằm trong câu`. Ba dấu backtick tạo khối mã và tên ngôn ngữ giúp tô màu cú pháp:

````markdown
```css
.note {
  color: rebeccapurple;
}
```
````

## 6. Mẫu note gọn, rõ và đẹp

Sao chép mẫu này vào một note luyện tập:

```markdown
# Tên chủ đề

> [!summary] Tóm tắt một câu
> Viết kết luận quan trọng nhất ở đây.

## Tôi muốn trả lời câu hỏi gì?

- Câu hỏi 1
- Câu hỏi 2

## Ý chính

1. **Khái niệm:** giải thích bằng lời của mình.
2. **Ví dụ:** một trường hợp cụ thể.
3. **Ứng dụng:** điều mình sẽ làm khác đi.

## Điều chưa hiểu

- [ ] Câu hỏi cần tìm thêm

## Liên quan

- [[Tên note liên quan]]

## Nguồn

- [Tên nguồn](https://example.com)
```

Note đẹp trước hết nhờ **cấu trúc nhất quán**, khoảng trắng hợp lý và tiêu đề rõ; màu sắc chỉ là lớp hoàn thiện sau cùng.

## 7. Quy trình 10 phút mỗi ngày

1. Nhấn `Ctrl+N` và ghi một ý duy nhất cho mỗi note.
2. Đặt tiêu đề mô tả được ý đó.
3. Viết tóm tắt bằng lời của bạn ở đầu note.
4. Thêm ít nhất một liên kết `[[...]]` tới note khác.
5. Đánh dấu câu hỏi còn mở bằng task `- [ ]`.
6. Cuối tuần, tìm các note chưa có liên kết và bổ sung quan hệ.

## 8. Bài thực hành

- [ ] Tạo note `Obsidian là gì theo cách hiểu của tôi`.
- [ ] Dùng ít nhất ba cấp tiêu đề.
- [ ] Thêm một danh sách, một task và một callout.
- [ ] Chèn một liên kết ngoài và một ảnh.
- [ ] Dùng `Ctrl+O` để quay lại note này.
- [ ] Mở Outline và kiểm tra cấu trúc.

> [!success] Hoàn thành khi
> Bạn có thể tạo, định dạng và tìm lại note mà gần như không cần dùng chuột.

## Bài tiếp theo

Tiếp tục với [[02 - Xây dựng kho kiến thức]] để học liên kết nội bộ, Backlinks, Properties, Tags, Search, Daily notes và Templates.

## Tài liệu chính thức

- [Basic formatting syntax — Obsidian Help](https://obsidian.md/help/Editing%2Band%2Bformatting/Basic%2Bformatting%2Bsyntax)
- [Hotkeys — Obsidian Help](https://obsidian.md/help/User%2Binterface/Hotkeys)
- [Command palette — Obsidian Help](https://obsidian.md/help/Plugins/Command%2Bpalette)
- [Quick switcher — Obsidian Help](https://obsidian.md/help/Plugins/Quick%2Bswitcher)

