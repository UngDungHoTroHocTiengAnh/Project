# Project

### Chức năng: Ứng dụng hỗ trợ học tiếng Anh  

---

#### 1. Mô tả tổng quan  
Ứng dụng cung cấp các công cụ đa dạng để hỗ trợ người dùng học tiếng Anh. Ngoài các chức năng học kỹ năng và làm bài kiểm tra, ứng dụng còn có tính năng học từ vựng theo chủ đề, cho phép thêm mới, chỉnh sửa và xóa từ vựng cá nhân.  

---

#### 2. Các yêu cầu chức năng (Functional Requirements)  

**2.1 Quản lý bài học**  
- Người dùng có thể xem danh sách các bài học theo các kỹ năng.  
- Hệ thống cho phép tải xuống bài học hoặc đánh dấu bài học đã hoàn thành.  
**2.2 Làm bài kiểm tra**  
- Các dạng bài kiểm tra đa dạng: trắc nghiệm, điền từ, viết luận.  
- Kết quả bài kiểm tra được hệ thống chấm điểm và lưu lại để người dùng xem lại tiến trình học tập.  
**2.3 Tra từ điển**  
- Người dùng có thể tra cứu nghĩa từ vựng, cách phát âm và ví dụ minh họa.  
- Hỗ trợ phát âm từ bằng giọng nói chuẩn Anh-Anh hoặc Anh-Mỹ.  
**2.4 Học từ vựng theo chủ đề**  
- Người dùng có thể chọn học từ vựng theo các chủ đề như: Gia đình, Công việc, Du lịch, v.v.  
- Hệ thống cung cấp danh sách các từ vựng liên quan, kèm phát âm, nghĩa và ví dụ.  
- Có chế độ ôn tập với flashcard và bài kiểm tra trắc nghiệm về từ vựng đã học.  

**2.5 Thêm, sửa, xóa từ vựng**  
- **Thêm từ vựng**:  
  - Người dùng có thể thêm từ mới vào danh sách từ vựng cá nhân hoặc gắn vào một chủ đề.  
  - Các thông tin cần nhập:  
    - Từ vựng (bắt buộc)  
    - Nghĩa (bắt buộc)  
    - Phát âm (tùy chọn, có thể nhập tay hoặc chọn từ gợi ý).  
    - Ví dụ sử dụng (tùy chọn).  

- **Sửa từ vựng**:  
  - Người dùng có thể cập nhật thông tin của từ vựng (nghĩa, phát âm, ví dụ) nhưng không thay đổi từ gốc.  

- **Xóa từ vựng**:  
  - Cho phép xóa từ khỏi danh sách cá nhân. Hiển thị xác nhận trước khi thực hiện.  


#### 3. Các yêu cầu phi chức năng (Non-functional Requirements)  
(Chi tiết như trên, bổ sung thêm:)  
- Từ vựng mới được đồng bộ với tài khoản người dùng để truy cập trên nhiều thiết bị.  
- Dữ liệu từ vựng được mã hóa để đảm bảo an toàn thông tin cá nhân.  

---

#### 4. Quy trình hoạt động (Workflow)  

**4.1 Quy trình thêm từ vựng**  
1. Người dùng chọn chức năng "Thêm từ vựng".  
2. Điền thông tin từ vựng (từ, nghĩa, ví dụ).  
3. Chọn hoặc tạo mới một chủ đề liên quan.  
4. Nhấn "Lưu".  

**4.2 Quy trình học từ vựng theo chủ đề**  
1. Người dùng chọn một chủ đề từ danh sách.  
2. Hệ thống hiển thị danh sách từ vựng kèm phát âm, nghĩa và ví dụ.  
3. Người dùng có thể ôn tập qua flashcard hoặc bài kiểm tra trắc nghiệm.  

**4.3 Quy trình sửa từ vựng**  
1. Người dùng chọn từ cần chỉnh sửa trong danh sách từ vựng.  
2. Cập nhật các thông tin mong muốn.  
3. Nhấn "Lưu".  

**4.4 Quy trình xóa từ vựng**  
1. Người dùng chọn từ cần xóa.  
2. Hệ thống hiển thị thông báo xác nhận.  
3. Nếu người dùng xác nhận, từ vựng sẽ bị xóa khỏi danh sách.  

---

#### 5. Thiết kế giao diện  

- **Danh sách từ vựng theo chủ đề**:  
  - Hiển thị các cột: Từ vựng, Nghĩa, Chủ đề, Ví dụ.  
  - Nút "Chỉnh sửa", "Xóa" trên mỗi dòng.  

- **Biểu mẫu thêm/chỉnh sửa từ vựng**:  
  - Các trường nhập liệu kèm nhãn rõ ràng: Từ, Nghĩa, Chủ đề, Phát âm, Ví dụ.  
  - Nút "Lưu", "Hủy".  

- **Flashcard từ vựng**:  
  - Hiển thị từ vựng ở mặt trước, nghĩa và ví dụ ở mặt sau.  
  - Nút "Tiếp theo", "Quay lại".  

---

#### 6. Yêu cầu tích hợp  

- **Tích hợp với module Tra từ điển** để tự động điền nghĩa và phát âm khi thêm từ vựng mới.  
- **Tích hợp API học tập trực tuyến** để tải thêm danh sách từ vựng chủ đề nâng cao.  

---

#### 7. Kiểm thử (Test Cases)  

- Thêm từ vựng với đầy đủ thông tin.  
- Thêm từ vựng thiếu thông tin bắt buộc, kiểm tra hiển thị lỗi.  
- Sửa thông tin từ vựng, lưu thành công.  
- Xóa từ vựng khỏi danh sách và kiểm tra dữ liệu được cập nhật.  
- Học từ vựng theo chủ đề và làm bài kiểm tra trắc nghiệm.
