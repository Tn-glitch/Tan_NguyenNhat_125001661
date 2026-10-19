# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

- **Họ và tên:** ........................................................
- **MSSV:** ................................................................
- **Tên đề tài Website:** VYBE – Website nghe nhạc trực tuyến
- **Công cụ AI đã sử dụng:** ChatGPT

## 1. Yêu cầu ban đầu (System/Initial Prompt)

**Prompt đã sử dụng:**

> Hãy đóng vai một lập trình viên Web chuyên nghiệp, giúp tôi xây dựng website nghe nhạc trực tuyến có tên VYBE bằng HTML5 và CSS3. Giao diện lấy cảm hứng từ Spotify và Apple Music, sử dụng tông màu đen kết hợp tím neon hiện đại. Website cần có thanh điều hướng, thanh tìm kiếm, danh sách bài hát, album, thể loại nhạc, trình phát nhạc, mục yêu thích, thư viện cá nhân và khu vực tài khoản. Thiết kế phải đẹp mắt, có hiệu ứng chuyển động, bố cục rõ ràng và tương thích với nhiều kích thước màn hình. Sử dụng Semantic HTML, CSS Variables và tổ chức mã nguồn thành hai file riêng biệt là index.html và styles.css. Ưu tiên sử dụng HTML và CSS, hạn chế JavaScript.

**Kết quả AI tạo ra:**

AI đã hỗ trợ xây dựng khung giao diện website VYBE, bao gồm thanh điều hướng bên trái, khu vực nội dung chính, banner bài hát nổi bật, danh sách nhạc, các nút lọc thể loại và thanh điều khiển giao diện. Đồng thời, AI tạo hệ thống màu sắc thống nhất bằng CSS Variables, sử dụng Font Awesome để hiển thị biểu tượng và tích hợp Animate.css để hỗ trợ hiệu ứng.

## 2. Quá trình tinh chỉnh và giải quyết sự cố (Iteration Iterations)

### Lần 1: Dựng khung Semantic HTML và CSS Variables

**Prompt đã dùng:**

> Hãy xây dựng cấu trúc HTML cho website VYBE bằng các thẻ Semantic HTML phù hợp như header, nav, main, section và footer. Tách phần giao diện và phần định dạng thành hai file index.html và styles.css. Sử dụng CSS Variables để quản lý màu sắc, kích thước, khoảng cách và hiệu ứng. Thiết kế theo phong cách dark mode kết hợp tím neon, bảo đảm mã nguồn dễ đọc và dễ chỉnh sửa.

**Kết quả AI tạo ra:**

AI tạo được bố cục chính gồm thanh điều hướng, phần đầu trang, nội dung khám phá âm nhạc và các khu vực chức năng. File CSS có các biến màu, biến kích thước, kiểu chữ, đường viền, đổ bóng và hiệu ứng chuyển tiếp. Các thẻ `nav`, `header`, `main` và `section` được sử dụng để phân chia nội dung rõ ràng.

**Nhận xét và tinh chỉnh của sinh viên:**

- Bố cục ban đầu cần được tổ chức rõ ràng để dễ bổ sung tính năng.
- Cần thống nhất màu sắc giữa các khu vực, tránh tình trạng mỗi thành phần có một kiểu định dạng riêng.
- Sử dụng CSS Variables giúp thay đổi màu sắc và kích thước trên toàn website nhanh chóng.
- Kiểm tra đường dẫn giữa file HTML và CSS để bảo đảm giao diện được hiển thị đúng.

### Lần 2: Tích hợp Animate.css và hiệu ứng chuyển động

**Prompt đã dùng:**

> Hãy bổ sung hiệu ứng chuyển động cho website VYBE để giao diện sinh động và hiện đại hơn. Tích hợp Animate.css, đồng thời sử dụng CSS Animation và Transition cho banner, thẻ bài hát, nút bấm và các thành phần giao diện. Hiệu ứng cần mượt mà, không quá rối mắt và không làm ảnh hưởng đến khả năng sử dụng website.

