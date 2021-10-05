## [Sun* Service](https://ctf.viblo.asia/puzzles/sun-service-knjw1vcjylx)

![image-20200412223749696](images/image-20200412223749696.png)

***

Ban đầu vào chỉ có 1 form. Ta sẽ thử truyền 1 domain hoặc ip vào:

![image-20200412223915987](images/image-20200412223915987.png)

Kết quả là đó là 1 công cụ ping

![image-20200412224102087](images/image-20200412224102087.png)

Chúng ta thử **google.com;cat index.php** tuy nhiên nó đã chặn space => ta bypass bằng **google.com;cat${IFS}index.php**

Trong đó **${IFS}** là 1 biến đặc biệt trong shell (**Internal Field Separator**) giá trị mặc định của nó là: **space, tab** hoặc **newline**

![image-20200412224928918](images/image-20200412224928918.png)

`Flag{Th1s_1s_4n_3asY_FL4G_R1ght?}`