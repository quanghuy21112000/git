# Cấu hình ip ens33: 192.168.0.90/24 

  - Sau khi login hệ thống chúng ta vào thư mục sau: `/etc/sysconfig/network-scripts/`  bằng lệnh:

    `cd /etc/sysconfig/network-scripts/`
    
      ![](./icon/55.png)
      
  - Nhập lệnh `ls` để lấy danh sách các file và thư mục.
      
      ![](./icon/56.png)
      
  - Ở đây chúng ta cần cấu hình cho **ifcfg-ens33** nên ta sử sụng lệnh `vi ifcfg-ens33` để chỉnh cấu hình và có kết quả sau:

      ![](./icon/57.png)
   
  - Sau đó khởi động lại bằng lệnh `systemctl restart network.service`. Sau đó kiểm tra cấu hình bằng lệnh `ip addr`.
      
      ![](./icon/58.png)
        
  - Như vậy là đã hoàn thành xong.
      
