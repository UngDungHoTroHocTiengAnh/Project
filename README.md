### Chức năng: Hỗ trợ học tiếng Anh

#### 1. Mô tả tổng quan  
Chức năng Hỗ trợ học tiếng Anh cho phép người dùng quản lý từ vựng bằng cách thêm, sửa, xóa các từ vựng theo chủ đề, học từ vựng thông qua giao diện thân thiện, và làm bài kiểm tra để đánh giá khả năng ghi nhớ. Đây là một phần quan trọng giúp người học cải thiện vốn từ vựng và khả năng sử dụng tiếng Anh trong thực tế.

#### 2. Các yêu cầu chức năng (Functional Requirements)  

**2.1 Thêm từ vựng**  
- Người dùng có thể thêm từ vựng mới với các thông tin sau:  
  - **Từ vựng** (bắt buộc, duy nhất, dạng chuỗi)  
  - **Nghĩa** (bắt buộc, dạng chuỗi)  
  - **Chủ đề** (dropdown chọn chủ đề: Động vật, Đồ ăn, Du lịch, v.v.)  
  - **Ví dụ câu** (tùy chọn)  
  - **Phát âm** (tùy chọn, file âm thanh hoặc ký tự phiên âm)  
- Hệ thống kiểm tra các trường bắt buộc và cảnh báo nếu dữ liệu không hợp lệ.  

**2.2 Cập nhật từ vựng**  
- Người dùng có thể chỉnh sửa thông tin từ vựng, bao gồm: nghĩa, chủ đề, ví dụ câu, phát âm.  
- Hệ thống ghi nhận lịch sử cập nhật (ai cập nhật, thời gian cập nhật).  

**2.3 Xóa từ vựng**  
- Cho phép xóa từ vựng khỏi danh sách.  
- Hiển thị cảnh báo trước khi xóa từ vựng.  

**2.4 Học từ vựng theo chủ đề**  
- Người dùng có thể chọn một chủ đề và hệ thống hiển thị danh sách từ vựng thuộc chủ đề đó.  
- Hỗ trợ chế độ học từ vựng:  
  - Hiển thị từ và nghĩa.  
  - Nghe phát âm (nếu có).  
  - Xem ví dụ sử dụng từ.  

**2.5 Làm bài kiểm tra**  
- Hệ thống cung cấp bài kiểm tra theo hai hình thức:  
  - **Trắc nghiệm**: Chọn nghĩa đúng cho từ vựng.  
  - **Điền từ**: Điền từ vựng vào câu cho sẵn.  
- Kết quả được chấm tự động và hiển thị ngay sau khi hoàn thành bài kiểm tra.  

#### 3. Các yêu cầu phi chức năng (Non-functional Requirements)  
- Giao diện thân thiện, hỗ trợ tiếng Việt và tiếng Anh.  
- Thời gian phản hồi khi hiển thị từ vựng hoặc kiểm tra không quá 1 giây.  
- Ứng dụng hỗ trợ cả máy tính và thiết bị di động.  
- Dữ liệu từ vựng được bảo mật, chỉ người dùng đăng nhập mới có quyền truy cập và chỉnh sửa.  

#### 4. Quy trình hoạt động (Workflow)  

**4.1 Quy trình thêm từ vựng**  
1. Người dùng nhấn nút "Thêm từ vựng" trên giao diện.  
2. Điền các thông tin yêu cầu vào biểu mẫu.  
3. Nhấn nút "Lưu".  
4. Hệ thống kiểm tra dữ liệu:  
   - Nếu hợp lệ: Lưu vào cơ sở dữ liệu và hiển thị thông báo thành công.  
   - Nếu không hợp lệ: Hiển thị lỗi cụ thể.  

**4.2 Quy trình học từ vựng**  
1. Người dùng chọn chủ đề từ vựng.  
2. Hệ thống hiển thị danh sách từ vựng theo chủ đề.  
3. Người dùng có thể xem nghĩa, ví dụ, và nghe phát âm từng từ.  

**4.3 Quy trình làm bài kiểm tra**  
1. Người dùng chọn bài kiểm tra theo chủ đề.  
2. Hệ thống hiển thị câu hỏi từng bước.  
3. Sau khi hoàn thành, hệ thống chấm điểm và hiển thị kết quả.  

#### 5. Thiết kế giao diện  
- **Danh sách từ vựng**:  
  - Cột: Từ vựng, Nghĩa, Chủ đề, Ví dụ, Phát âm.  
  - Nút "Chỉnh sửa", "Xóa" hiển thị trong từng dòng.  
  (hình minh họa)  

- **Biểu mẫu thêm/chỉnh sửa từ vựng**:  
  - Các trường nhập liệu kèm nhãn rõ ràng.  
  - Nút "Lưu", "Hủy".  
  (hình minh họa)  

- **Giao diện học từ vựng**:  
  - Hiển thị từ vựng kèm nghĩa và ví dụ.  
  - Nút "Nghe phát âm".  
  (hình minh họa)  

#### 6. Yêu cầu tích hợp  
- Tích hợp với hệ thống phát âm trực tuyến để lấy dữ liệu phát âm.  
- Hỗ trợ đồng bộ dữ liệu từ vựng với các ứng dụng học tiếng Anh khác qua API.  

#### 7. Kiểm thử (Test Cases)  
- Thêm từ vựng mới với đầy đủ thông tin hợp lệ.  
- Thêm từ vựng thiếu thông tin bắt buộc (kiểm tra cảnh báo lỗi).  
- Sửa thông tin từ vựng.  
- Xóa từ vựng khỏi danh sách.  
- Làm bài kiểm tra với cả hai hình thức và hiển thị kết quả chính xác.
