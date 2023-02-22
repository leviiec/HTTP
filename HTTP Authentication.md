HTTP authentication – còn được gọi là cơ chế xác thực HTTP giúp người dùng xác minh danh tính. Nó là một cơ chế bảo mật kiểm tra xem người dùng có đủ điều kiện truy cập web hay không. Khi máy khách và máy chủ giao tiếp với nhau, dựa vào thành phần HTTP, máy chủ sẽ yêu cầu thông tin đăng nhập để xác thực. Vậy nên có thể nói, việc xác thực web sẽ thông qua tiêu chuẩn HTTP bảo đảm an toàn cho người dùng.  

Một phiên bản bảo mật hơn HTTP chính là HTTPS (S viết tắt từ SSL) có khả năng thiết lập mã hóa khi giao tiếp. Có nhiều cách để cơ chế xác thực HTTP để khiến cho các thông tin đăng nhập của tin tặc không đủ quyền bẻ khóa. Từ đó, việc truy cập của người dùng sẽ trở nên an toàn hơn trong môi trường mạng.  

HTTP có một framework chung để kiểm soát kiềm truy cập của người dùng vào tài nguyên web. Tất nhiên framework sẽ dựa vào tiêu đề (header) xác thực để sử dụng. Các header hỗ trợ người dùng cách cung cấp thông tin đăng nhập của họ và hồ sơ. Có hai loại header chủ yếu là: WWW-Authenticate header và Proxy Authentication header.  

Giao thức HTTP bao gồm các cơ chế riêng để xác thực người dùng bằng các sơ đồ xác thực khác nhau, bao gồm:  
    
    Basic là một cơ chế xác thực đơn giản gửi thông tin đăng nhập của người dùng dưới dạng chuỗi được mã hóa Base64 trong tiêu đề yêu cầu (request header) với mỗi thông báo.  
    
    NTLM là một cơ chế thử thách-phản hồi và sử dụng một phiên bản của giao thức Windows NTLM.  
    
    Digest là một cơ chế thử thách-phản hồi và sử dụng tổng kiểm tra MD5 của nonce với thông tin đăng nhập của người dùng.  
    
    HTTP Authentication Schemes: còn được gọi là lược đồ xác thực HTTP. Máy chủ đưa ra những lược đồ xác thực khác nhau cho người dùng lựa chọn. Chúng đều là những phương pháp dùng trên web cho độ an toàn cao.  
    
    Bearer authentication (xác thực đa yếu tố): xác thực dựa trên mã thông báo. Nó có thêm một lớp bổ sung và bảo mật cấp với mã thông báo để xác thực thông tin nhận được từ người dùng.  
    
    Negotiate authentication (đàm phán xác thực): là phiên bản nâng cấp của NTLM. Nó sử dụng giao thức Kerberos làm nhà cung cấp xác thực một cách nhanh chóng và an toàn.  
    
    
Tương đối hiếm khi gặp các giao thức xác thực này đang được sử dụng bởi các ứng dụng web được triển khai trên Internet. Chúng được sử dụng phổ biến hơn trong các tổ chức để truy cập các dịch vụ dựa trên mạng nội bộ.  

Web Functionality:  
  Ngoài giao thức liên lạc cốt lõi được sử dụng để gửi tin nhắn giữa máy khách và máy chủ, các ứng dụng web sử dụng nhiều công nghệ để cung cấp chức năng của chúng. Bất kỳ ứng dụng chức năng hợp lý nào cũng có thể sử dụng hàng chục công nghệ riêng biệt trong các thành phần máy chủ và máy khách của nó. Trước khi bạn có thể thực hiện một cuộc tấn công nghiêm trọng vào một ứng dụng web, bạn cần có hiểu biết cơ bản về cách thức triển khai chức năng của ứng dụng đó, cách các công nghệ được sử dụng được thiết kế để hoạt động và điểm yếu của chúng có thể nằm ở đâu.  

