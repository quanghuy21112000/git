# Quản lý đĩa

 I. **Các thiết bị đĩa**
  
  1. **dmesg** 
   - Thông báo khởi động hạt nhân có thể được nhìn thấy sau khi khởi động bằng dmesg. Vì các thiết bị đĩa cứng 
được nhân phát hiện trong quá trình khởi động, bạn cũng có thể sử dụng dmesg để tìm thông tin về các 
thiết bị đĩa.
    
     ![](./image/4.png)
   
  2. **/ proc / scsi / scsi** 
   - Định vị thiết bị scsi thông qua cat / proc / scsi / scsi .
    
      ![](./image/5.png)
   
   
 II. **Phân vùng đĩa**
  
   1. **Về phân vùng**
   - Linux yêu cầu bạn tạo một hoặc nhiều phân vùng. Các đoạn tiếp theo sẽ giải thích cách để tạo và sử dụng phân vùng.
   - Hình dạng và kích thước của một phân vùng thường được xác định bởi một hình trụ bắt đầu và kết thúc (đôi khi theo lĩnh vực). Các phân vùng có thể thuộc loại chính (tối đa bốn), mở rộng (tối đa một) hoặc lôgic (chứa trong phân vùng mở rộng). Mỗi phân vùng có một nhập trường có chứa mã. Điều này xác định hệ điều hành máy tính hoặc
hệ thống tệp phân vùng.
   
       ![](./image/6.png)
  
   2. **Các phân vùng**
   - Tệp /proc/partitions chứa một bảng với số lượng phân vùng chính và phụ thiết bị, số khối của chúng và tên thiết bị trong / dev. Xác minh với / proc / devices để liên kết số chính với thiết bị thích hợp.
   
        ![](./image/7.png)
   
   - **df -h**: để hiển thị các phân vùng và kích thước hiện có.
     
        ![](./image/8.png)
     
 III. **Hệ thống tập tin**
  
   1. **Về hệ thống tệp** 
   - Hệ thống tệp là một cách sắp xếp các tệp trên phân vùng của bạn. Bên cạnh lưu trữ dựa trên tệp, hệ thống tệp thường bao gồm thư mục và kiểm soát truy cập, đồng thời chứa thông tin meta về tệp như thời 
gian truy cập, thời gian sửa đổi và quyền sở hữu tệp.
   - Các thuộc tính (độ dài, bộ ký tự, ...) của tên tệp được xác định bởi hệ thống tệp bạn chọn. Thư mục thường được triển khai dưới dạng tệp, bạn sẽ phải tìm hiểu cách thực hiện điều này! Kiểm soát truy cập trong hệ thống tệp được theo dõi bởi quyền sở hữu của người dùng (và chủ sở hữu nhóm và thành 
viên) kết hợp với một hoặc nhiều danh sách kiểm soát truy cập.
   - **man fs**: Trang hướng dẫn về hệ thống tệp được truy cập.
     
       ![](./image/9.png)

   - **/ etc / filesystems**: Tệp / etc / filesystems chứa danh sách các hệ thống tệp được phát hiện tự động (trong trường hợp lệnh mount được sử dụng mà không có tùy chọn -t.
   2. **Hệ thống tệp chung**
   - **ext2 và ext3**: Một khi hệ thống tệp Linux phổ biến nhất là hệ thống tệp ext2 (mở rộng thứ hai). Một bất lợi là việc kiểm tra hệ thống tệp trên ext2 có thể mất nhiều thời gian. ext2 đã được thay thế bằng ext3 trên hầu hết các máy Linux. Về cơ bản chúng giống nhau, ngoại trừ việc 
ghi nhật ký chỉ có trong ext3. 
   - **ext4**: ext4 hỗ trợ các tệp lớn hơn (lên đến 16 terabyte) và các hệ thống tệp lớn hơn ext3 (và nhiều tính năng khác).
   - **xfs**:một hệ thống tệp hiệu suất cao có khả năng mở rộng cao.
   - Tệp / proc / filesystems hiển thị danh sách các hệ thống tệp được hỗ trợ. Khi bạn mount một hệ thống tệp mà không xác định rõ ràng một hệ thống tệp, thì mount trước tiên sẽ cố gắng thăm dò / etc / filesystems và sau đó thăm dò / proc / filesystems cho tất cả các hệ thống tệp không có nhãn nodev. Nếu / etc / filesystems kết thúc bằng một dòng chỉ chứa dấu hoa thị (*) thì cả hai tệp đều được kiểm tra.
   
       ![](./image/10.png)
       
  3. **Đặt một hệ thống tệp trên một phân vùng**
   - Bây giờ chúng ta có một phân vùng mới. Hệ thống nhị phân để tạo hệ thống tệp có thể được tìm thấy với ls.
   
       ![](./image/11.png)
   
  4. **Kiểm tra hệ thống tệp**
   - Lệnh fsck là một công cụ giao diện người dùng để kiểm tra lỗi của hệ thống tệp.

       ![](./image/12.png)
  
 IV. 
 
     
        
  
                                                                                                              
  
                                                                                                              
                                                                                                              
                                                                                                              

       
