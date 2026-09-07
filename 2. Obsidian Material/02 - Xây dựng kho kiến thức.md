---
title: "Xây dựng kho kiến thức trong Obsidian"
aliases:
  - "Obsidian trung cấp"
  - "Liên kết và tổ chức note"
tags:
  - learning/obsidian
  - guide/intermediate
level: intermediate
status: reference
created: 2026-08-19
updated: 2026-08-19
description: "Tổ chức note bằng links, backlinks, tags, properties, search, daily notes và templates."
---

# 02 — Xây dựng kho kiến thức

> [!abstract] Mục tiêu
> Sau bài này, vault của bạn không còn là một chồng tài liệu. Mỗi note có thể được tìm bằng nhiều đường: thư mục, liên kết, tag, property, tìm kiếm và note trung tâm.

Nếu chưa quen Markdown và phím tắt, hãy đọc [[01 - Obsidian nhập môn]] trước.

## 1. Bốn công cụ tổ chức và vai trò của chúng

| Công cụ | Trả lời câu hỏi | Ví dụ |
| --- | --- | --- |
| **Folder** | File đang sống ở đâu? | `Diary/`, `Projects/`, `Sources/` |
| **Link** | Ý này liên quan trực tiếp tới ý nào? | `[[Màu sắc]]` liên kết `[[Tương phản]]` |
| **Tag** | Note thuộc nhóm trạng thái/chủ đề xuyên thư mục nào? | `#status/draft`, `#source/book` |
| **Property** | Dữ liệu có cấu trúc của note là gì? | `status`, `created`, `rating`, `author` |

Một quy tắc dễ nhớ:

- Dùng **folder** cho nơi chứa ổn định.
- Dùng **link** cho quan hệ có ý nghĩa.
- Dùng **tag** cho nhãn cần lọc xuyên nhiều nơi.
- Dùng **property** cho dữ liệu cần sắp xếp, lọc hoặc hiển thị trong Bases.

> [!warning] Tránh tổ chức quá sớm
> Đừng tạo hàng chục folder và tag khi vault mới có vài note. Chỉ thêm một cấu trúc khi bạn thực sự cần tìm hoặc nhóm thông tin theo cấu trúc đó.

## 2. Liên kết nội bộ — trái tim của Obsidian

### Liên kết tới một note

Gõ `[[` rồi nhập tên note:

```markdown
[[Tên note]]
[[Tên note|văn bản hiển thị]]
```

Bạn có thể liên kết đến note chưa tồn tại. Liên kết sẽ có màu khác; bấm vào nó để tạo note mới.

### Liên kết tới một tiêu đề

```markdown
[[Tên note#Tên mục]]
[[Tên note#Tên mục|đọc phần giải thích]]
[[#Một mục trong chính note này]]
```

Gõ `[[##` để tìm tiêu đề trên toàn vault. Đây là cách tốt để trỏ thẳng đến một phần cụ thể thay vì bắt người đọc mở cả note dài.

### Liên kết tới một block

Thêm block ID vào cuối một đoạn:

```markdown
Đây là kết luận có thể tái sử dụng ở nơi khác. ^ket-luan
```

Sau đó liên kết bằng:

```markdown
[[Tên note#^ket-luan]]
```

Block ID chỉ gồm chữ Latin, số và dấu gạch ngang. Bạn cũng có thể gõ `[[Tên note#^` rồi chọn block từ gợi ý mà không cần tự đặt ID.

### Alias — nhiều tên, một note

Nếu một khái niệm có tên viết tắt hoặc tên tiếng Anh, thêm `aliases` vào Properties:

```yaml
---
aliases:
  - AI
  - Trí tuệ máy
---
```

Khi chọn alias `AI`, Obsidian tạo liên kết dạng `[[Artificial Intelligence|AI]]`, vì vậy vẫn trỏ đúng file gốc.

## 3. Backlinks, Outgoing links và Page preview

- **Outgoing links** cho biết note hiện tại nhắc đến note nào.
- **Backlinks** cho biết note nào đang nhắc đến note hiện tại.
- **Unlinked mentions** tìm nơi tên hoặc alias xuất hiện nhưng chưa trở thành link.
- **Page preview** cho phép xem trước note khi giữ `Ctrl` và rê chuột lên liên kết trong chế độ chỉnh sửa.

Một thói quen tốt khi hoàn tất note:

1. Mở Backlinks.
2. Xem các unlinked mentions có thật sự cùng khái niệm không.
3. Chỉ chuyển những quan hệ có ý nghĩa thành link.
4. Viết một cụm từ giải thích quan hệ, thay vì đặt link trơ trọi.

Ví dụ tốt:

```markdown
Nguyên tắc này bổ sung cho [[Tương phản thị giác]] vì cả hai đều giúp tạo thứ bậc thông tin.
```

## 4. Nhúng để tái sử dụng nội dung

Thêm `!` trước wikilink để hiển thị nội dung nguồn ngay trong note hiện tại:

