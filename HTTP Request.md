HTTP Request hiểu một cách đơn giản là các thông tin sẽ được gửi từ khách hàng (client) lên server. Server sẽ có nhiệm vụ tìm và xử lý các loại dữ liệu, thông tin, client mong muốn. HTTP Request có thể tồn tại dưới file text hoặc dưới dạng XML hoặc dạng Json. Để hiểu rõ hơn, bạn có thể tham khảo các thông tin về cấu trúc HTTP Request và một số phương phức phổ biến.  

Cấu trúc của HTTP Request bao gồm:  

    <img width="525" alt="image" src="https://user-images.githubusercontent.com/125866921/220236350-dc2d2fdb-cfdb-4bd8-aced-bb47cd476352.png">  
    
Request line là dòng đầu tiên của HTTP Request, với ba loại chính là method, path ( hay URL) và HTTP version. Cụ thể:  

    Method: gồm nhiều loại nhưng phổ biến nhất là GET và POST. Trong đó, phương thức GET có tác dụng dùng để yêu cầu các tài nguyên cung cấp trong URL.  
    
    Path (URL): có tác dụng định danh các nguồn tài nguyên được yêu cầu bởi khách hàng, người dùng và bắt buộc phải có dấu “/".  
    
    HTTP version: Đây là phiên bản HTTP được sử dụng, trong đó phổ biến nhất là HTTP/1.0 hay HTTP/1.1.  
    
Yếu tố thứ hai góp phần làm hình thành HTTP Request đó là các header. Thông tin được bổ sung sẽ truyền tải giữa cả máy chủ và máy khách, chẳng hạn như cookie, thông tin về ủy quyền, tác nhân người dùng… Tương tự một HTTP Request, header sẽ phân biệt chữ thường và chữ hoa, theo sau đó là dấu “.” và một giá trị.  

    ![image](https://user-images.githubusercontent.com/125866921/220236891-d3c1994e-9cee-4902-bc32-a2d28cb9d8de.png)  
    
Yếu tố thứ ba được đề cập đến đó là massage body. Máy chủ dùng nội dung thư để cung cấp những thông thông tin cần thiết nhất đến với máy khách. Massage body có chứa các dòng yêu cầu, thông tin, dòng trống, tiêu đề, và nội dung. Trong đó, yếu tố nội dung sẽ tùy chọn. Không phải tất cả các yêu cầu đều có nội dung nhưng sẽ dùng POST để phân phối tải trọng.  

    The Referer header được sử dụng để chỉ ra URL mà yêu cầu bắt nguồn từ đó (ví dụ: vì người dùng đã nhấp vào liên kết trên trang đó). Lưu ý rằng tiêu đề này đã bị sai chính tả trong đặc tả HTTP ban đầu và phiên bản sai chính tả đã được giữ lại kể từ đó.  
    
    The User-Agent header được sử dụng để cung cấp thông tin về trình duyệt hoặc phần mềm máy khách khác đã tạo yêu cầu. Lưu ý rằng hầu hết các trình duyệt bao gồm tiền tố Mozilla x vì lý do lịch sử. Đây là chuỗi Tác nhân người dùng được sử dụng bởi trình duyệt Netscape thống trị ban đầu và các trình duyệt khác muốn khẳng định với các trang web rằng chúng tương thích với tiêu chuẩn này. Cũng như nhiều điều kỳ quặc trong lịch sử máy tính, nó đã trở nên lâu đời đến mức nó vẫn được giữ lại, ngay cả trên phiên bản Internet Explorer hiện tại, phiên bản đã đưa ra yêu cầu được hiển thị trong ví dụ.  
    
    The Host header chỉ định tên máy chủ xuất hiện trong URL đầy đủ ang được truy cập. Điều này là cần thiết khi nhiều trang web được lưu trữ trên cùng một máy chủ, vì URL được gửi trong dòng đầu tiên của yêu cầu thường không chứa tên máy chủ. (Xem Chương 17 để biết thêm thông tin về các trang web được lưu trữ ảo.)  
    
    The Cookie header được sử dụng để gửi các tham số bổ sung mà máy chủ đã cấp cho máy khách (được mô tả chi tiết hơn ở phần sau của chương này).  
