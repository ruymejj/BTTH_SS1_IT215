PHẦN 1: KHÁI NIỆM CƠ BẢN
1.1. Backend là gì?
Khi nói đến một ứng dụng web, chúng ta thường tưởng tượng ngay đến những gì mình nhìn thấy: nút bấm, thanh menu, hình ảnh, màu sắc. Phần hiển thị đó được gọi là Frontend – phần "mặt tiền" của ứng dụng.
Backend là phần ngược lại: nó nằm phía sau, người dùng không trực tiếp nhìn thấy nhưng lại là nơi xử lý toàn bộ logic của ứng dụng. Backend đảm nhiệm các công việc như:
-Nhận yêu cầu từ người dùng (thông qua Frontend)
-Xử lý dữ liệu: tính toán, kiểm tra, phân tích
-Giao tiếp với cơ sở dữ liệu để lưu trữ hoặc truy xuất thông tin
-Trả về kết quả phù hợp cho người dùng
Ví dụ thực tế: Khi đăng nhập vào một trang mạng xã hội, phần Backend là nơi kiểm tra tài khoản và mật khẩu có khớp trong cơ sở dữ liệu hay không, rồi mới quyết định cho phép đăng nhập. Nếu không có Backend, ứng dụng chỉ là một tờ giấy vẽ đẹp nhưng không có chức năng gì.
1.2. Client – Server là gì?
Mô hình Client – Server là nền tảng của giao tiếp trên Internet, giống như mối quan hệ giữa khách hàng và nhà hàng phục vụ.
Client (Máy khách) là bên gửi yêu cầu. Đây có thể là trình duyệt web (Chrome, Firefox...), ứng dụng di động, hoặc một chương trình tự động gọi API.
Server (Máy chủ) là bên nhận yêu cầu, xử lý và trả kết quả về. Server thường là một máy tính mạnh mẽ chạy liên tục 24/7 và có thể phục vụ hàng nghìn Client cùng lúc.
Quy trình diễn ra như sau: Client gửi yêu cầu → Server nhận → Server xử lý → Server trả kết quả → Client hiển thị cho người dùng. Đây là một vòng lặp xảy ra mỗi khi thực hiện bất kỳ thao tác nào trên web.
1.3. API là gì?
API là viết tắt của Application Programming Interface – tạm dịch là "Giao diện lập trình ứng dụng". Khái niệm này thực ra rất gần gũi nếu nhìn qua một ví dụ thực tế.
Hãy hình dung một nhà hàng: khách hàng không tự vào bếp lấy thức ăn mà đặt món qua người phục vụ. Người phục vụ chính là API – cầu nối trung gian giữa khách hàng (Client) và nhà bếp (Server). Khách hàng chỉ cần biết gọi món gì, không cần biết bếp nấu như thế nào.
Trong lập trình, API định nghĩa những yêu cầu nào có thể gửi đi, định dạng của yêu cầu và phản hồi, cũng như cách hai hệ thống "nói chuyện" với nhau. API giúp các hệ thống viết bằng ngôn ngữ khác nhau vẫn có thể giao tiếp được với nhau.
1.4. JSON là gì?
JSON (JavaScript Object Notation) là định dạng văn bản dùng để trao đổi dữ liệu giữa Client và Server. Dù tên có chứa "JavaScript" nhưng JSON được hỗ trợ bởi hầu hết mọi ngôn ngữ lập trình hiện đại.
Điểm mạnh của JSON là dễ đọc đối với cả con người lẫn máy móc. Dữ liệu được tổ chức theo cặp key–value (khóa–giá trị) và có thể lồng nhau. Ví dụ, thông tin một người dùng bao gồm tên, tuổi, email, danh sách sở thích đều được ghi rõ ràng theo cấu trúc nhất định.
Khi tìm kiếm sản phẩm trên một trang thương mại điện tử, Server trả về danh sách sản phẩm dưới dạng JSON, rồi Frontend đọc dữ liệu đó và hiển thị thành những thẻ sản phẩm trên màn hình.
PHẦN 2: KIẾN THỨC WEB CƠ BẢN
2.1. HTTP là gì?
HTTP (HyperText Transfer Protocol) là giao thức truyền thông được sử dụng để giao tiếp giữa Client và Server trên Web. Nói đơn giản, HTTP là "ngôn ngữ chung" mà mọi trình duyệt và máy chủ đều phải tuân theo để hiểu nhau.
Mỗi khi gõ một địa chỉ web vào trình duyệt, trình duyệt gửi một HTTP Request đến máy chủ. Máy chủ xử lý xong thì gửi lại một HTTP Response. Trong phản hồi đó có mã trạng thái (status code) cho biết kết quả: 200 là thành công, 404 là không tìm thấy, 500 là lỗi phía máy chủ, 401 là chưa xác thực.
Phiên bản bảo mật của HTTP là HTTPS (có chữ S là Secure). HTTPS mã hóa dữ liệu truyền đi nên an toàn hơn, đặc biệt quan trọng khi xử lý thông tin nhạy cảm như mật khẩu hay thông tin thẻ ngân hàng.
2.2. Các phương thức HTTP: GET, POST, PUT, DELETE
HTTP cung cấp nhiều phương thức (method) khác nhau để xác định mục đích của yêu cầu. Bốn phương thức phổ biến nhất tương ứng với bốn thao tác cơ bản khi làm việc với dữ liệu – thường gọi tắt là CRUD (Create, Read, Update, Delete):
GET – Lấy dữ liệu: Dùng để yêu cầu Server trả về dữ liệu mà không làm thay đổi gì trên Server. Ví dụ: xem danh sách sản phẩm, xem thông tin cá nhân, tải trang web.
POST – Gửi dữ liệu mới: Dùng để gửi dữ liệu lên Server nhằm tạo mới một bản ghi. Dữ liệu được gửi trong phần thân (body) của request nên phù hợp với thông tin nhạy cảm. Ví dụ: đăng ký tài khoản, đặt hàng.
PUT – Cập nhật dữ liệu: Dùng để thay thế hoặc cập nhật một bản ghi đã tồn tại. Thường phải cung cấp toàn bộ thông tin của bản ghi. Ví dụ: chỉnh sửa thông tin cá nhân, cập nhật bài đăng.
DELETE – Xóa dữ liệu: Dùng để yêu cầu Server xóa một bản ghi cụ thể. Ví dụ: xóa bình luận, hủy đơn hàng.
Việc sử dụng đúng phương thức HTTP không chỉ giúp code rõ ràng hơn mà còn là chuẩn thiết kế trong xây dựng API hiện đại (REST API).
PHẦN 3: TÌM HIỂU FastAPI
3.1. FastAPI là gì?
FastAPI là một web framework Python hiện đại, được thiết kế để xây dựng API một cách nhanh chóng, đơn giản và đáng tin cậy. Framework này do Sebastián Ramírez tạo ra và phát hành lần đầu vào năm 2018. Dù còn khá mới, FastAPI đã nhanh chóng trở nên phổ biến nhờ những ưu điểm vượt trội.
Tên gọi FastAPI phản ánh đúng hai điểm mạnh cốt lõi: tốc độ thực thi cao (Fast) và việc xây dựng API trở nên dễ dàng (API). Framework này tận dụng hai thư viện hiện đại của Python là Pydantic (kiểm tra và xác thực dữ liệu) và Starlette (xử lý HTTP bất đồng bộ).
3.2. FastAPI dùng để làm gì?
FastAPI được sử dụng chủ yếu để:
-Xây dựng REST API cho ứng dụng web hoặc mobile: Tạo ra các endpoint để Frontend hoặc ứng dụng di động có thể gọi và nhận dữ liệu.
-Phát triển Microservices: Mỗi dịch vụ nhỏ trong hệ thống lớn có thể được xây dựng riêng biệt bằng FastAPI.
-Xây dựng backend cho ứng dụng AI/Machine Learning: FastAPI rất phổ biến trong việc triển khai các mô hình AI vì Python là ngôn ngữ chính trong lĩnh vực này.
-Tạo các dịch vụ xử lý dữ liệu: Nhận dữ liệu đầu vào, xử lý và trả kết quả – phù hợp với các pipeline dữ liệu.
Một điểm đặc biệt là FastAPI tự động tạo ra tài liệu API tương tác (giao diện Swagger UI) ngay khi viết code. Điều này giúp lập trình viên dễ dàng kiểm thử và chia sẻ tài liệu mà không cần viết thêm bất kỳ dòng code nào.
3.3. FastAPI khác gì so với web framework truyền thống?
Qua quá trình tìm hiểu, em nhận thấy FastAPI có một số điểm khác biệt đáng kể so với các framework truyền thống như Django hay Flask:
Về tốc độ và hiệu năng: FastAPI được xây dựng trên nền tảng bất đồng bộ (async/await) từ đầu, cho phép xử lý nhiều request cùng lúc mà không cần chờ đợi nhau. Các framework truyền thống như Flask ban đầu được thiết kế theo mô hình đồng bộ. Đây là lý do tốc độ của FastAPI được đánh giá ngang ngửa với framework viết bằng Node.js hay Go.
Về xác thực dữ liệu tự động: FastAPI tích hợp sẵn Pydantic để kiểm tra dữ liệu. Khi người dùng gửi dữ liệu sai định dạng, FastAPI tự động phát hiện và trả về thông báo lỗi rõ ràng mà không cần lập trình viên phải tự viết code kiểm tra. Với Flask, việc này phải làm thủ công hoặc dùng thêm thư viện bên ngoài.
Về tài liệu tự động: FastAPI tự động sinh ra trang tài liệu API tương tác (Swagger UI và ReDoc) chỉ từ code đã viết. Với Django REST Framework hay Flask, lập trình viên thường phải viết tài liệu thủ công hoặc dùng công cụ bên ngoài – đây là điểm em thấy ấn tượng nhất.
Về việc sử dụng type hint: FastAPI khuyến khích và tận dụng tối đa tính năng type hint của Python hiện đại. Điều này không chỉ giúp code dễ đọc hơn mà còn giúp trình soạn thảo như VS Code hỗ trợ gợi ý code tốt hơn.
Tuy nhiên, FastAPI cũng có điểm cần lưu ý: vì còn tương đối mới nên cộng đồng chưa nhiều bằng Django, và FastAPI chủ yếu tập trung vào xây dựng API chứ không phải là full-stack framework có thể làm luôn cả giao diện web như Django.