**Thách thức gặp phải:**

Trong quá trình xây dựng giao diện, cần bảo đảm các hiệu ứng chuyển động hoạt động phù hợp với thiết kế nền tối. Nếu sử dụng quá nhiều hiệu ứng, website có thể gây mất tập trung hoặc làm giảm trải nghiệm người dùng.

**Cách sửa prompt (Debug prompt):**

> Hãy kiểm tra lại các hiệu ứng CSS đang sử dụng. Chỉ giữ những hiệu ứng cần thiết như chuyển động nền, hiệu ứng hover và chuyển cảnh giữa các khu vực. Bảo đảm tên lớp CSS chính xác, thời gian chuyển động hợp lý và không làm thay đổi kích thước hoặc vị trí thành phần ngoài ý muốn. Kiểm tra đường dẫn thư viện Animate.css và chỉ sử dụng hiệu ứng khi cần thiết.

**Kết quả và nhận xét của sinh viên:**

Website được bổ sung các hiệu ứng chuyển động như ánh sáng nền neon, hiệu ứng hover trên thẻ thể loại và chuyển cảnh khi hiển thị nội dung. CSS sử dụng `@keyframes`, `transition` và `transform` để tạo chuyển động mà không cần viết thêm JavaScript cho các hiệu ứng này.

### Lần 3: Xây dựng danh sách bài hát và bộ lọc thể loại

**Prompt đã dùng:**

> Hãy tạo khu vực bảng xếp hạng bài hát cho website VYBE. Mỗi bài hát cần có ảnh bìa, tên bài hát, nghệ sĩ, album, trình phát âm thanh và nút yêu thích. Bổ sung bộ lọc theo thể loại như Synthwave, Lo-Fi, Electronic, Acoustic và Classical. Ưu tiên sử dụng HTML5 và CSS3 để triển khai.

**Thách thức gặp phải:**

Danh sách bài hát có nhiều thông tin nên cần bố trí thành các cột rõ ràng, tránh tình trạng nội dung bị lệch khi tên bài hát dài. Ngoài ra, bộ lọc thể loại phải có khả năng ẩn những bài hát không thuộc thể loại được chọn.

**Cách sửa prompt (Debug prompt):**

> Hãy điều chỉnh CSS để các hàng bài hát có bố cục đồng nhất, ảnh bìa có kích thước phù hợp và nội dung dài không làm vỡ giao diện. Sử dụng radio button kết hợp với bộ chọn CSS để lọc bài hát theo thể loại. Kiểm tra để khi chọn một thể loại, chỉ những bài hát tương ứng được hiển thị và khi chọn Tất cả, danh sách được khôi phục.

**Kết quả và nhận xét của sinh viên:**

AI đã hỗ trợ xây dựng danh sách bài hát bằng HTML, sử dụng các lớp CSS để phân loại thể loại nhạc và radio button để điều khiển bộ lọc. Các thẻ `audio` của HTML5 được sử dụng để phát những tệp âm thanh được liên kết.

Qua lần tinh chỉnh này, em hiểu rõ hơn cách kết hợp cấu trúc HTML với CSS để tạo ra những thành phần giao diện có tính tương tác cơ bản.

### Lần 4: Hoàn thiện giao diện và kiểm tra tính tương thích

**Prompt đã dùng:**

> Hãy rà soát giao diện website VYBE trên máy tính và màn hình nhỏ. Kiểm tra thanh điều hướng, banner, danh sách bài hát, thanh tìm kiếm và các thành phần tương tác. Điều chỉnh media queries, kích thước chữ, khoảng cách và bố cục để hạn chế tràn nội dung. Không thay đổi phong cách màu sắc chính của website và không xóa những chức năng đã xây dựng.

**Thách thức gặp phải:**

