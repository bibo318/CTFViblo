## [PHP Up Right It](https://ctf.viblo.asia/puzzles/php-up-right-it-x1g34zp8knu)

![image-20200411230305353](images/image-20200411230305353.png)



Khi truy cập vào thì là 1 trang trắng

![image-20200411230448132](images/image-20200411230448132.png)



Tuy nhiên có thể để ý thấy query ở link. Sau khi refresh 1 vài lần với Network tool của Chrome DevTools chúng ta có thể thấy rất nhiều query parameters và mỗi chuỗi đó chính là 1 kí tự trong flag => Sau khi nối lại ta được flag: `Flag{URI_is_Import@nT}`

![image-20200411230740868](images/image-20200411230740868.png)

