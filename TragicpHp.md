## [Tragic pHp](https://ctf.viblo.asia/puzzles/tragic-php-jjq3i6qrgkd)

![image-20200412223825524](images/image-20200412223825524.png)



![image-20200411234150293](images/image-20200411234150293.png)

![image-20200411234202640](images/image-20200411234202640.png)

Truy cập  http://172.104.49.143:1303/index.phps ta có mã nguồn của index.php. Đọc qua 1 chút thì ta xác định được là phải bypass **strcmp** của php

![image-20200411234217243](images/image-20200411234217243.png)



Có rất nhiều cách để bypass tuy nhiên mình vẫn sử dụng Chrome DevTools:

![image-20200411234554897](images/image-20200411234554897.png)

Thay đổi value thành value[] và submit form. Trong php **strcmp()** chỉ nhận tham số là 1 chuỗi, nếu truyền vào là 1 mảng sẽ gây lỗi khiến việc so sánh chuỗi luôn luôn đúng.

![image-20200411234640326](images/image-20200411234640326.png)

`Flag{dont_trust_strcmp_at_all}`