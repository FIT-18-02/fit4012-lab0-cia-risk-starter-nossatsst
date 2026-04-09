## Lab 01 - CIA & Risk: Hệ thống lưu điểm

### 1. Mục tiêu bài lab
- Nhận diện tài sản cần bảo vệ trong một hệ thống thông tin đơn giản.
- Phân biệt Confidentiality, Integrity, Availability (CIA).
- Xác định threat, vulnerability, mitigation.
- Thực hành workflow GitHub chuyên nghiệp: fork, clone, commit, push.

### 2. Cách làm
- Phân tích bối cảnh hệ thống lưu điểm để xác định các Assets quan trọng.
- Phân loại 3 sự cố A, B, C dựa trên định nghĩa về tính Bảo mật, Toàn vẹn và Khả dụng.
- Nghiên cứu sâu sự cố B để tìm ra mối đe dọa và lỗ hổng kỹ thuật.
- Sử dụng Git để quản lý phiên bản và nộp bài đúng quy trình.

### 3. Kết quả chính
**Assets:**
- Tài sản 1: Cơ sở dữ liệu điểm số của sinh viên.
- Tài sản 2: Thông tin định danh và tài khoản của Giảng viên.

**CIA mapping:**
- incident_a: Availability
- incident_b: Integrity
- incident_c: Confidentiality

**Phân tích sự cố B:**
- threat: Kẻ tấn công thực hiện thay đổi dữ liệu trái phép (Grade Tampering).
- vulnerability: Hệ thống thiếu kiểm tra quyền hạn (Authorization) và thiếu Audit Logs.
- mitigation: Triển khai kiểm soát truy cập RBAC và cơ chế ghi nhật ký thay đổi.

### 4. Kết luận ngắn
Qua bài lab này, em đã học được cách áp dụng mô hình CIA để đánh giá rủi ro cho một hệ thống thực tế. Phần khó nhất là việc xác định chính xác lỗ hổng (vulnerability) đằng sau một sự cố. Điều cần chú ý nhất khi phân tích an toàn thông tin là phải nhìn nhận sự cố dưới nhiều góc độ để đưa ra biện pháp giảm thiểu (mitigation) phù hợp. Bài tập cũng giúp em thành thạo hơn các lệnh Git cơ bản trên chiếc Acer Nitro 5 của mình.