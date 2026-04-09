# FIT4012 - Report 1 Page
## Lab 01 - CIA & Risk: Hệ thống lưu điểm

### 1. Mục tiêu bài lab
- Nhận diện tài sản cần bảo vệ trong một hệ thống thông tin đơn giản.
- Phân biệt ba mục tiêu bảo mật cốt lõi: Confidentiality (Bảo mật), Integrity (Tính toàn vẹn), Availability (Tính khả dụng).
- Xác định threat, vulnerability và đề xuất mitigation phù hợp.
- Làm quen với workflow GitHub: fork/clone/edit/commit/push.

### 2. Cách làm
- Phân tích bối cảnh hệ thống lưu điểm cho giảng viên nhập điểm và sinh viên xem điểm.
- Xác định các tài sản quan trọng cần bảo vệ.
- Ghép nối từng sự cố (A, B, C) với thành phần tương ứng trong bộ ba CIA.
- Phân tích sâu sự cố B theo mô hình Threat – Vulnerability – Mitigation.
- Hoàn thiện câu trả lời trong `answers/lab1_answers.md` và báo cáo này, sau đó commit & push lên GitHub.

### 3. Kết quả chính

**Assets:**
- Dữ liệu điểm số của sinh viên (grades database) – thông tin nhạy cảm, ảnh hưởng trực tiếp đến kết quả học tập và học bạ.
- Tài khoản và thông tin xác thực của giảng viên & sinh viên (user accounts, passwords, sessions) – đảm bảo chỉ người có quyền mới được truy cập và chỉnh sửa.

**CIA mapping:**
- Sự cố A (Không đăng nhập được vào tối trước ngày công bố điểm) → **A - Availability (Tính khả dụng)**
- Sự cố B (Điểm của sinh viên bị thay đổi từ 8.0 thành 5.0) → **I - Integrity (Tính toàn vẹn)**
- Sự cố C (Danh sách điểm bị lộ ra nhóm chat ngoài lớp) → **C - Confidentiality (Bảo mật)**

**Phân tích sự cố B:**
- **Threat**: Người dùng trái phép (sinh viên hoặc hacker) cố tình thay đổi điểm số để trục lợi cá nhân hoặc gây hại.
- **Vulnerability**: Cơ chế phân quyền yếu, thiếu kiểm soát truy cập chặt chẽ (không áp dụng RBAC), cho phép người dùng không phải giảng viên có thể chỉnh sửa dữ liệu điểm.
- **Mitigation**: Triển khai Role-Based Access Control (RBAC), chỉ cho phép giảng viên mới được chỉnh sửa điểm; bật audit logging để ghi lại mọi thay đổi (ai, khi nào, thay đổi từ giá trị nào sang giá trị nào); sử dụng backup và checksum để phát hiện và khôi phục dữ liệu bị sửa.

### 4. Kết luận ngắn
Qua bài lab này, em hiểu rõ hơn tầm quan trọng của bộ ba CIA trong việc bảo vệ hệ thống thông tin. Em học được cách nhìn nhận vấn đề an toàn bảo mật một cách có hệ thống: từ việc xác định tài sản → phân tích rủi ro theo CIA → đề xuất giải pháp giảm thiểu.

Phần khó nhất là phân biệt rõ ràng giữa các sự cố và ánh xạ chính xác với CIA, vì đôi khi một sự cố có thể ảnh hưởng đến nhiều thành phần. Em nhận ra rằng khi phân tích một sự cố an toàn thông tin, cần chú ý đến **tác động thực tế** và **ưu tiên xử lý** dựa trên mức độ nghiêm trọng (Integrity thường rất quan trọng trong hệ thống điểm số vì ảnh hưởng trực tiếp đến công bằng).

Bài lab cũng giúp em làm quen với quy trình làm việc chuyên nghiệp qua GitHub, đặc biệt là việc commit có ý nghĩa và giữ lịch sử làm việc rõ ràng. Em sẽ áp dụng tư duy CIA này vào các bài lab và dự án sau này.