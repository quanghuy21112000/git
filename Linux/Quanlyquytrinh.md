# Quản lý quy trình 
  
  I. **Giới thiệu về các quy trinh**
  
   1. **Quản lý quy trình cơ bản**
    
        - **$$ và $ PPID**: Một số biến môi trường shell chứa thông tin về các tiến trình. Biến $$ sẽ giữ ID quy trình hiện tại của bạn và $ 
PPID chứa PID mẹ. Thực ra $$ là một tham số shell và không phải là một biến, bạn không thể gán giá trị cho nó. Dưới đây là một ví dụ.
       
        ![](./image/1.png)
       
        - **pidof**: tìm thấy tất cả id quy trình theo tên bằng lệnh pidof.
        - **parent and child**: Các quy trình có mối quan hệ parent-child. Mọi quy trình đều có quy trình mẹ.
Khi bắt đầu một bash mới , bạn có thể sử dụng echo để xác minh rằng pid trước đó có phải là ppid của shell mới 
hay không. Tiến trình con từ phía trên bây giờ là tiến trình cha mẹ.
        - **fork and exec**: Một quá trình bắt đầu một quá trình khác trong hai giai đoạn. Đầu tiên, quá trình này tạo ra một nhánh rẽ của chính nó, một bản sao giống hệt nhau. Sau đó, quá trình được chia nhỏ thực hiện một tệp thi hành để thay thế quá trình được chia nhỏ bằng quá trình con đích.

  
  II. **Các ưu tiên**
  
  III. **Giải pháp**
