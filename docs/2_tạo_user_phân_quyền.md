# TẠO USER 



## I. TẠO USER.

TUY NHIÊN, ORCL YÊU CẦU TÊN USER PHẢI CHỨA TIỀN TỐ NÓ TẠO SẴN. TA CÓ THỂ LÀM THEO NHỮNG BƯỚC SAU:

### BƯỚC 1:

`SHOW PARAMETER COMMON_USER_PREFIX;` check tiền tố nó là gì?

`ALTER SYSTEM SET COMMON_USER_PREFIX = 'new_prefix' SCOPE=SPFILE;`: đổi tiền tố  theo ý thích!

- ví dụ: `ALTER SYSTEM SET COMMON_USER_PREFIX = 'U' SCOPE=SPFILE;`
Sau khi thực hiện bước này, các người dùng mới sẽ có tiền tố là U##, ví dụ: U01, U02, vv. 


### BƯỚC 2:
```
SHUTDOWN IMMEDIATE;
STARTUP;

CREATE SPFILE FROM MEMORY;


```

### BƯỚC 3: 


`CREATE USER orcl IDENTIFIED BY password`: lệnh tạo user.

TÊn user = tientouser nhé. phải như vậy!


## II. TẠO GROUP.

