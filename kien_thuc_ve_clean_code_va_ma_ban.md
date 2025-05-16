# Hướng dẫn nhận diện Mã bẩn & Nguyên tắc Clean Code

## Dấu hiệu nhận diện Mã bẩn (Code Smells)
- **Code trùng lặp (Duplication):** Cùng một đoạn logic xuất hiện ở nhiều nơi. Việc sửa lỗi hoặc cập nhật logic sẽ khó khăn và dễ gây ra sai sót.
- **Đặt tên không có ý nghĩa:** Tên biến, hàm, lớp quá ngắn, không rõ ràng hoặc gây nhầm lẫn (ví dụ: s, t, c, data, handleData). Mã không "tự giải thích" được.
- **Hàm quá dài (Long Method):** Một hàm thực hiện quá nhiều công việc hoặc có quá nhiều dòng code, khó theo dõi logic.
- **Biểu thức hoặc logic khó hiểu:** Các câu điều kiện phức tạp, lồng ghép sâu, hoặc cách viết code không trực quan, khó nắm bắt mục đích.
- **Sử dụng "Magic Numbers" hoặc Hardcoded Values:** Các giá trị cố định xuất hiện trực tiếp trong code mà không được gán cho hằng số có tên rõ ràng. Khó hiểu ý nghĩa của số đó và khó thay đổi khi cần.
- **Comments thừa, vô nghĩa, hoặc lỗi thời:** Comments chỉ diễn tả lại code (cái gì), không giải thích "tại sao" code lại như vậy. Comments sai lệch so với code hiện tại.
- **Code bị commented-out:** Mã nguồn không còn sử dụng nhưng vẫn để lại và bị commented-out.
- **Tham số (Arguments) quá nhiều:** Hàm có quá nhiều tham số đầu vào, khiến việc sử dụng và đọc hiểu hàm khó khăn.
- **Flag Arguments:** Truyền một giá trị boolean vào hàm để quyết định hàm sẽ thực hiện một trong hai luồng logic.
- **Overengineering:** Tạo ra cấu trúc quá phức tạp hoặc giải pháp quá mức cần thiết cho một vấn đề đơn giản.
- **Dead Code:** Các đoạn code không bao giờ được thực thi.
- **Cấu trúc file/thư mục lộn xộn:** Code không được tổ chức logic trong các file và thư mục.

## Nguyên tắc Viết Mã Sạch (Clean Code Principles) - Dành cho người mới bắt đầu

- **Đặt tên rõ ràng:** Dùng tên biến, hàm dễ hiểu, nói rõ chúng dùng để làm gì. Ví dụ: thay vì `x`, `y`, hãy dùng `userName`, `score`.
- **Hàm làm một việc duy nhất:** Mỗi hàm chỉ nên giải quyết một vấn đề nhỏ. Nếu hàm làm quá nhiều thứ, hãy chia nhỏ nó ra.
- **Không lặp lại code (DRY):** Nếu bạn viết đi viết lại cùng một đoạn code, hãy tạo một hàm chung để dùng lại.
- **Code dễ đọc:** Viết code sao cho người khác (và chính bạn sau này) đọc vào có thể hiểu được. Dùng khoảng trắng, thụt đầu dòng hợp lý.
- **Comment khi cần thiết:** Giải thích những đoạn code phức tạp hoặc "tại sao" bạn viết như vậy, chứ không phải "code này làm gì".
- **Tránh "Magic Numbers":** Đừng dùng những con số không rõ ý nghĩa trực tiếp trong code. Hãy đặt tên cho chúng. Ví dụ, thay vì `if (status == 1)`, dùng `const PENDING_STATUS = 1; if (status == PENDING_STATUS)`.

### Clean Code JavaScript Cơ Bản Cho Người Mới

- **Dùng `const` và `let`:**
    - `const`: Cho những giá trị không thay đổi (như số PI, tên một trang web).
    - `let`: Cho những giá trị có thể thay đổi (như điểm số, tuổi).
    - *Tránh dùng `var` để code dễ hiểu hơn.*
- **Dùng Arrow Functions `=>` (khi thích hợp):** Giúp viết hàm ngắn gọn hơn, nhất là với các hàm đơn giản.
- **Sử dụng `'use strict';`:** Đặt ở đầu file JavaScript để trình duyệt báo lỗi sớm nếu có những lỗi phổ biến.
- **Dùng Template Literals (dấu \` \`):** Giúp viết chuỗi (text) có chứa biến dễ dàng hơn. Ví dụ: `` `Chào bạn, ${userName}!` ``.
- **Tránh biến toàn cục (Global Variables):** Hạn chế tạo biến bên ngoài tất cả các hàm, để tránh nhầm lẫn và lỗi khó tìm.
- **Định dạng code nhất quán:** Dùng công cụ như Prettier (hoặc chức năng format của VS Code) để code luôn được sắp xếp gọn gàng, dễ nhìn.
