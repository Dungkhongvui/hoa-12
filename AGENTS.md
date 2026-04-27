# AGENTS.md

## 1. Bối cảnh dự án

Repo này là kho học tập và soạn tài liệu cho môn **Hóa học lớp 12**.

Mục tiêu chính của repo:

- Tạo ghi chú học tập dạng Markdown cho từng chủ đề Hóa 12.
- Chuẩn hóa cách viết ghi chú để học sinh học được ngay.
- Tách nội dung theo loại: lý thuyết cơ bản, lý thuyết nâng cao, kỹ năng giải bài tập cơ bản, kỹ năng giải bài tập nâng cao.
- Dùng repo như một kho tri thức có thể mở rộng dần, thay vì mỗi lần viết lại từ đầu.

Người dùng muốn agent khi vào dự án có thể hiểu nhanh:

1. Repo dùng để làm gì.
2. Có những skill nào.
3. Khi người dùng gọi skill thì phải đọc và làm theo đúng quy trình.
4. File mới nên đặt ở đâu, đặt tên thế nào, viết theo cấu trúc nào.

---

## 2. Mục tiêu sử dụng repo

Repo `hoa-12` được dùng để hỗ trợ các nhiệm vụ học tập và giảng dạy Hóa 12, đặc biệt là:

- Tạo bài ghi chú theo từng chủ đề.
- Chuyển kiến thức rời rạc thành cấu trúc dễ học.
- Viết nội dung Markdown để lưu trữ, chỉnh sửa và tái sử dụng.
- Tạo nền cho các tài liệu tiếp theo như mindmap, bài tập tự luyện, đề kiểm tra, bảng so sánh.

Khi làm việc trong repo này, agent cần ưu tiên tính **dễ học, đúng bản chất, đúng quy trình** hơn là viết thật dài.

---

## 3. Ngôn ngữ và phong cách trả lời

- Trả lời bằng **tiếng Việt**.
- Viết rõ ràng, có cấu trúc, dễ học lại.
- Ưu tiên giải thích bản chất, không chỉ chép kiến thức.
- Với Hóa học, phải cân bằng phương trình khi đưa phản ứng.
- Không bịa nguồn, không bịa công thức, không bịa phản ứng.
- Nếu dùng kiến thức nền thay vì tài liệu riêng, phải ghi rõ trong bài.
- Khi chưa chắc, nói rõ mức độ chưa chắc và đề xuất cần tài liệu kiểm chứng.

---

## 4. Cấu trúc repo hiện tại

Các phần quan trọng:

```text
.chatgpt/
└── skills/
    └── tao-bai-ghi-chu/
        └── SKILL.md

notes/
└── ly-thuyet-co-ban/
    └── ester.md
```

Ý nghĩa:

- `.chatgpt/skills/`: nơi chứa các skill mà người dùng có thể gọi bằng ngôn ngữ tự nhiên hoặc lệnh slash.
- `notes/`: nơi lưu các bài ghi chú học tập.
- `notes/ly-thuyet-co-ban/`: ghi chú lý thuyết cơ bản.

---

## 5. Quy tắc bắt buộc khi xử lý skill

Khi người dùng gọi một skill, ví dụ:

```text
/tao-bai-ghi-chu
/ghi-chu
/note
Tạo bài ghi chú...
```

Agent phải làm theo thứ tự:

1. Tìm và đọc file skill tương ứng trong `.chatgpt/skills/.../SKILL.md`.
2. Xác định người dùng đã cung cấp đủ thông tin chưa.
3. Nếu thiếu thông tin, hỏi đúng câu mà skill yêu cầu.
4. Không tự ý bỏ qua bước.
5. Không hỏi dồn quá nhiều nếu skill quy định hỏi theo từng bước.
6. Sau khi đủ thông tin, mới tạo nội dung hoặc ghi file.
7. Nếu ghi file lên GitHub, phải kiểm tra file đã tồn tại chưa để tránh ghi đè.
8. Sau khi hoàn thành, báo lại file path và commit/PR nếu có.

Bài học từ lần sử dụng đầu tiên:

> Người dùng kỳ vọng agent **follow đúng quy trình trong skill**, không chỉ hiểu ý chung rồi tự làm.

---

## 6. Skill hiện có: `tao-bai-ghi-chu`

Đường dẫn:

```text
.chatgpt/skills/tao-bai-ghi-chu/SKILL.md
```

Tên skill:

```text
tạo bài ghi chú
```

Cách kích hoạt thường gặp:

```text
/tao-bai-ghi-chu
/note
/ghi-chu
Tạo bài ghi chú về ...
Làm cho tôi một note về ...
Viết ghi chú Markdown cho ...
```

