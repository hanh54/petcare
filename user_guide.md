# Tài liệu hướng dẫn sử dụng hệ thống quản lý phòng thực hành

## 1. Giới thiệu

Hệ thống quản lý tiêm phòng - PetCare là ứng dụng web hỗ trợ quản lý dịch vụ tiêm phòng cho thú cưng, cho phép khách hàng (chủ thú cưng) dễ dàng thêm thú cưng, đặt lịch tiêm, xem lịch sử tiêm; đồng thời giúp quản trị viên quản lý loại vaccine, quản lý lịch hẹn và theo dõi báo cáo thống kê.
Hệ thống giúp tối ưu quy trình làm việc tại cơ sở thú y và mang lại trải nghiệm tiện lợi, chính xác cho khách hàng.
## 2. Chức năng theo vai trò

### 2.1. Sinh viên

#### Tìm kiếm phòng

- Truy cập đường dẫn: `/student/search_rooms`
- Chức năng:
  - Tìm kiếm phòng theo tên, loại phòng, số máy, vị trí
  - Chỉ hiển thị phòng có trạng thái "trống"
  - Xem danh sách phòng phù hợp với tiêu chí tìm kiếm

#### Xem chi tiết phòng

- Truy cập đường dẫn: `/student/room_detail/{id}`
- Chức năng:
  - Xem thông tin chi tiết về phòng: tên, loại, số máy, vị trí, trạng thái
  - Xem danh sách thiết bị trong phòng
  - Xem lịch sử dụng phòng và các lớp học sắp diễn ra

#### Đặt phòng

- Truy cập đường dẫn: `/student/book_room`
- Chức năng:
  - Đề xuất đặt phòng theo khung giờ
  - Điền thông tin đặt phòng: mục đích, thời gian bắt đầu, kết thúc
  - Hệ thống sẽ kiểm tra xung đột và lưu yêu cầu với trạng thái "chờ duyệt"

### 2.2. Giảng viên

#### Tìm kiếm phòng

- Truy cập đường dẫn: `/teacher/search_rooms`
- Chức năng:
  - Tìm kiếm phòng theo tên, loại phòng, số máy, vị trí
  - Xem danh sách phòng phù hợp với tiêu chí tìm kiếm
  - Truy cập nhanh đến chức năng đề xuất phòng trống theo thời gian

#### Xem chi tiết phòng

- Truy cập đường dẫn: `/teacher/room_detail/{id}`
- Chức năng:
  - Xem thông tin chi tiết về phòng: tên, loại, số máy, vị trí, trạng thái
  - Xem danh sách thiết bị trong phòng và tình trạng
  - Xem và lựa chọn khung giờ trống để đặt phòng

#### Đề xuất phòng trống theo thời gian

- Truy cập đường dẫn: `/teacher/suggest_rooms`
- Chức năng:
  - Chọn khung thời gian cần tìm phòng trống
  - Chọn loại phòng và số máy tối thiểu
  - Hệ thống đề xuất danh sách phòng trống phù hợp với yêu cầu
  - Truy cập nhanh đến chức năng đặt phòng

#### Đặt phòng

- Truy cập đường dẫn: `/teacher/book_room`
- Chức năng:
  - Đặt phòng trực tiếp với thông tin lớp học
  - Điền thông tin đặt phòng: lớp, thời gian bắt đầu, kết thúc
  - Hệ thống sẽ kiểm tra xung đột và xác nhận đặt phòng

### 2.3. Quản trị viên

#### Tìm kiếm và quản lý phòng

- Truy cập đường dẫn: `/admin/search_rooms`
- Chức năng:
  - Tìm kiếm phòng theo nhiều tiêu chí: tên, loại, số máy, vị trí, trạng thái
  - Thêm, sửa, xóa phòng
  - Quản lý thông tin chi tiết của phòng
  - Truy cập nhanh đến chức năng quản lý loại phòng

## 3. Hướng dẫn tìm kiếm phòng

### 3.1. Tìm kiếm cơ bản

1. Truy cập vào phần tìm kiếm phòng theo vai trò của bạn:
   - Sinh viên: `/student/search_rooms`
   - Giảng viên: `/teacher/search_rooms`
   - Quản trị viên: `/admin/search_rooms`
2. Điền các tiêu chí tìm kiếm:
   - Tên phòng: nhập từ khóa tìm kiếm
   - Số máy tối thiểu: nhập số người
   - Vị trí: nhập từ khóa vị trí
3. Nhấn nút "Tìm kiếm" để hiển thị kết quả
4. Kết quả sẽ hiển thị dưới dạng bảng với các thông tin cơ bản và nút tác vụ

### 3.2. Tìm kiếm phòng trống theo thời gian (Dành cho giảng viên)

1. Truy cập: `/teacher/suggest_rooms`
2. Chọn thời gian bắt đầu và kết thúc cần tìm phòng trống
3. Chọn thêm loại phòng và số máy tối thiểu (nếu cần)
4. Nhấn "Tìm phòng trống" để xem kết quả
5. Kết quả hiển thị các phòng khả dụng trong khung giờ đã chọn

## 4. Hướng dẫn xem chi tiết phòng

1. Từ trang kết quả tìm kiếm, nhấn vào nút "Chi tiết" của phòng cần xem
2. Thông tin chi tiết phòng sẽ hiển thị:
   - Thông tin cơ bản: tên, loại, số máy, vị trí, trạng thái
   - Danh sách thiết bị trong phòng (nếu có)
   - Lịch sử dụng phòng hoặc lịch sắp tới
   - Đối với giảng viên: hiển thị thêm khung giờ trống để chọn đặt phòng

## 5. Hướng dẫn đặt phòng

### 5.1. Đặt phòng cho sinh viên

1. Từ trang chi tiết phòng, nhấn vào nút "Đề xuất đặt phòng này"
2. Điền thông tin đặt phòng:
   - Chọn thời gian bắt đầu và kết thúc
   - Nhập mục đích sử dụng
3. Nhấn "Đặt phòng" để gửi yêu cầu
4. Yêu cầu sẽ ở trạng thái "chờ duyệt" và cần được quản trị viên phê duyệt

### 5.2. Đặt phòng cho giảng viên

1. Có nhiều cách để đặt phòng:
   - Từ trang chi tiết phòng: nhấn "Đặt phòng này"
   - Từ trang đề xuất phòng trống: chọn phòng phù hợp và nhấn "Đặt phòng"
   - Từ trang tìm kiếm: nhấn "Đặt phòng" với phòng mong muốn
2. Điền thông tin đặt phòng:
   - Chọn thời gian bắt đầu và kết thúc
   - Nhập mã lớp học
3. Hệ thống sẽ kiểm tra xung đột lịch và xác nhận đặt phòng

## 7. Lưu ý quan trọng

- Sinh viên chỉ có thể đề xuất đặt phòng, cần được quản trị viên phê duyệt
- Giảng viên có thể trực tiếp đặt phòng nếu không xung đột lịch
- Không thể đặt phòng trong khoảng thời gian đã có người đặt trước
- Đảm bảo kiểm tra thông tin phòng và thiết bị trước khi đặt
- Báo cáo ngay khi phát hiện thiết bị hỏng hóc
- Tuân thủ quy định sử dụng phòng thực hành