```markdown
![[Tên note]]
![[Tên note#Một mục]]
![[Tên note#^ket-luan]]
![[hinh-anh.png|600]]
![[tai-lieu.pdf#page=3]]
```

Nội dung nhúng luôn cập nhật khi file nguồn thay đổi. Đây là cách tạo dashboard hoặc note tổng hợp mà không sao chép nội dung.

> [!example] Khi nào nên nhúng?
> Một định nghĩa chuẩn được dùng ở nhiều bài, một danh sách tài nguyên chung, một trang cụ thể của PDF hoặc một hình minh họa cần xuất hiện trong note học tập.

## 5. Callout — làm nổi bật đúng chỗ

Cú pháp cơ bản:

```markdown
> [!note] Tiêu đề tùy chọn
> Nội dung callout.
```

Các kiểu hữu ích:

```markdown
> [!abstract] Tóm tắt
> Ý chính của note.

> [!tip] Mẹo
> Một cách làm hiệu quả.

> [!warning] Cảnh báo
> Rủi ro cần tránh.

> [!example] Ví dụ
> Một trường hợp cụ thể.

> [!question] Câu hỏi mở
> Điều cần nghiên cứu thêm.

> [!success] Kết luận
> Kết quả đã xác nhận.
```

Thêm `-` để callout mặc định thu gọn, hoặc `+` để mở nhưng cho phép thu gọn:

```markdown
> [!faq]- Chi tiết bổ sung
> Bấm vào tiêu đề để mở nội dung.
```

Callout hỗ trợ Markdown, wikilink và embed. Dùng tối đa một hoặc hai callout quan trọng trong mỗi màn hình để tránh “nhiễu màu”.

## 6. Properties — metadata có cấu trúc

Properties nằm ở đầu file và được lưu dưới dạng YAML:

```yaml
---
title: "Tên note"
aliases:
  - "Tên khác"
tags:
  - topic/design
  - status/learning
type: concept
status: active
created: 2026-08-19
rating: 4
reviewed: false
related:
  - "[[Một note khác]]"
---
```

Các kiểu property chính gồm text, list, number, checkbox, date, date-time và tags. Một tên property nên luôn giữ cùng ý nghĩa và kiểu dữ liệu trên toàn vault.

### Bộ property tối thiểu nên dùng

| Property | Ý nghĩa | Giá trị gợi ý |
| --- | --- | --- |
| `type` | Loại note | `concept`, `source`, `project`, `daily` |
| `status` | Trạng thái xử lý | `inbox`, `active`, `reference`, `archive` |
| `created` | Ngày tạo | `YYYY-MM-DD` |
| `tags` | Nhóm xuyên thư mục | danh sách tag |
| `aliases` | Tên thay thế | danh sách tên |

> [!tip] Ít nhưng nhất quán
> Bắt đầu với 3–5 property. Chỉ thêm property mới khi bạn đã biết mình sẽ tìm, lọc hoặc sắp xếp theo nó.

## 7. Tags có chiến lược

Tag lồng nhau dùng dấu `/`:

```markdown
#status/inbox
#status/learning
#source/book
#source/article
#topic/design
```

Không dùng khoảng trắng trong tag. Bạn có thể dùng `kebab-case`, `snake_case` hoặc chữ Unicode.

Tránh tạo tag chỉ xuất hiện một lần và không giúp lọc. Với quan hệ cụ thể giữa hai ý tưởng, link thường có giá trị hơn tag.

## 8. Search — tìm chính xác thay vì nhớ vị trí

Nhấn `Ctrl+Shift+F`. Một số truy vấn hữu ích:

| Truy vấn | Kết quả |
| --- | --- |
| `"design system"` | Cụm từ chính xác |
| `typography -web` | Có `typography` nhưng không có `web` |
| `file:meeting` | Tên file chứa `meeting` |
| `path:"Obsidian Material"` | File trong đường dẫn này |
| `tag:#status/learning` | Note có tag đó hoặc tag con phù hợp |
| `task-todo:` | Các task chưa hoàn thành |
| `task-todo:review` | Task chưa xong có chữ `review` |
| `[status:active]` | Property `status` bằng `active` |
| `[rating:>3]` | Property số lớn hơn 3 |

Bạn có thể nhúng kết quả tìm kiếm động vào note:

````markdown
```query
tag:#status/learning task-todo:
```
````

Trong Reading view, khối này tự hiển thị kết quả hiện tại của vault.

## 9. Templates — ngừng lặp lại cấu trúc

### Thiết lập

1. Tạo folder, ví dụ `Templates`.
2. Vào **Settings → Templates → Template folder location**.
3. Chọn folder vừa tạo.
4. Dùng Command palette: `Templates: Insert template`.
5. Khi đã quen, gán một hotkey riêng cho lệnh này.

### Mẫu note học tập

