# Tài liệu hướng dẫn sử dụng hệ thống quản lý tiêm phòng - Petcare

## 1. Giới thiệu

Hệ thống quản lý tiêm phòng - PetCare là ứng dụng web hỗ trợ quản lý dịch vụ tiêm phòng cho thú cưng, cho phép khách hàng (chủ thú cưng) dễ dàng thêm thú cưng, đặt lịch tiêm, xem lịch sử tiêm; đồng thời giúp quản trị viên quản lý loại vaccine, quản lý lịch hẹn và theo dõi báo cáo thống kê.
Hệ thống giúp tối ưu quy trình làm việc tại cơ sở thú y và mang lại trải nghiệm tiện lợi, chính xác cho khách hàng.
## 2. Chức năng theo vai trò

### 2.1. Khách hàng

#### Đăng ký – Đăng nhập

- Truy cập đường dẫn: 
  -  Đăng nhập - `/customer/index.php?controller=XacThucController&action=hienThiDangNhap`
  - Đăng ký - `/customer/index.php?controller=XacThucController&action=hienThiDangKy`
- Chức năng:
  - Tạo tài khoản
  - Đăng nhập, đăng xuất
  - Cập nhật thông tin cá nhân

#### Quản lý thú cưng

- Truy cập đường dẫn: `/customer/index.php?controller=KhachHangController&action=hienThiHoSo`
- Chức năng:
  - Thêm thú cưng: tên, loại, giống, cân nặng, ngày sinh, giới tính, tình trạng sức khỏe, ảnh
  - Xem danh sách thú cưng
  - Chỉnh sửa thông tin thú cưng

#### Xem danh sách dịch vụ tiêm phòng

- Truy cập đường dẫn: `/customer/index.php?controller=DichVuController&action=hienThiDanhSachDichVu`
- Chức năng:
  - Xem thông tin vaccine: mô tả, số lần tiêm, giá, hình ảnh
  - Chọn loại vaccine để đặt lịch

#### Đặt lịch tiêm phòng

- Truy cập đường dẫn: `/customer/index.php?controller=LichTiemController&action=hienThiDatLich`
- Chức năng:
  - Chọn thú cưng cần tiêm
  - Chọn loại vaccine
  - Chọn ngày – giờ hẹn tiêm
  - Nhập ghi chú (nếu có)
  - Gửi yêu cầu đặt lịch (ở trạng thái chờ duyệt)

#### Xem lịch tiêm đã đặt

- Truy cập đường dẫn: `/customer/index.php?controller=LichTiemController&action=hienThiLichTiem`
- Chức năng:
  - Xem danh sách lịch tiêm sắp tới
  - Theo dõi trạng thái: chờ duyệt, đã duyệt, hoàn thành, hủy

#### Xem lịch sử tiêm phòng

- Truy cập đường dẫn: `/customer/index.php?controller=LichTiemController&action=hienThiLichSuTiem`
- Chức năng:
  - Xem các mũi tiêm đã thực hiện
  - Xem liều lượng, bác sĩ thực hiện, ghi chú

### 2.2. Quản trị viên

#### Quản lý loại vaccine

- Truy cập đường dẫn: `/petcare/admin/index.php?controller=AdminController&action=quanLyVacXin`
- Chức năng:
  - Thêm loại vaccine mới
  - Chỉnh sửa thông tin vaccine
  - Xóa vaccine

#### Quản lý lịch hẹn

- Truy cập đường dẫn: `/petcare/admin/index.php?controller=AdminController&action=quanLyDatLich`
- Chức năng:
  - Xem toàn bộ lịch hẹn
  - Cập nhật trạng thái: chờ duyệt, đã duyệt, đang tiêm, hoàn thành, hủy

#### Xem báo cáo – thống kê

- Truy cập đường dẫn: `/petcare/admin/index.php`
- Chức năng:
  - Thống kê số lịch hẹn
  - Thống kê số loại vaccine 

#### Đặt phòng

- Truy cập đường dẫn: `/teacher/book_room`
- Chức năng:
  - Đặt phòng trực tiếp với thông tin lớp học
  - Điền thông tin đặt phòng: lớp, thời gian bắt đầu, kết thúc
  - Hệ thống sẽ kiểm tra xung đột và xác nhận đặt phòng

## 3. Hướng dẫn sử dụng

### 3.1. Đăng ký và đăng nhập

1. Truy cập trang đăng nhập/đăng ký theo đường dẫn tương ứng
2. Nhập thông tin tài khoản
3. Xác nhận và truy cập hệ thống theo vai trò

### 3.2. Hướng dẫn quản lý thú cưng (Khách hàng)

1. Truy cập mục: Hồ sơ cá nhân
2. Chọn Thêm thú cưng
3. Nhập đầy đủ thông tin
4. Lưu lại để hệ thống ghi nhận thú cưng mới

### 3.3. Hướng dẫn đặt lịch tiêm (Khách hàng)

1. Truy cập mục Danh sách dịch vụ
2. Chọn loại vaccine cần tiêm
3. Chọn thú cưng – ngày – giờ
4. Nhấn Đặt lịch
5. Kiểm tra lại lịch tại mục Lịch tiêm

### 3.4. Hướng dẫn xem lịch sử tiêm

1. Truy cập mục Lịch sử tiêm
2. Hệ thống hiển thị:
    - Vaccine đã tiêm
    - Ngày tiêm
    - Bác sĩ thực hiện
    - Liều lượng
    - Ghi chú

### 3.5. Hướng dẫn quản lý vaccine (Quản trị viên)

1. Truy cập mục Quản lý Vaccine
2. Chức năng:
    - Thêm vaccine
    - Sửa vaccine
    - Xóa vaccine
3. Hệ thống tự động cập nhật dữ liệu sau khi lưu

### 3.6. Hướng dẫn quản lý lịch hẹn (Quản trị viên)

1. Mở trang Quản lý lịch hẹn
2. Tại mỗi lịch hẹn: Cập nhật trạng thái thực hiện
3. Hệ thống ghi nhận và hiển thị ngay cho phía khách hàng

## 4. Lưu ý quan trọng

- Khách hàng phải có tài khoản mới đặt lịch được
- Lịch tiêm bị trùng giờ sẽ không được duyệt
- Khách hàng cần theo dõi trạng thái để biết lịch tiêm có được xác nhận hay không
- Các thông tin thú cưng và khách hàng phải được cập nhật đầy đủ để tránh lỗi đặt lịch
- Quản trị viên cần kiểm tra kỹ thông tin vaccine trước khi cập nhật
