# Lab 01 Answers
## CIA & Risk: Hệ thống lưu điểm

**Họ và tên:** Tạ Công Sơn

**MSSV:** 1871020504

**Lớp/Nhóm:** CNTT 18-02

---

## 1. Assets
Liệt kê ít nhất 2 assets cần bảo vệ.

- Asset 1: Cơ sở dữ liệu điểm số của sinh viên (Grade Database).
- Asset 2: Tài khoản xác thực của giảng viên và quản trị viên (Admin Credentials).
- Asset 3 (nếu có): Hệ thống máy chủ lưu trữ ứng dụng quản lý điểm.

---

## 2. Mapping CIA
Ghép từng sự cố với CIA.

- Sự cố A -> Availability (Tính khả dụng)
- Sự cố B -> Integrity (Tính toàn vẹn)
- Sự cố C -> Confidentiality (Tính bảo mật)

---

## 3. Phân tích sự cố B
- Threat: Kẻ tấn công (sinh viên hoặc tin tặc) cố tình thay đổi dữ liệu điểm số trái phép.
- Vulnerability: Hệ thống thiếu cơ chế kiểm tra quyền truy cập chặt chẽ (Broken Access Control) và không có nhật ký thay đổi dữ liệu (Audit Logs).
- Mitigation: Triển khai kiểm soát truy cập dựa trên vai trò (RBAC) và ghi lại toàn bộ lịch sử thay đổi (Audit Logging) trên cơ sở dữ liệu.

---

## 4. Reflection
Nếu là quản trị viên hệ thống, em sẽ ưu tiên xử lý sự cố B (Integrity) trước tiên. Trong một hệ thống giáo dục, tính chính xác và tin cậy của điểm số là giá trị cốt lõi nhất. Nếu dữ liệu điểm bị sai lệch mà không thể kiểm soát, hệ thống sẽ mất hoàn toàn uy tín đối với sinh viên và nhà trường. Sự cố A và C tuy quan trọng nhưng không gây ra hậu quả pháp lý và niềm tin nghiêm trọng bằng việc thay đổi kết quả học tập. Qua đó, bảo vệ tính toàn vẹn chính là bảo vệ công bằng trong giáo dục.

---

## 5. Bonus Flag
`FIT4012{A-A-B-I-C-C}`

Flag của em: FIT4012{A-A-B-I-C-C}