# Bài 4: Lưu trữ dữ liệu đơn giản với Docker Volume

Hướng dẫn thực hiện tạo và sử dụng Docker Named Volume để lưu trữ dữ liệu bền vững giữa các container.

## Các lệnh thực hiện

1. **Tạo Docker Volume:**
   ```bash
   docker volume create easy-volume

docker run --rm -v easy-volume:/data alpine sh -c "echo 'Luu tru du lieu Docker' > /data/test.txt"

docker run --rm -v easy-volume:/data alpine cat /data/test.txt


D:\RIKKEI\DevOps\Session8_Docker\Session8_B4\homework\session_09\ex4>docker volume ls --filter name=easy-volume
DRIVER    VOLUME NAME
local     easy-volume

D:\RIKKEI\DevOps\Session8_Docker\Session8_B4\homework\session_09\ex4>docker run --rm -v easy-volume:/data alpine sh -c "echo 'Luu tru du lieu Docker' > /data/test.txt"

D:\RIKKEI\DevOps\Session8_Docker\Session8_B4\homework\session_09\ex4>docker run --rm -v easy-volume:/data alpine cat /data/test.txt
Luu tru du lieu Docker

D:\RIKKEI\DevOps\Session8_Docker\Session8_B4\homework\session_09\ex4>