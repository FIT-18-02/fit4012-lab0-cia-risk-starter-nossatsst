# Lab 01 Answers
## CIA & Risk: Hệ thống lưu điểm

**Họ và tên:** Tạ Công Sơn

**MSSV:** 1871020504

**Lớp/Nhóm:** cntt 18-02    
---

## 1. Assets
Liệt kê ít nhất 2 assets cần bảo vệ.

- Asset 1:Dữ liệu điểm số của sinh viên (điểm từng môn, bảng điểm).
- Asset 2:Tài khoản và thông tin xác thực của giảng viên & sinh viên (username, password).
- Asset 3 (nếu có):Hệ thống quản lý điểm (database và ứng dụng).

---

## 2. Mapping CIA
Ghép từng sự cố với CIA.

- Sự cố A ->(không đăng nhập được)
- Sự cố B ->(điểm bị thay đổi từ 8.0 thành 5.0)
- Sự cố C ->(danh sách điểm bị lộ)

---

## 3. Phân tích sự cố B
- Threat:Sinh viên hoặc hacker cố tình sửa điểm để lợi ích cá nhân (grade tampering).
- Vulnerability:Thiếu phân quyền truy cập (không có RBAC), không ghi log thay đổi, xác thực yếu.
- Mitigation:
  - Sử dụng Role-Based Access Control (chỉ giảng viên sửa điểm).
  - Bật audit logging và hashing cho mỗi thay đổi điểm.
  - Áp dụng Multi-Factor Authentication (MFA) cho giảng viên.

---

## 4. Reflection
Nếu là quản trị viên hệ thống, em sẽ ưu tiên xử lý sự cố B (Integrity) trước vì điểm số bị thay đổi ảnh hưởng trực tiếp đến tính công bằng học tập, dễ gây khiếu nại và mất lòng tin lâu dài. Dữ liệu sai rất khó khôi phục nếu không có log tốt.  

Sự cố A chỉ tạm thời, sự cố C có thể xử lý sau bằng cách thông báo. Việc bảo vệ Integrity là quan trọng nhất để duy trì độ tin cậy của hệ thống. Qua bài lab này, em hiểu rõ hơn về việc áp dụng CIA trong thực tế.

---

## 5. Bonus Flag
`FIT4012{A-?-B-?-C-?}`

Flag của em:

