# BT2_QlGV
Bài tập Quản Lý Giáo Vụ

Cho cơ sở dữ liệu “Quản lý giáo vụ” gồm có những quan hệ sau:

🤔HOCVIEN (MAHV, HO, TEN, NGSINH, GIOITINH, NOISINH, MALOP)
Tân từ: mỗi học viên phân biệt với nhau bằng mã học viên, lưu trữ họ tên, ngày sinh, giới tính, nơi sinh, thuộc 
lớp nào.

🤔LOP (MALOP, TENLOP, TRGLOP, SISO, MAGVCN)
Tân từ: mỗi lớp gồm có mã lớp, tên lớp, học viên làm lớp trưởng của lớp, sỉ số lớp và giáo viên chủ nhiệm.

🤔KHOA (MAKHOA, TENKHOA, NGTLAP, TRGKHOA)
Tân từ: mỗi khoa cần lưu trữ mã khoa, tên khoa, ngày thành lập khoa và trưởng khoa (cũng là một giáo viên 
thuộc khoa).

🤔MONHOC (MAMH, TENMH, TCLT, TCTH, MAKHOA)
Tân từ: mỗi môn học cần lưu trữ tên môn học, số tín chỉ lý thuyết, số tín chỉ thực hành và khoa nào phụ trách.

🤔DIEUKIEN (MAMH, MAMH_TRUOC)
Tân từ: có những môn học học viên phải có kiến thức từ một số môn học trước.

🤔GIAOVIEN (MAGV, HOTEN, HOCVI,HOCHAM,GIOITINH, NGSINH, NGVL,HESO, MUCLUONG, MAKHOA)
Tân từ: mã giáo viên để phân biệt giữa các giáo viên, cần lưu trữ họ tên, học vị, học hàm, giới tính, ngày sinh, 
ngày vào làm, hệ số, mức lương và thuộc một khoa.

🤔GIANGDAY (MALOP, MAMH, MAGV, HOCKY, NAM, TUNGAY, DENNGAY)
Tân từ: mỗi học kỳ của năm học sẽ phân công giảng dạy: lớp nào học môn gì do giáo viên nào phụ trách.
KETQUATHI (MAHV, MAMH, LANTHI, NGTHI, DIEM, KQUA)

Tân từ: lưu trữ kết quả thi của học viên: học viên nào thi môn học gì, lần thi thứ mấy, ngày thi là ngày nào, 
điểm thi bao nhiêu và kết quả là đạt hay không đạt.

I. Ngôn ngữ định nghĩa dữ liệu (Data Definition Language):
1. Tạo quan hệ và khai báo tất cả các ràng buộc khóa chính, khóa ngoại. Thêm vào 3 thuộc tính 
GHICHU, DIEMTB, XEPLOAI cho quan hệ HOCVIEN.
2. Mã học viên là một chuỗi 5 ký tự, 3 ký tự đầu là mã lớp, 2 ký tự cuối cùng là số thứ tự học viên 
trong lớp. VD: “K1101”
3. Thuộc tính GIOITINH chỉ có giá trị là “Nam” hoặc “Nu”.
4. Điểm số của một lần thi có giá trị từ 0 đến 10 và cần lưu đến 2 số lẽ (VD: 6.22).
5. Kết quả thi là “Dat” nếu điểm từ 5 đến 10 và “Khong dat” nếu điểm nhỏ hơn 5.
6. Học viên thi một môn tối đa 3 lần.
7. Học kỳ chỉ có giá trị từ 1 đến 3.
8. Học vị của giáo viên chỉ có thể là “CN”, “KS”, “Ths”, ”TS”, ”PTS”.
9. Lớp trưởng của một lớp phải là học viên của lớp đó.
10. Trưởng khoa phải là giáo viên thuộc khoa và có học vị “TS” hoặc “PTS”.
