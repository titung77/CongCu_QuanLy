# Thiết kế cơ sở dữ liệu 
## Bảng dữ liệu.
* Bảng danh mục.
    Dùng để lưu trữ danh mục sản phẩm.
|Name|	Type|	Null|	Chú thích|	Khóa|
----------------------------------------------
|MaDanhMuc|	Int|	No|	Mã danh mục	Khóa chính|
----------------------------------------------
|TenDanhMuc|	Varchar|	No|	Tên danh mục	|
----------------------------------------------
|SlugDanhMuc|	Varchar|	No|	Slug Danh Mục|
----------------------------------------------	
|TrangThai|	Int|	No|	Trạng Thái	|
----------------------------------------------
|HinhAnh|	VarChar|	No|	Hình Ảnh|	

Bảng món ăn.
Dùng để lưu trữ danh sách món ăn.
Name	Type	Null	Chú thích	Khóa
MaMonAn	Int	No	Mã sản phẩm	Khóa chính
TenMonAn	Varchar	No	Mã sản phẩm	
SlugMonAn	Varchar	No	Mã danh mục	
Gia	Float	No	Giá sản phẩm	
MoTaNgan	Varchar	No	Mô Tả Ngắn	
MoTaChiTiet	Text	No	Mô Tả Chi Tiết	
HinhAnh	Varchar	No	Hình Ảnh	
GiamGia	Float	No	Giảm Giá	
Video	Varchar	No	Video	
NgayTao	DateTime	No	Ngày Tạo	
MaDanhMuc	Int	No	Mã Danh Mục	
MaDG	Int	No	Mã Giảm Giá	

Bảng chi tiết hóa đơn.
Dùng để lưu trữ thông tin chi tiết hóa đơn.
Name	Type	Null	Chú thích	Khóa
MaCTHD	Int	No	Mã chú thích hóa đơn	Khóa chính
MaHD	Int	No	Mã Hóa Đơn	
MaMonAn	Int	No	Mã Món Ăn	
SoLuongBan	Bigint	No	Số lượng bán	
TongTien	Float	No	Tổng tiền	
DonGiaBan	Float	No	Đơn gía bán	

 
Bảng Nhân Viên.
Dùng để lưu trữ thông tin nhân viên.
Name	Type	Null	Chú thích	Khóa
MaNV	Int	No	Mã Nhân Viên	Khóa chính
TenNV	Varchar	No	Tên nhân viên	
MatKhau	Varchar	No	Mật khẩu	
DiaChi	Varchar	No	Địa chỉ	
DienThoai	Varchar	No	Số điện thoại	
ChucVu	Int	No	Chức vụ	

Bảng Shipper.
Dùng để lưu trữ thông tin shipper.
Name	Type	Null	Chú thích	Khóa
MaShip	Int	No	Mã Shipper	Khóa chính
TenDN	Varchar	No	Tên Đơn Hàng	
DienThoai	Varchar	No	Số Điện Thoại	
MatKhau	Varchar	No	Mật khẩu	
Email	Varchar	No	Email	

Bảng hóa đơn bán hàng.
Dùng để lưu trữ hóa đơn bán hàng.
Name	Type	Null	Chú thích	Khóa
MaHD	int	No	Mã hóa đơn	Khóa chính
MaKH	Int	No	Mã khách hàng	
NgayGiao	DateTime	No	Ngày Giao	
NgayDat	DateTime	No	Ngày đặt	
HoTen	Varchar	No	Họ Tên	
DiaChi	Varchar	No	Địa chỉ	
CachThanhToan	Varchar	No	Cách thanh toán	
LoaiVanChuyen	Int	No	Loại vận chuyển	
PhiVanChuyen	Float	No	Phí vận chuyển	
GhiChu	Varchar	No	Ghi chú	
TrangThaiDonHang	Int	No	Trạng Thái Đơn Hàng	
MaShip	Int	No	Mã Ship	
MaNV	Int	No	Mã Nhân Viên	
MaVT	Int	No	Mã Vị Trí	

Bảng đánh giá.
Dùng để lưu trữ thông tin đánh giá.
Name	Type	Null	Chú thích	Khóa
MaDG	int	No	Mã đánh giá	Khóa chính
MaKH	Bigint	No	Mã khách hàng	
NoiDung	Bigint	No	Nội dung	
TrangThai	Bigint	No	Trạng thái	
MaMonAn	Int	No	Mã món ăn	
MaHD	Int	No	Mã hoá đơn	

Bảng chi tiết chức năng.
Dùng để lưu trữ thông tin chi tiết chức năng.
Name	Type	Null	Chú thích	Khóa
MaCT	Int	No	Mã Chi Tiet	Khóa chính
MaCN	Int	No	Mã chức năng	
MaNV	Int	No	Mã nhân viên	
GiaTriChucNang	Varchar	No	Giá trị chức năng	

Bảng khách hàng.
Dùng để lưu trữ thông tin khách hàng.
Name	Type	Null	Chú thích	Khóa
MaKH	int	No	Mã khách hàng	Khóa chính
TenTK	Varchar	No	Tên tài khoản	
MatKhau	Varchar	No	Mật khẩu	
DiaChi	Varchar	No	Địa chỉ	
Email	Varchar	No	Email	
NgaySinh	DateTime	No	Ngày sinh	
NgayTao	DateTime	No	Ngày tạo	
DienThoai	VarChar	No	Điện thoại	
HinhAnh	Varchar	No	Hình ảnh	
TrangThai	Int	No	Trạng thái	
MaVT	Int	No	Mã vị trí	

Bảng vị trí..
Dùng để lưu trữ vị trí.
Name	Type	Null	Chú thích	Khóa
MaVT	Int	No	Mã vị trí	Khóa chính
TenVT	Varchar	No	Tên vị trí	
Mota	Text	No	Mô tả	
ToaDo	Varchar	No	Tọa độ	

 
Bảng chức năng.
Dùng để lữu trữ thông tin chức năng.
Name	Type	Null	Chú thích	Khóa
MaCN	int	No	Mã chức năng	Khóa chính
TenChucNang	Varchar	No	Tên chức năng	
MoTa	Text	No	Mô tả	


Sơ đồ thực thể liên kết
 



Thiết kế giao diện 
Giao diện đăng nhập.
 
 
Giao diện trang chủ
 

Giao diện giỏ hàng.
 
Giao diện đăng kí tài khoản
 
Giao diện chi tiết món ăn
 
Giao diện đặt hàng
 

Giao diện cập nhật danh mục.
 
Giao diện quản lý danh mục.
 
Giao diện thêm mới món ăn.
 

 Giao diện quản lý món ăn.
 
Giao diện đổi mật khẩu.
 

