## [Web13](https://ctf.viblo.asia/puzzles/web13-hltbsx0esfz)

![image-20200620100633869](images/image-20200620100633869.png)

![image-20200620100655281](images/image-20200620100655281.png)

![image-20200620100727162](images/image-20200620100727162.png)

![image-20200620100746268](images/image-20200620100746268.png)

Ta thử LFI đọc file /etc/passwd tuy nhiên yêu cầu đầu vào phải là URL, ta sử dụng thêm URI scheme file://

![image-20200620100912723](images/image-20200620100912723.png)

OK giờ ta sẽ đọc file index.php. Thông qua 1 symbolic link tới current working directory của tiến trình

`Payload: file:///proc/self/cwd/index.php`

file config.php

`Payload: file:///proc/self/cwd/config.php`

![image-20200620113830244](images/image-20200620113830244.png)

`Flag{OKOK_YAH_FLAG_123!}`