Giao diện có nhiều thành phần nên khi thay đổi kích thước màn hình, một số khu vực có thể cần điều chỉnh lại khoảng cách, kích thước hoặc cách sắp xếp. Bên cạnh đó, cần kiểm tra các đường dẫn CSS, hình ảnh và âm thanh để tránh lỗi hiển thị.

**Cách sửa prompt (Debug prompt):**

> Hãy kiểm tra từng thành phần của website, xác định những khu vực có nguy cơ tràn ngang hoặc khó sử dụng trên màn hình nhỏ. Bổ sung hoặc chỉnh sửa media queries phù hợp, giữ nguyên các chức năng hiện có và chỉ sửa những phần thực sự cần thiết. Hướng dẫn cách kiểm tra lỗi đường dẫn giữa index.html và styles.css.

**Kết quả và nhận xét của sinh viên:**

AI hỗ trợ rà soát cấu trúc giao diện và đề xuất điều chỉnh CSS để cải thiện khả năng hiển thị. Em nhận thấy việc kiểm tra website sau mỗi lần chỉnh sửa là cần thiết, vì mã nguồn có thể đúng về cú pháp nhưng giao diện thực tế vẫn chưa đáp ứng yêu cầu.

## 3. Đánh giá cá nhân về quá trình Vibe Coding

### 3.1. AI đã giúp tiết kiệm thời gian ở phần nào nhất?

AI giúp em tiết kiệm thời gian nhiều nhất ở giai đoạn xây dựng cấu trúc HTML và thiết kế CSS. Thay vì phải viết từng thành phần từ đầu, em có thể mô tả yêu cầu bằng ngôn ngữ tự nhiên để AI đề xuất bố cục, màu sắc, kiểu chữ và hiệu ứng phù hợp.

Ngoài ra, AI hỗ trợ giải thích cách sử dụng CSS Variables, Semantic HTML, radio button, checkbox và các hiệu ứng chuyển động. Nhờ đó, em có thể tập trung nhiều hơn vào việc kiểm tra giao diện, điều chỉnh bố cục và hoàn thiện trải nghiệm người dùng.

### 3.2. Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web

Qua quá trình thực hiện website VYBE, em rút ra một số bài học:

- **Đưa ra yêu cầu cụ thể:** Prompt cần nêu rõ mục tiêu website, màu sắc, bố cục, chức năng và công nghệ sử dụng.
- **Chia nhỏ công việc:** Nên phát triển lần lượt cấu trúc HTML, CSS, hiệu ứng và chức năng thay vì yêu cầu AI hoàn thành mọi thứ trong một bước.
- **Tinh chỉnh dựa trên kết quả:** Khi giao diện chưa đạt yêu cầu, cần mô tả chính xác thành phần bị lỗi và kết quả mong muốn.
- **Kiểm tra mã nguồn:** Không nên mặc định mọi đoạn mã do AI tạo ra đều chính xác. Cần chạy thử website và kiểm tra các chức năng thực tế.
- **Hiểu mã nguồn do AI tạo:** AI chỉ là công cụ hỗ trợ. Sinh viên cần hiểu cách hoạt động của HTML và CSS để có thể chỉnh sửa, bảo trì và phát triển website.

### 3.3. Kết luận

Vibe Coding giúp em tiếp cận quá trình phát triển website theo hướng nhanh chóng và trực quan hơn. Thông qua việc xây dựng VYBE, em học được cách chuyển yêu cầu thành prompt, sử dụng kết quả do AI đề xuất và tiếp tục tinh chỉnh để hoàn thiện sản phẩm.

Bài học quan trọng nhất của em là chất lượng đầu ra phụ thuộc nhiều vào cách đặt câu hỏi và khả năng đánh giá kết quả. AI có thể hỗ trợ viết mã nhanh, nhưng người phát triển vẫn phải chịu trách nhiệm kiểm tra tính chính xác, khả năng sử dụng và chất lượng của website.
