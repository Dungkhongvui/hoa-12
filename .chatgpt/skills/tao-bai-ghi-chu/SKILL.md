# Skill: tạo bài ghi chú

## 1. Tên và cách kích hoạt

**Tên skill:** `tạo bài ghi chú`

Skill được kích hoạt khi người dùng nói tự nhiên hoặc dùng lệnh slash.

### Cách nói tự nhiên

Ví dụ:

- `Tạo bài ghi chú về đại cương kim loại`
- `Làm cho tôi một note về kim loại kiềm`
- `Viết ghi chú Markdown cho phần phức chất`
- `Tạo bài ghi chú dạng kỹ năng giải bài tập oxi hóa khử`
- `Tạo note nâng cao về điện phân`

### Lệnh slash gợi ý

```text
/tao-bai-ghi-chu
/note
/ghi-chu
```

Có thể dùng kèm tham số tự nhiên:

```text
/tao-bai-ghi-chu chủ đề: kim loại kiềm; loại: lý thuyết cơ bản
/ghi-chu chủ đề: phức chất; loại: lý thuyết nâng cao
/note chủ đề: bài toán CO2 tác dụng với kiềm; loại: kỹ năng giải bài tập nâng cao
```

---

## 2. Mục tiêu

Tạo ra **một file Markdown hoàn chỉnh** cho một chủ đề học tập.

File ghi chú phải thuộc một trong bốn loại sau:

1. **Lý thuyết cơ bản + ví dụ**
2. **Lý thuyết nâng cao + ví dụ**
3. **Phương pháp/kỹ năng giải bài tập cơ bản + ví dụ**
4. **Phương pháp/kỹ năng giải bài tập nâng cao + ví dụ**

Kết quả cuối cùng cần có:

- Tên file `.md` rõ ràng, dễ tìm.
- Nội dung trình bày theo cấu trúc học được ngay.
- Có ví dụ minh họa khi cần.
- Có phần lưu ý/sai lầm thường gặp.
- Có đường dẫn file sau khi tạo xong.

---

## 3. Quy trình thực thi

Khi skill được kích hoạt, làm theo đúng thứ tự:

### Bước 1: Hỏi chủ đề ghi chú

Nếu người dùng chưa nói rõ chủ đề, hỏi:

> Chủ đề ghi chú là gì?

Ví dụ chủ đề:

- Đại cương kim loại
- Kim loại nhóm IA
- Kim loại nhóm IIA
- Kim loại chuyển tiếp
- Phức chất
- Ăn mòn kim loại
- Điều chế kim loại
- Bài toán CO2 tác dụng với dung dịch kiềm

### Bước 2: Chọn loại ghi chú phù hợp

Nếu người dùng chưa nói rõ loại ghi chú, hỏi người dùng chọn một trong bốn loại:

1. Lý thuyết cơ bản
2. Lý thuyết nâng cao
3. Phương pháp/kỹ năng giải bài tập cơ bản
4. Phương pháp/kỹ năng giải bài tập nâng cao

Nếu có thể suy luận hợp lý từ yêu cầu, đề xuất loại ghi chú và xác nhận ngắn.

### Bước 3: Đọc tài liệu nguồn

Ưu tiên nguồn theo thứ tự:

1. Nội dung người dùng paste trực tiếp vào chat.
2. Ảnh, file, đề bài, tài liệu người dùng gửi.
3. File trong repo nếu người dùng cung cấp đường dẫn cụ thể.
4. Kiến thức nền đã biết, nhưng phải ghi rõ khi không có tài liệu nguồn riêng.

Không tự bịa nguồn. Nếu thiếu tài liệu để viết chắc chắn, hỏi người dùng bổ sung.

### Bước 4: Trình bày lại theo khung What - Why - How - Lưu ý

Mọi bài ghi chú cần được tổ chức lại để dễ học, không chỉ chép lại tài liệu nguồn.

Khung lõi:

```markdown
# Tên chủ đề

## 1. What - Đây là gì?

## 2. Why - Vì sao cần học phần này?

## 3. How - Cách hiểu/cách làm/cách áp dụng

## 4. Ví dụ minh họa

## 5. Lưu ý khi áp dụng

## 6. Sai lầm thường gặp

## 7. Checklist tự kiểm tra
```

