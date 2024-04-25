# CÁC CÂU LỆNH CƠ BẢN VỚI DB.


## 


### 2.1. LÀM VIỆC VỚI BẢNG.

#### TẠO BẢNG:

```
CREATE TABLE tên bảng(
    artist_id NUMBER,-- ID của nghệ sĩ
    email VARCHAR(100),-- Địa chỉ email của nghệ sĩ
    country VARCHAR2(50),
    artist_name NVARCHAR2(100),-- Tên nghệ sĩ
    description NVARCHAR2(500), -- Mô tả về nghệ sĩ 
    artist_type VARCHAR2(50) NOT NULL, -- Loại nghệ sĩ: "composer" hoặc "performer"
    active NUMBER(1) DEFAULT 1, -- Trạng thái hoạt động của nghệ sĩ (1: active, 0: inactive)
    date_created DATE NOT NULL -- Ngày tạo nghệ sĩ trong hệ thống
);

```


#### KIỂM TRA BẢNG.


`DESCRIBE tên bảng;`: list ra thông tin của bảng.


LỆNH LIST RA TẤT CẢ CÁC BẢNG KỂ CẢ BẢNG USER K CÓ QUYỀN TRUY CẬP!.

```
SELECT table_name 
FROM all_tables;
```

LỆNH LIST RA TẤT CẢ CÁC BẢNG CỦA USER

```
SELECT table_name 
FROM user_tables;

```