Mục tiêu của skill:

- Tạo một file Markdown hoàn chỉnh cho một chủ đề học tập.
- Nội dung phải học được ngay.
- Có ví dụ minh họa.
- Có lưu ý và sai lầm thường gặp.
- Có checklist tự kiểm tra.

---

## 7. Quy trình chuẩn khi tạo bài ghi chú

Khi skill `tao-bai-ghi-chu` được kích hoạt, phải đi theo thứ tự sau.

### Bước 1: Hỏi chủ đề ghi chú

Nếu người dùng chưa nói rõ chủ đề, hỏi:

```text
Chủ đề ghi chú là gì?
```

Ví dụ chủ đề:

- Đại cương kim loại
- Kim loại nhóm IA
- Kim loại nhóm IIA
- Kim loại chuyển tiếp
- Phức chất
- Ăn mòn kim loại
- Điều chế kim loại
- Ester
- Lipid
- Amin
- Amino acid
- Polime

### Bước 2: Hỏi loại ghi chú

Nếu người dùng chưa nói rõ loại, hỏi người dùng chọn một trong bốn loại:

```text
1. Lý thuyết cơ bản
2. Lý thuyết nâng cao
3. Phương pháp/kỹ năng giải bài tập cơ bản
4. Phương pháp/kỹ năng giải bài tập nâng cao
```

### Bước 3: Hỏi tài liệu nguồn

Nếu người dùng chưa cung cấp nguồn, hỏi:

```text
Có tài liệu nguồn/file/ảnh nào cần bám theo không?
```

Có thể cho người dùng chọn:

```text
1. Chưa có tài liệu riêng -> dùng kiến thức nền và ghi rõ trong bài.
2. Có tài liệu riêng -> gửi ảnh/file/nội dung để bám theo.
```

### Bước 4: Tạo nội dung theo khung lõi

Mọi bài ghi chú cần có khung:

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

Với **lý thuyết**, nhấn mạnh:

- Khái niệm.
- Bản chất.
- Công thức hoặc nhóm chức nếu có.
- Tính chất.
- Dấu hiệu nhận biết.
- Ví dụ ngắn.
- So sánh nếu dễ nhầm.

Với **kỹ năng bài tập**, nhấn mạnh:

- Dạng bài.
- Dấu hiệu nhận biết dạng.
- Quy trình giải.
- Công thức thường dùng.
- Bẫy/sai lầm.
- Ví dụ mẫu có lời giải.

---

## 8. Quy tắc đặt tên file và thư mục

Tên file:

- Không dấu.
- Chữ thường.
- Các từ nối bằng dấu gạch ngang `-`.
- Đuôi `.md`.

Ví dụ:

```text
ester.md
phuc-chat.md
kim-loai-kiem.md
co2-tac-dung-voi-kiem.md
```

Cấu trúc thư mục đề xuất:

```text
notes/
├── ly-thuyet-co-ban/
├── ly-thuyet-nang-cao/
├── ky-nang-co-ban/
└── ky-nang-nang-cao/
```

Ánh xạ loại ghi chú sang thư mục:

| Loại ghi chú | Thư mục |
|---|---|
| Lý thuyết cơ bản | `notes/ly-thuyet-co-ban/` |
| Lý thuyết nâng cao | `notes/ly-thuyet-nang-cao/` |
| Kỹ năng giải bài tập cơ bản | `notes/ky-nang-co-ban/` |
| Kỹ năng giải bài tập nâng cao | `notes/ky-nang-nang-cao/` |

Ví dụ file đã tạo:

```text
notes/ly-thuyet-co-ban/ester.md
```

---

## 9. Chuẩn chất lượng nội dung Hóa học

Khi viết nội dung Hóa học:

- Phải cân bằng phương trình phản ứng.
- Phải phân biệt rõ điều kiện phản ứng nếu có.
- Phải ghi rõ môi trường phản ứng: acid, kiềm, nhiệt độ, xúc tác.
- Không dùng công thức tổng quát ngoài phạm vi áp dụng.
- Với mỗi công thức quan trọng, nên ghi điều kiện áp dụng.
- Với phần dễ nhầm, thêm bảng so sánh.
- Với lý thuyết dài, thêm checklist cuối bài.
- Với bài tập, luôn nêu dấu hiệu nhận biết dạng bài trước khi nêu cách giải.

Ví dụ quy tắc phạm vi áp dụng:

```text
CnH2nO2 chỉ áp dụng chắc cho ester no, đơn chức, mạch hở.
```

Không được viết thành quy luật cho mọi ester.

---

## 10. Quy trình ghi file lên GitHub

Trước khi ghi file:

