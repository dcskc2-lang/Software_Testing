Chương 1: Nguyên lý của kiểm thử
Ngày: 05/01/2026 

Nơi thực hiện bài kiểm thử: Cantunsee.space 

Mục tiêu: Kiểm tra khả năng nhận diện chi tiết trong thiết kế giao diện (padding, typography, contrast, v.v.). 

Kết quả: 6280 

<img width="1835" height="1005" alt="Screenshot 2026-01-05 140420" src="https://github.com/user-attachments/assets/5a422003-e481-4a1a-953d-1dd0491981d8" />

Chương 2: Quy trình kiểm thử 

1. Giới thiệu

2. Dự án này bao gồm class `StudentAnalyzer` để xử lý danh sách điểm số học sinh và các unit test tương ứng sử dụng JUnit 5.

3. Chức năng chính

 -`countExcellentStudents`: Đếm số học sinh giỏi (>= 8.0), bỏ qua các điểm không hợp lệ (<0 hoặc >10).

 -`calculateValidAverage`: Tính điểm trung bình của các điểm hợp lệ.

4. Cấu trúc thư mục

 -`unit-test/src/`: Chứa mã nguồn Java.

 -`unit-test/test/`: Chứa mã nguồn kiểm thử.

5. Cách chạy kiểm thử
Yêu cầu: JDK 8+ và thư viện JUnit 5.

-Thực hiện: Chạy trực tiếp trên `VS Code` (IntelliJ/Eclipse) bằng cách click chuột phải vào file StudentAnalyzerTest.java và chọn Run.