```markdown
---
title: "{{title}}"
tags:
  - status/learning
type: concept
status: active
created: "{{date:YYYY-MM-DD}}"
---

# {{title}}

> [!abstract] Tóm tắt
> Viết 2–3 câu bằng lời của mình.

## Câu hỏi trung tâm

- 

## Ý chính

### 1.

### 2.

## Ví dụ hoặc ứng dụng

## Điều còn chưa rõ

- [ ] 

## Liên quan

- [[]]

## Nguồn

- 
```

> [!warning] Sửa template ở Source mode
> Các biến như `{{date}}` trong Properties nên được đặt trong dấu ngoặc kép. Source mode giúp tránh giao diện Properties ghi đè biến trước khi template được chèn.

## 10. Daily notes — hộp thư đến theo thời gian

Daily note phù hợp với nhật ký, task trong ngày, cuộc gặp và các ý chưa kịp phân loại.

Thiết lập ở **Settings → Daily notes**:

- **Date format**: nên dùng `YYYY-MM-DD` để sắp xếp đúng theo thời gian.
- **New file location**: chọn folder `Diary` hiện có của bạn nếu muốn nhật ký nằm cùng một nơi.
- **Template file location**: chọn một template ngày.

Mẫu đơn giản:

```markdown
---
tags:
  - daily
type: daily
date: "{{date:YYYY-MM-DD}}"
---

# {{date:YYYY-MM-DD}}

## Ưu tiên hôm nay

- [ ] 

## Nhật ký

- {{time}} — 

## Điều đã học

- 

## Note đã tạo

- [[]]

## Tổng kết

- Điều tốt:
- Điều cần cải thiện:
```

Daily note là nơi **ghi nhanh**, không nhất thiết là nơi giữ kiến thức cuối cùng. Khi một ý đủ quan trọng, tách nó thành note riêng rồi liên kết ngược lại ngày đã ghi.

## 11. MOC — note mục lục theo chủ đề

MOC (Map of Content) là một note trung tâm do bạn chủ động sắp xếp. Ví dụ:

```markdown
# MOC — Thiết kế

> [!abstract] Mục tiêu
> Bản đồ các chủ đề thiết kế tôi đang học.

## Nền tảng

- [[Màu sắc]] — cách phối và tạo ý nghĩa
- [[Typography]] — thứ bậc và khả năng đọc
- [[Bố cục]] — tổ chức không gian

## Đang học

- [ ] [[Design systems]]

## Dự án áp dụng

- [[Thiết kế portfolio cá nhân]]
```

Khác với Graph view, MOC thể hiện **thứ tự và diễn giải do bạn lựa chọn**. Hãy tạo MOC khi một chủ đề đã có khoảng 5–10 note liên quan.

## 12. Quy trình xử lý kiến thức

```text
Ghi nhanh → Làm rõ → Liên kết → Tổng hợp → Ôn lại → Áp dụng
```

1. **Ghi nhanh** vào Daily note hoặc note `inbox`.
2. **Làm rõ** bằng lời của chính bạn; một note tập trung vào một ý.
3. **Liên kết** tới bối cảnh, nguồn và khái niệm liên quan.
4. **Tổng hợp** trong MOC khi số note tăng lên.
5. **Ôn lại** note có status `active` hoặc task chưa xong.
6. **Áp dụng** vào một dự án, quyết định hoặc sản phẩm cụ thể.

## Bài thực hành

- [ ] Thêm Properties cho ba note hiện có.
- [ ] Tạo một alias và thử mở bằng `Ctrl+O`.
- [ ] Tạo link tới heading và link tới block.
- [ ] Nhúng một heading của note này vào note thử nghiệm.
- [ ] Tạo một template note học tập.
- [ ] Thiết lập Daily notes dùng folder `Diary` nếu phù hợp với cách bạn đang viết nhật ký.
- [ ] Tạo một MOC cho chủ đề bạn đang học.

> [!success] Hoàn thành khi
> Một note mới của bạn có cấu trúc nhất quán, có thể tìm bằng Search/Properties và có ít nhất hai liên kết có ý nghĩa.

## Bài tiếp theo

Tiếp tục với [[03 - Hệ thống nâng cao và làm đẹp]] để dùng Bases, Graph, Canvas, truy vấn động và CSS snippets.

## Tài liệu chính thức

- [Internal links — Obsidian Help](https://obsidian.md/help/Linking%2Bnotes%2Band%2Bfiles/Internal%2Blinks)
- [Embed files — Obsidian Help](https://obsidian.md/help/Linking%2Bnotes%2Band%2Bfiles/Embed%2Bfiles)
- [Callouts — Obsidian Help](https://obsidian.md/help/Editing%2Band%2Bformatting/Callouts)
- [Properties — Obsidian Help](https://obsidian.md/help/Editing%2Band%2Bformatting/Properties)
- [Search — Obsidian Help](https://obsidian.md/help/Plugins/Search)
- [Templates — Obsidian Help](https://obsidian.md/help/Plugins/Templates)
- [Daily notes — Obsidian Help](https://obsidian.md/help/Plugins/Daily%2Bnotes)