Server-Side Functionality:  

  World Wide Web ban đầu chứa nội dung hoàn toàn tĩnh. Trang web bao gồm nhiều tài nguyên khác nhau, chẳng hạn như trang HTML và hình ảnh, được tải đơn giản lên máy chủ web và gửi tới bất kỳ người dùng nào yêu cầu chúng. Mỗi khi một tài nguyên cụ thể được yêu cầu, máy chủ sẽ phản hồi với cùng một nội dung.  
    
  Các ứng dụng web ngày nay vẫn thường sử dụng một số lượng lớn tài nguyên tĩnh. Tuy nhiên, một lượng lớn nội dung mà chúng hiển thị cho người dùng được tạo động. Khi người dùng yêu cầu một tài nguyên động, phản hồi của máy chủ sẽ được tạo nhanh chóng và mỗi người dùng có thể nhận được nội dung được tùy chỉnh riêng cho họ.  
  
  Nội dung động được tạo bởi các tập lệnh hoặc mã thực thi khác trên máy chủ. Các tập lệnh này giống như các chương trình máy tính theo đúng nghĩa của chúng. Chúng có nhiều đầu vào khác nhau, thực hiện xử lý trên những đầu vào này và trả lại đầu ra của chúng cho người dùng.  
  
  Khi trình duyệt của người dùng yêu cầu một tài nguyên động, thông thường nó không chỉ yêu cầu một bản sao của tài nguyên đó. Nói chung, nó cũng gửi các tham số khác nhau cùng với yêu cầu của nó. Chính các tham số này cho phép ứng dụng phía máy chủ tạo nội dung phù hợp với từng người dùng. Các yêu cầu HTTP có thể được sử dụng để gửi tham số đến ứng dụng theo ba cách chính:  
    
    Trong chuỗi truy vấn URL.  
    
    Trong đường dẫn tệp của URL kiểu REST.  
    
    Trong HTTP Cookies.  
    
    Trong phần thân của yêu cầu sử dụng phương thức POST.  
    
  Ngoài các nguồn đầu vào chính này, về nguyên tắc, ứng dụng phía máy chủ có thể sử dụng bất kỳ phần nào của yêu cầu HTTP làm đầu vào cho quá trình xử lý của nó. Ví dụ: một ứng dụng có thể xử lý User-Agent header để tạo nội dung được tối ưu hóa cho loại trình duyệt đang được sử dụng.  
  
  Giống như phần mềm máy tính nói chung, các ứng dụng web sử dụng nhiều loại công nghệ ở phía máy chủ để cung cấp chức năng của chúng:  
  
    Scripting languages như PHP, VBScript, and Perl.  
    
    Các nền tảng ứng dụng web như ASP.NET và Java.  
    
    Các máy chủ web như Apache, IIS và Netscape Enterprise.  
    
    Cơ sở dữ liệu như MS-SQL, Oracle và MySQL.  
    
    Các thành phần phụ trợ khác như hệ thống tệp, dịch vụ web dựa trên SOAP và dịch vụ thư mục.  
    
The Java Platform:  

    Trong nhiều năm, Nền tảng Java, Phiên bản Doanh nghiệp (trước đây gọi là J2EE) là một tiêu chuẩn thực tế cho các ứng dụng doanh nghiệp quy mô lớn. Ban đầu được phát triển bởi Sun Microsystems và hiện thuộc sở hữu của Oracle, nó phù hợp với các kiến trúc đa tầng và cân bằng tải, đồng thời rất phù hợp để phát triển mô-đun và tái sử dụng mã. Do có lịch sử lâu đời và được áp dụng rộng rãi nên có nhiều công cụ phát triển, máy chủ ứng dụng và khung chất lượng cao để hỗ trợ các nhà phát triển. Nền tảng Java có thể chạy trên một số hệ điều hành cơ bản, bao gồm Windows, Linux và Solaris.  
    
    Mô tả về các ứng dụng web dựa trên Java thường sử dụng một số thuật ngữ có khả năng gây nhầm lẫn cần phải biết như sau:  
    
        Enterprise Java Bean (EJB) là một thành phần phần mềm tương đối nặng đóng gói logic của một chức năng kinh doanh cụ thể trong ứng dụng. EJB nhằm giải quyết các thách thức kỹ thuật khác nhau mà các nhà phát triển ứng dụng phải giải quyết, chẳng hạn như tính toàn vẹn của giao dịch.  
        
        A Plain Old Java Object (POJO) là một đối tượng Java thông thường, khác với một đối tượng đặc biệt như EJB. Một POJO thường được sử dụng để biểu thị các đối tượng do người dùng định nghĩa và đơn giản hơn và nhẹ hơn nhiều so với EJB và những đối tượng được sử dụng trong các khuôn khổ khác.  
        
        A Java Servlet là một đối tượng cư trú trên một máy chủ ứng dụng và nhận các yêu cầu HTTP từ các máy khách và trả về các phản hồi HTTP. Việc triển khai Servlet có thể sử dụng nhiều giao diện để tạo điều kiện phát triển các ứng dụng hữu ích.  
        
        A Java web container là một nền tảng hoặc công cụ cung cấp môi trường thời gian chạy cho các ứng dụng web dựa trên Java. Ví dụ về bộ chứa web Java là Apache Tomcat, BEA WebLogic và JBoss.  
        
      Nhiều ứng dụng web Java sử dụng các thành phần nguồn mở và bên thứ ba cùng với mã được tạo tùy chỉnh. Đây là một lựa chọn hấp dẫn vì nó giảm nỗ lực phát triển và Java rất phù hợp với cách tiếp cận mô đun này. Dưới đây là một số ví dụ về các thành phần thường được sử dụng cho các chức năng chính của ứng dụng:  
      
        Authentication — JAAS, ACEGI.  
        
        Presentation layer — SiteMesh, Tapestry.  
        
        Database object relational mapping — Hibernate.  
        
        Logging — Log4J.  
        
      Nếu bạn có thể xác định gói nguồn mở nào được sử dụng trong ứng dụng mà bạn đang tấn công, bạn có thể tải xuống các gói này và thực hiện đánh giá mã hoặc cài đặt chúng để thử nghiệm. Một lỗ hổng trong bất kỳ lỗ hổng nào trong số này có thể bị khai thác để làm tổn hại đến ứng dụng rộng hơn.  
      
