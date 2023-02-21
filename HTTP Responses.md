Nguyên lý:  

    Khi bạn nhập vào địa chỉ *******.com, kết quả trả về (response) chính là giao diện của website và các thông tin của header. Như vậy dữ liệu mà server trả về là những đoạn mã HTML kèm theo các thông tin của header. Browser sẽ dựa vào các thông tin này để hiển thị trạng thái kết quả của request. Mã HTML dùng để hiển thị giao diện của website. Nếu bạn nhập vào một URL không tồn tại thì thông tin của header cũng sẽ không có gì.  
    
Cấu trúc của HTTP Respones:  
    <img width="575" alt="image" src="https://user-images.githubusercontent.com/125866921/220240219-47766dfa-047e-4e27-a0c0-208ed60b020e.png">  
    
Cấu trúc HTTP Response gần giống với HTTP request. Điểm khác biẹt là thay vì Request-Line, HTTP có response có Status-Line. Tương tự như Request-Line, Status-Line cũng có ba phần được phần cách với nhau bằng khoảng trống như sau:  

    HTTP-version: phiên bản HTTP cao nhất mà server hỗ trợ.  
    
    Status-Code: mã kết quả trả về.  
    
    Reason-Phrase: mô tả về Status-Code.  
    
Yếu tố Status-Code là một số nguyên 3 ký tự. Ký tự đầu tiên của mã hóa trạng thái định nghĩa hạng (loại) phản hồi và hai ký tự cuối không có bất cứ vai trò phân loại nào. Có 5 giá trị của ký tự đầu tiên:  

    1xx: Thông tin. Mã này nghĩa là yêu cầu đã được nhận và tiến trình đang tiếp tục.  
    
    2xx (PHỔ BIẾN NHẤT): Thành công. Mã này nghĩa là hoạt động đã được nhận, được hiểu, và được chấp nhận một cách thành công.  
    
    3xx: Sự điều hướng lại. Mã này nghĩa là hoạt động phải được thực hiện để hoàn thành yêu cầu.  
    
    4xx: Lỗi Client. Mã này nghĩa là yêu cầu chứa cú pháp không chính xác hoặc không được thực hiện.  
    
    5xx: Lỗi Server. Mã này nghĩa là Server thất bại với việc thực hiện một yêu cầu nhìn như có vẻ khả thi.  
    
Một số điểm đáng quan tâm khác:  

    The Server header chứa biểu ngữ cho biết phần mềm máy chủ web đang được sử dụng và đôi khi là các chi tiết khác như mô-đun đã cài đặt và hệ điều hành máy chủ. Thông tin chứa đựng có thể chính xác hoặc không.  
    
    The Set-Cookie header cấp cho trình duyệt một cookie khác; điều này được gửi lại trong tiêu đề Cookie của các yêu cầu tiếp theo tới máy chủ này.  
    
    The Pragma header hướng dẫn trình duyệt không lưu trữ phản hồi trong bộ đệm của nó. Tiêu đề Hết hạn chỉ ra rằng nội dung phản hồi đã hết hạn trong quá khứ và do đó không được lưu vào bộ nhớ đệm. Các hướng dẫn này thường được đưa ra khi nội dung động được trả về để đảm bảo rằng các trình duyệt có được phiên bản mới của nội dung này vào lần tiếp theo.  
    
    Hầu như tất cả các phản hồi HTTP đều chứa nội dung thư theo dòng trống sau tiêu đề. The Content-Type header chỉ ra rằng phần nội dung của thư này chứa tài liệu HTML.  
    
    The Content-Length header cho biết độ dài của nội dung thư tính bằng byte.  
