## [Enough PHP magic](https://ctf.viblo.asia/puzzles/enough-php-magic-qtd1odoekwl)

![image-20200412225019506](images/image-20200412225019506.png)

![image-20200412225054265](images/image-20200412225054265.png)

Ta scan thử => tìm được file index.phps và mã nguồn như sau:

![image-20200412225611815](images/image-20200412225611815.png)

Ta chú ý hàm **extract** nó sẽ nhận vào 1 mảng và trích xuất mảng tạo ra các biến

Vì thế ta có thể thay đổi `$filename` thành rỗng và từ đó `$combination` cũng rỗng khiến `$attempt` = ` $combination`

Payload: http://172.104.49.143:1307/index.php?filename=&attempt

`Flag{extract_is_not_safe}`