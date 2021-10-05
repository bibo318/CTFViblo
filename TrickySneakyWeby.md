## [Tricky Sneaky Weby](https://ctf.viblo.asia/puzzles/tricky-sneaky-weby-o1y7q2psuok)

![image-20200411231413127](images/image-20200411231413127.png)

Bài này có vẻ là rất nhiều level.

![image-20200411231507771](images/image-20200411231507771.png)

Khi nhập kí tự thì toàn bộ đều trở thành dạng chữ thường thay vì chữ hoa đó là vì đoạn js:

```javascript
<script>
  jQuery(document).ready(function ($) {
  $('#password').on('keydown keyup', function () {
    $(this).val($(this).val().toLowerCase());
  });
});
</script>
```

Có rất nhiều cách để bypass tuy nhiên tôi sẽ sử dụng Chrome DevTools:

![image-20200411231802307](images/image-20200411231802307.png)

Sử dụng **Event Listeners** xoá các event keydown và keyup của input#password đi sau đó copy hoặc nhập lại chuỗi `SUN$HELL`

Oke chúng ta đã pass level 1:

![image-20200411231943699](images/image-20200411231943699.png)

Tiếp tục level 2:

![image-20200411232030767](images/image-20200411232030767.png)

Đề yêu cầu là không còn trực tuyến thì sẽ hiển thị mật khẩu. Vì vậy chúng ta lại tiếp tục sử dụng Chrome DevTools để offline

![image-20200411232144976](images/image-20200411232144976.png)

![image-20200411232201039](images/image-20200411232201039.png)

![image-20200411232231591](images/image-20200411232231591.png)

Tuy nhiên flag nhận được chỉ là fake. Chúng ta xem tiếp mã nguồn của trang

![image-20200411232324827](images/image-20200411232324827.png)

Tiếp tục với level cuối:

Với level này thì trang không cho phép bôi đen và copy trực tiếp nên chúng ta sẽ vào mã nguồn copy đoạn mã f929cb2e53b11bdc223e32547a9da2622c2c913deedf2575bf95239d và sử dụng curl để gửi POST request:

![image-20200411233246761](images/image-20200411233246761.png)

Ban đầu khi copy đoạn mã vào thì chúng có chứa **<200b>** là (Unicode Character 'ZERO WIDTH SPACE’), chúng ta chỉ cần replace all nó đi là được

![image-20200411233312562](images/image-20200411233312562.png)

`Flag{only_trust_what_you_typed}`