1. Xác định repo đang làm việc. Với dự án này là:

   ```text
   Dungkhongvui/hoa-12
   ```

2. Xác định branch. Mặc định hiện tại:

   ```text
   main
   ```

3. Kiểm tra file đích đã tồn tại chưa.
4. Nếu file đã tồn tại, không ghi đè khi chưa hỏi lại người dùng.
5. Nếu file chưa tồn tại và người dùng đã yêu cầu tạo file, có thể tạo file mới.
6. Commit message nên ngắn gọn, rõ hành động.

Ví dụ commit message:

```text
Add basic ester note
Add AGENTS project instructions
```

Sau khi ghi file, báo lại:

```markdown
Đã tạo file.

- File: `...`
- Repo: `...`
- Branch: `...`
- Commit: `...`
```

---

## 11. Mẫu đầu ra khi hoàn thành bài ghi chú

Khi tạo xong bài ghi chú, trả lời ngắn gọn:

```markdown
Đã tạo bài ghi chú.

- Chủ đề: ...
- Loại ghi chú: ...
- File: `.../...md`
- Repo: `Dungkhongvui/hoa-12`
- Branch: `main`
- Commit: `...`
- Ghi chú: ...
```

Không cần dán toàn bộ nội dung file nếu đã ghi lên GitHub, trừ khi người dùng yêu cầu xem lại.

---

## 12. Ví dụ luồng làm việc đúng

Nếu người dùng nói:

```text
/tao-bai-ghi-chu
```

Agent nên làm:

1. Đọc `.chatgpt/skills/tao-bai-ghi-chu/SKILL.md`.
2. Hỏi: `Chủ đề ghi chú là gì?`
3. Sau khi người dùng trả lời chủ đề, hỏi loại ghi chú.
4. Sau khi người dùng trả lời loại, hỏi tài liệu nguồn.
5. Sau khi đủ thông tin, viết bài.
6. Chọn path theo loại ghi chú.
7. Kiểm tra file tồn tại.
8. Tạo file.
9. Báo lại kết quả.

Ví dụ luồng đã thực hiện:

```text
User: tạo bài ghi chú
Assistant: Chủ đề ghi chú là gì?
User: Ester
Assistant: Bạn muốn loại ghi chú nào?
User: 1. Lý thuyết cơ bản
Assistant: Có tài liệu nguồn/file/ảnh nào cần bám theo không?
User: Chưa có tài liệu riêng
Assistant: Tạo notes/ly-thuyet-co-ban/ester.md
```

---

## 13. Điều cần tránh

- Không bỏ qua file skill khi người dùng đang gọi skill.
- Không tự suy luận quá nhanh rồi làm sai quy trình.
- Không hỏi cùng lúc quá nhiều câu nếu skill đã quy định từng bước.
- Không ghi đè file cũ khi chưa kiểm tra.
- Không tạo nội dung chung chung, lan man.
- Không tạo bài chỉ có lý thuyết mà thiếu ví dụ, lưu ý, sai lầm thường gặp, checklist.
- Không ghi nguồn giả.
- Không dùng công thức hoặc phản ứng chưa chắc chắn.

---

## 14. Định hướng mở rộng repo

Trong tương lai, repo có thể bổ sung thêm:

```text
.chatgpt/skills/tao-mindmap/
.chatgpt/skills/tao-bai-tap-tu-luyen/
.chatgpt/skills/tao-de-kiem-tra/
.chatgpt/skills/chuyen-ghi-chu-thanh-mermaid/
```

Nếu có skill mới, mỗi skill nên có file:

```text
.chatgpt/skills/<ten-skill>/SKILL.md
```

Mỗi skill cần mô tả rõ:

- Tên skill.
- Cách kích hoạt.
- Mục tiêu.
- Quy trình từng bước.
- Quy tắc ghi file.
- Đầu ra chuẩn.

---

## 15. Tóm tắt dành cho agent

Đây là repo học Hóa 12 bằng Markdown.

Khi làm việc trong repo này:

1. Luôn kiểm tra `AGENTS.md` trước để hiểu bối cảnh.
2. Nếu người dùng gọi skill, đọc file skill trong `.chatgpt/skills/.../SKILL.md`.
3. Với skill tạo bài ghi chú, phải hỏi đủ 3 nhóm thông tin: chủ đề, loại ghi chú, nguồn tài liệu.
4. Viết theo khung What - Why - How - Ví dụ - Lưu ý - Sai lầm - Checklist.
5. Ghi file vào đúng thư mục trong `notes/`.
6. Kiểm tra file tồn tại trước khi tạo/cập nhật.
7. Báo lại đường dẫn file và commit sau khi hoàn thành.
