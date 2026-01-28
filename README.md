# Chương 1: Nguyên lý của kiểm thử
Ngày: 05/01/2026 

Nơi thực hiện bài kiểm thử: [Can't Unsee](https://cantunsee.space)

Mục tiêu: Kiểm tra khả năng nhận diện chi tiết trong thiết kế giao diện (padding, typography, contrast, v.v.). 

Kết quả: 6280 

<img width="1835" height="1005" alt="Screenshot 2026-01-05 140420" src="https://github.com/user-attachments/assets/5a422003-e481-4a1a-953d-1dd0491981d8" />

# Chương 2: Quy trình kiểm thử 

1. Giới thiệu

- Dự án này bao gồm class `StudentAnalyzer` để xử lý danh sách điểm số học sinh và các unit test tương ứng sử dụng JUnit 5.

2. Chức năng chính

 - `countExcellentStudents`: Đếm số học sinh giỏi (>= 8.0), bỏ qua các điểm không hợp lệ (<0 hoặc >10).

 - `calculateValidAverage`: Tính điểm trung bình của các điểm hợp lệ.

3. Cấu trúc thư mục

 - `unit-test/src/`: Chứa mã nguồn Java.

 - `unit-test/test/`: Chứa mã nguồn kiểm thử.

4. Cách chạy kiểm thử
Yêu cầu: JDK 8+ và thư viện JUnit 5.

- Thực hiện: Chạy trực tiếp trên `VS Code` (IntelliJ/Eclipse) bằng cách click chuột phải vào file StudentAnalyzerTest.java và chọn Run.

# Chương 3: Kiểm thử tĩnh

1. Giới thiệu
   
Sử dụng Cypress để thực hiện kiểm thử tự động End-to-End (E2E) cho trang web mẫu Swag Labs (SauceDemo). Bài tập tập trung vào việc mô phỏng hành vi người dùng thực tế từ đăng nhập đến thanh toán.

3. Các kịch bản kiểm thử (Test Scenarios)
   
Dự án bao gồm 2 file kiểm thử chính nằm trong thư mục cypress/e2e/:

`login_spec.cy.js` (Kiểm thử Đăng nhập):

- Đăng nhập thành công với tài khoản hợp lệ (standard_user).
  
- Hiển thị thông báo lỗi chính xác khi nhập sai thông tin (invalid_user).
  
`cart_spec.cy.js` (Kiểm thử Giỏ hàng & Thanh toán):

- Thêm sản phẩm vào giỏ hàng và kiểm tra số lượng (Badge count).
  
- Sắp xếp danh sách sản phẩm theo giá (Thấp đến Cao).
  
- Xóa sản phẩm khỏi giỏ hàng.
  
- Thực hiện quy trình thanh toán đầy đủ (Checkout Flow): Giỏ hàng -> Điền thông tin -> Xác nhận -> Hoàn tất.

4. Kết quả kiểm thử (Evidence)

- Kết quả kịch bản Đăng nhập:

<img width="1919" height="1013" alt="image" src="https://github.com/user-attachments/assets/7d896a39-f9cf-4c7b-a441-c0f65f23cbd4" />

<img width="1918" height="1021" alt="image" src="https://github.com/user-attachments/assets/da0c8c78-1146-4cd8-9457-e4492bd8cedd" />


- Kết quả kịch bản Giỏ hàng & Thanh toán:

<img width="1919" height="1024" alt="Screenshot 2026-01-21 163816" src="https://github.com/user-attachments/assets/c3d0ed51-85e6-41b0-99ec-0c91c799d821" />

<img width="1919" height="1019" alt="Screenshot 2026-01-21 163826" src="https://github.com/user-attachments/assets/1fcaa5f3-9fd5-4326-8983-a250077c46f3" />

<img width="1918" height="1018" alt="Screenshot 2026-01-21 163833" src="https://github.com/user-attachments/assets/bebec699-553b-4c4b-aaf6-56ff46c453e8" />

## Chương 4:

## 1. Giới thiệu
- **Mục tiêu**: Đánh giá hiệu năng của website Wikipedia dưới các mức tải khác nhau.
- **Website kiểm thử**: [https://www.wikipedia.org](https://www.wikipedia.org)
- **Công cụ sử dụng**: Apache JMeter 5.6.3
- **Ngày thực hiện**: 24/1/2026

## 2. Kịch bản kiểm thử (Test Scenarios)

Kịch bản 1: Cơ bản (Basic Load)
- **Cấu hình**: 10 users, 5 loops.
- **Mục đích**: Kiểm tra phản hồi cơ bản của server với lượng truy cập thấp.
- **Hành vi**: Truy cập trang chủ.

Kịch bản 2: Tải nặng (Heavy Load)
- **Cấu hình**: 50 users, Ramp-up 30s, chạy trong 2 phút.
- **Mục đích**: Kiểm tra khả năng chịu tải của server khi lượng user tăng dần.
- **Hành vi**: Truy cập trang chủ và trang ngẫu nhiên (Wiki Random).

Kịch bản 3: Tùy chỉnh (Custom Load)
- **Cấu hình**: 20 users, chạy trong 60s.
- **Mục đích**: Mô phỏng hành vi người dùng đọc các bài viết cụ thể.
- **Hành vi**: Truy cập Portal:Arts và Portal:History.

## 3. Kết quả Kiểm thử

Kịch bản 1 (Basic)

<img width="1521" height="788" alt="image" src="https://github.com/user-attachments/assets/737a3163-243c-410c-9163-37f3d153f421" />

- **Error %**: 0% (Sau khi thêm User-Agent)

Kịch bản 2 (Heavy)

<img width="1919" height="1026" alt="image" src="https://github.com/user-attachments/assets/f1efc5bb-379c-41fb-94cc-614a76064218" />

- **Error %**: 0%

Kịch bản 3 (Custom)

<img width="1919" height="1029" alt="image" src="https://github.com/user-attachments/assets/81e78b79-c8fc-4a7c-9501-4d13d3c2987e" />

- **Error %**: 2%

4. Phân tích & Nhận xét
- **Tỉ lệ lỗi**: Ban đầu gặp lỗi 403 Forbidden do Wikipedia chặn bot. Đã khắc phục bằng cách thêm "User-Agent" giả lập trình duyệt Chrome.
- **Khả năng chịu tải**: Server phản hồi tốt trong bài test nhanh.

5. Kết luận
- Trang web hoạt động **Tốt** sau khi cấu hình đúng Header.
- Kịch bản kiểm thử đã sẵn sàng để chạy tải nặng thực tế.
