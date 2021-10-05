##  [Web5](https://ctf.viblo.asia/puzzles/web5-takknpf4nb2)

![image-20200620094503579](images/image-20200620094503579.png)

![image-20200620095137281](images/image-20200620095137281.png)



Thử 1 vài công cụ và payload, ta nhận định đây là **Templates Injections**, cụ thể là Jinja2 của python

thử payload: {{7*'7’}} ta thu được kết quả như sau:

![image-20200620095305151](images/image-20200620095305151.png)

Ta sử dụng tplmap để tấn công và thực hiện shell

![image-20200620095428105](images/image-20200620095428105.png)

![image-20200620095543244](images/image-20200620095543244.png)

![image-20200620095609860](images/image-20200620095609860.png)

#### `Flag{cTf_iS_n0t_H@rd`}