Tùy loại ghi chú mà điều chỉnh:

- Lý thuyết: nhấn mạnh khái niệm, bản chất, dấu hiệu nhận biết, ví dụ.
- Kỹ năng bài tập: nhấn mạnh quy trình giải, dạng bài, dấu hiệu chọn phương pháp, bẫy.

### Bước 5: Duyệt lại và thêm ví dụ nếu cần

Kiểm tra:

- Có đủ What - Why - How chưa?
- Có ví dụ chưa?
- Có lưu ý/sai lầm thường gặp chưa?
- Có phù hợp với học sinh/lớp học/ngữ cảnh của người dùng chưa?

### Bước 6: Kiểm tra lại cho đến khi đúng ý

Nếu người dùng yêu cầu sửa, chỉnh theo hướng:

- Rút gọn
- Chi tiết hơn
- Dễ hiểu hơn
- Thêm ví dụ
- Thêm bài tập tự luyện
- Tách thành nhiều file
- Chuyển thành mindmap/Mermaid

### Bước 7: Báo đường dẫn file `.md`

Sau khi tạo file, báo lại:

```text
Đã tạo file: <đường-dẫn-file.md>
```

Nếu ghi lên GitHub, luôn cung cấp đường dẫn repo/path hoặc pull request nếu làm qua branch.

---

## 4. Quy tắc ghi file

### Tên file

Dùng tên file không dấu, chữ thường, nối bằng dấu gạch ngang.

Ví dụ:

```text
notes/dai-cuong-kim-loai.md
notes/phuc-chat-ly-thuyet-nang-cao.md
notes/co2-tac-dung-voi-kiem-ky-nang-nang-cao.md
```

### Cấu trúc thư mục đề xuất

```text
notes/
├── ly-thuyet-co-ban/
├── ly-thuyet-nang-cao/
├── ky-nang-co-ban/
└── ky-nang-nang-cao/
```

### Khi ghi lên GitHub

Chỉ commit trực tiếp khi người dùng đã xác nhận rõ:

- Repo
- Branch
- Cách làm: commit trực tiếp hoặc tạo branch + pull request

Nếu có khả năng ghi đè file cũ, phải hỏi lại trước.

---

## 5. Quy tắc chất lượng

- Không viết lan man; ưu tiên cấu trúc học được ngay.
- Không chỉ tóm tắt; phải tổ chức lại kiến thức theo logic học tập.
- Không bịa dữ kiện, công thức, phản ứng hoặc kết luận.
- Nếu không chắc, ghi rõ mức độ chưa chắc và cần nguồn kiểm chứng.
- Với Hóa học, cần cân bằng phương trình khi đưa phản ứng.
- Với bài tập, cần chỉ rõ dấu hiệu nhận biết dạng bài.
- Với lý thuyết dài, cần có bảng so sánh hoặc checklist.
- Với nội dung quan trọng, thêm ví dụ ngắn ngay sau phần lý thuyết.

---

## 6. Câu hỏi cần hỏi thêm khi thiếu thông tin

Hỏi ngắn, tối đa 3 câu/lượt:

1. Chủ đề ghi chú là gì?
2. Bạn muốn loại ghi chú nào: lý thuyết cơ bản, lý thuyết nâng cao, kỹ năng cơ bản, hay kỹ năng nâng cao?
3. Có tài liệu nguồn/file/ảnh nào cần bám theo không?

Nếu người dùng yêu cầu ghi GitHub, hỏi thêm khi chưa rõ:

1. Ghi vào repo nào?
2. Commit trực tiếp hay tạo branch + pull request?
3. Đường dẫn thư mục/file mong muốn là gì?

---

## 7. Đầu ra chuẩn

Khi hoàn thành, trả lời ngắn gọn:

```markdown
Đã tạo bài ghi chú.

- Chủ đề: ...
- Loại ghi chú: ...
- File: `.../...md`
- Ghi chú: ...
```
