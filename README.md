# Tài liệu dành cho học viên

## Chuyên đề “Clean Code & Fix Bug”

**Ngày tạo:** 17/05/2025  
**Version:** 2.0

### Mục đích
- Tạo sân chơi học hỏi, bổ ích cho học viên thông qua việc thực hành clean code và sửa lỗi (fix bug).

### Mục tiêu
- Nâng cao kỹ năng nhận diện mã bẩn (code smell) và lỗi trong thực tế.
- Phát triển khả năng áp dụng các nguyên tắc clean code để cải thiện chất lượng code.
- Rèn luyện kỹ năng debug và sửa lỗi hiệu quả.
- Tăng cường kỹ năng làm việc nhóm và quản lý thời gian.
- Thực hành sử dụng Git/GitHub theo quy trình chuyên nghiệp.

### Format Cuộc thi
- Mỗi team nhận 10 đoạn code xấu hoặc chứa lỗi. Trong 40 phút, thực hiện:
  - **Refactor code**: Làm sạch và cải thiện chất lượng code.
  - **Fix bug**: Sửa lỗi để code chạy đúng và ổn định.
- Có thể chia task trong nhóm, miễn là nộp bản cuối đúng deadline.

#### Thời gian phân bổ:
- **5 phút:** Setup (Ổn định chỗ ngồi, nhận đề, phổ biến quy chế).
- **40 phút:** Làm bài (refactoring code và fix bug).
- **5 phút:** Nộp bài qua GitHub.

#### Bộ đề mẫu:
- 10 câu hỏi, bao gồm 5 câu nhận diện và sửa lỗi cơ bản (8 điểm/câu) và 5 câu thực hành viết code sạch (12 điểm/câu).
- Xem chi tiết đề bài tại: [Đề bài Clean Code & Fix Bug](./de_bai_clean_code_fix_bug.md)

### Tài liệu chi tiết cuộc thi
Để hiểu rõ hơn về cuộc thi, vui lòng tham khảo các tài liệu sau:
- **Kiến thức nền tảng:** [Hướng dẫn nhận diện Mã bẩn & Nguyên tắc Clean Code](./kien_thuc_ve_clean_code_va_ma_ban.md)

### Quy chế
#### Quy định chung
- Mỗi nhóm có 3-4 thành viên (tuỳ số lượng học viên).
- Tuân thủ nghiêm ngặt thời gian làm bài và nộp bài.
- Không trao đổi với các nhóm khác trong quá trình làm bài.
- Có thể sử dụng tài nguyên internet để tham khảo nhưng không copy hoàn toàn.

#### Quy định nộp bài
- **Thời gian:** Các bạn có 5 phút để hoàn tất việc nộp bài lên GitHub.
- **Yêu cầu quan trọng:**
  1. **Commit ý nghĩa:** Mỗi lần lưu (commit) code lên GitHub, hãy đặt tên commit rõ ràng, ví dụ:
     - `fix: Sửa lỗi hàm tính tổng`
     - `refactor: Tối ưu vòng lặp`
     - `feat: Hoàn thành câu 1`
     - *Tránh các commit vô nghĩa như "update", "fix bug", "done".*
  2. **Đúng Repository:** Đảm bảo bạn nộp bài vào đúng repository của nhóm mình theo format `CleanCodeFixBug_NhomX`.

### Agenda
| Mốc thời gian | Hoạt động                                                                            | Vai trò       |
| ------------- | ------------------------------------------------------------------------------------ | ------------- |
| **5 phút**    | - BTC phân chia nhóm (3-5 nhóm tùy số lượng học viên).                               | BTC/ Học viên |
|               | - BTC giới thiệu quy chế và cách thức chấm điểm.                                     |               |
|               | - BTC phát đề bài (dạng text để import vào IDE, ngôn ngữ JavaScript).                |               |
|               | - Học viên quét mã QR để nhận liên kết đến repository cuộc thi.                      | Học viên      |
|               | [https://bit.ly/CleanCodeFixBug-Challenge](https://bit.ly/CleanCodeFixBug-Challenge) |               |
|               | ![Mã QR](./images/QR_CleanCodeFixBug-Challenge.png)                                  |               |
| **40 phút**   | - Học viên đọc đề và làm bài.                                                        | Học viên      |
|               | - Học viên xác định các mã xấu/lỗi cần xử lý.                                        |               |
|               | - Học viên refactor code và fix bug trực tiếp trên IDE.                              |               |
|               | - Yêu cầu: Comment lại mã gốc trước khi refactor/fix bug.                            |               |
| **5 phút**    | - Học viên nộp bài qua GitHub theo hướng dẫn.                                        | Học viên      |
