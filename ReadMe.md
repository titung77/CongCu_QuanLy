# Thiết Kế Cơ Sở Dữ Liệu và Giao Diện

## 1. Thiết Kế Cơ Sở Dữ Liệu

### 1.1. Bảng Danh Mục
Lưu trữ thông tin danh mục sản phẩm.

| Name         | Type     | Null | Chú thích        | Khóa       |
|--------------|----------|------|------------------|------------|
| MaDanhMuc    | Int      | No   | Mã danh mục      | Khóa chính |
| TenDanhMuc   | Varchar  | No   | Tên danh mục     |            |
| SlugDanhMuc  | Varchar  | No   | Slug danh mục    |            |
| TrangThai    | Int      | No   | Trạng thái       |            |
| HinhAnh      | Varchar  | No   | Hình ảnh         |            |

---

### 1.2. Bảng Món Ăn
Lưu trữ thông tin danh sách món ăn.

| Name          | Type     | Null | Chú thích         | Khóa       |
|---------------|----------|------|-------------------|------------|
| MaMonAn       | Int      | No   | Mã món ăn         | Khóa chính |
| TenMonAn      | Varchar  | No   | Tên món ăn        |            |
| SlugMonAn     | Varchar  | No   | Slug món ăn       |            |
| Gia           | Float    | No   | Giá món ăn        |            |
| MoTaNgan      | Varchar  | No   | Mô tả ngắn        |            |
| MoTaChiTiet   | Text     | No   | Mô tả chi tiết    |            |
| HinhAnh       | Varchar  | No   | Hình ảnh          |            |
| GiamGia       | Float    | No   | Giảm giá          |            |
| Video         | Varchar  | No   | Video             |            |
| NgayTao       | DateTime | No   | Ngày tạo          |            |
| MaDanhMuc     | Int      | No   | Mã danh mục       |            |
| MaDG          | Int      | No   | Mã giảm giá       |            |

---

### 1.3. Bảng Chi Tiết Hóa Đơn
Lưu trữ thông tin chi tiết hóa đơn.

| Name         | Type     | Null | Chú thích             | Khóa       |
|--------------|----------|------|-----------------------|------------|
| MaCTHD       | Int      | No   | Mã chi tiết hóa đơn   | Khóa chính |
| MaHD         | Int      | No   | Mã hóa đơn            |            |
| MaMonAn      | Int      | No   | Mã món ăn             |            |
| SoLuongBan   | Bigint   | No   | Số lượng bán          |            |
| TongTien     | Float    | No   | Tổng tiền             |            |
| DonGiaBan    | Float    | No   | Đơn giá bán           |            |

---

### 1.4. Bảng Nhân Viên
Lưu trữ thông tin nhân viên.

| Name      | Type     | Null | Chú thích     | Khóa       |
|-----------|----------|------|---------------|------------|
| MaNV      | Int      | No   | Mã nhân viên  | Khóa chính |
| TenNV     | Varchar  | No   | Tên nhân viên |            |
| MatKhau   | Varchar  | No   | Mật khẩu      |            |
| DiaChi    | Varchar  | No   | Địa chỉ       |            |
| DienThoai | Varchar  | No   | Số điện thoại |            |
| ChucVu    | Int      | No   | Chức vụ       |            |

...

---