# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

- **Họ và tên:** Nguyễn Nhật Tân
- **MSSV:** 125001661
- **Lớp:** 25CT113
- **Tên đề tài Website:** VYBE - Nền Tảng Nghe Nhạc Trực Tuyến Đẳng Cấp (Spotify & Apple Music Aesthetic, 100% Pure HTML5 & CSS3)
- **Công cụ AI đã sử dụng:** Google Antigravity (Gemini Advanced Agentic Coding)

---


## 1. Yêu cầu ban đầu (System / Initial Prompt)

> **Prompt tổng quan khởi tạo:**
> *"Bạn là một kỹ sư lập trình web bằng AI. Hãy tạo một website nghe nhạc hiện đại tên VYBE, giao diện cao cấp với tông màu đen, xám và tím neon, thiết kế như Spotify kết hợp Apple Music nhưng có phong cách riêng. Yêu cầu giao diện:
> - Trang chủ có nhạc nổi bật, bài hát thịnh hành, album và playlist.
> - Thanh tìm kiếm bài hát, ca sĩ, album.
> - Trình phát nhạc cố định phía dưới màn hình (Bottom Player Bar).
> - Có nút phát, tạm dừng, chuyển bài, tua nhạc, chỉnh âm lượng, phát ngẫu nhiên và lặp lại.
> - Có lời bài hát (Synced Lyrics), danh sách phát, yêu thích và lịch sử nghe nhạc.
> - Hiệu ứng chuyển động mượt mà, ảnh album đẹp, giao diện tối sang trọng.
> - Tương thích hoàn hảo với điện thoại, máy tính bảng và máy tính.
> - Sử dụng HTML, CSS với mã nguồn rõ ràng, chuẩn SEO."*

---

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iteration Iterations)

### Lần 1: Dựng khung Semantic HTML5 & Hệ thống CSS Variables
- **Prompt đã dùng:**
  > *"Hãy thiết kế lại toàn bộ cấu trúc mã nguồn theo chuẩn Semantic HTML5, sử dụng các thẻ `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`. Khai báo bảng CSS Variables đầy đủ cho màu nền Darkest (`#07070a`), màu bề mặt kính mờ Glassmorphism, dải màu tím Neon (`#8b5cf6` đến `#d946ef`), kích thước typography và hiệu ứng đổ bóng Neon Glow."*
- **Kết quả AI tạo ra:**
  - AI khởi tạo file `index.html` và `css/styles.css` với đầy đủ `:root` CSS custom properties.
  - Phân chia bố cục Sidebar bên trái, Header cố định với thanh tìm kiếm và Main Content dạng Scroll mượt mà.
- **Nhận xét & Tinh chỉnh của SV:**
  - AI ban đầu vẫn còn dùng nhiều thẻ `<div>` lồng nhau ở các mục danh sách bài hát.
  - Đã nhắc AI chuyển các nhóm nội dung thành `<section class="view-section">`, thanh điều hướng thành `<nav class="sidebar">` và danh sách playlist thành các phần tử ngữ nghĩa chuẩn.

---

### Lần 2: Tối ưu 100% Pure HTML5 & CSS3 thuần (Loại bỏ hoàn toàn JavaScript)
- **Prompt đã dùng:**
  > *"Xóa bỏ toàn bộ file JavaScript trong dự án. Chỉ được dùng mỗi HTML và CSS thuần thôi. Hãy áp dụng kỹ thuật Radio Hack và Checkbox Hack để chuyển đổi giữa các View (SPA Routing), đóng/mở Modal, bật/tắt Lời bài hát, và dùng trình phát `<audio controls>` native của HTML5."*
- **Thách thức gặp phải:**
  - Trình duyệt thông thường nếu không có JavaScript sẽ không chuyển đổi trang (Tab) được và không phát được âm thanh nếu dùng nút bấm giả lập.
- **Cách sửa prompt (Debug prompt):**
  > *"Đặt các thẻ `<input type="radio" name="view-tab" id="tab-home">` ở đầu `<body>`. Sau đó dùng CSS Sibling Selector `#tab-home:checked ~ .app-container .main-content #view-home { display: block; }` để hiển thị trang tương ứng. Đối với âm thanh, nhúng thẻ `<audio controls preload="none">` với các link mp3 trực tiếp từ SoundHelix, Internet Archive và Wikimedia Commons để người dùng bấm nghe được nhạc thật 100%."*
- **Kết quả:**
  - Xóa sạch toàn bộ thư mục `js/` và thẻ `<script>`. Website hoạt động hoàn hảo 100% bằng CSS3 thuần.

---

### Lần 3: Tích hợp Đăng nhập tài khoản & Mở rộng bài hát nổi tiếng
- **Prompt đã dùng:**
  > *"Làm thêm phần đăng nhập tài khoản và cho thêm đa dạng các bài hát nổi tiếng cả V-Pop lẫn Quốc tế."*
- **Kết quả AI tạo ra:**
  - Xây dựng Modal Đăng nhập / Đăng ký dạng Pop-up kính mờ cao cấp với Google & Apple Sign-In.
  - Thêm trang Tài khoản VIP (`#view-profile`) với thông tin thành viên Premier, huy hiệu Hi-Res Audio 24-bit/96kHz, thống kê giờ nghe và cài đặt âm thanh vòm Dolby Atmos.
  - Bổ sung các bản hit thịnh hành: *Blinding Lights (The Weeknd)*, *See Tình (Hoàng Thùy Linh)*, *Nơi Này Có Anh (Sơn Tùng M-TP)*, *Shape of You (Ed Sheeran)*, *Faded (Alan Walker)*, *Canon in D (Pachelbel)*...

---

### Lần 4: Xây dựng Danh mục thể loại & Bộ lọc Genre Pills
- **Prompt đã dùng:**
  > *"Thêm các bài hát vào các danh mục thể loại này: Synthwave & Cyber, Lo-Fi & Chill, Acoustic & Coffee, EDM & Rave và Cổ điển theo đúng hình ảnh giao diện."*
- **Thách thức gặp phải:**
  - Số lượng bài hát ban đầu trong mỗi thể loại còn ít, chưa đủ để làm nổi bật tính năng lọc khi click vào các Pill Thể loại (`Lo-Fi Chill`, `Synthwave`, `Acoustic`,...).
- **Cách sửa prompt (Debug prompt):**
  > *"Bổ sung hơn 30 bài hát đa dạng kèm stream audio Lossless thật. Gắn class `genre-synth`, `genre-lofi`, `genre-acoustic`, `genre-electronic`, `genre-classical` vào từng bài hát. Viết CSS để khi chọn radio `#genre-lofi:checked`, Pill 'Lo-Fi Chill' phát sáng neon màu tím hồng rực rỡ và danh sách bài hát tự động ẩn các bài không thuộc thể loại đó bằng CSS `:not()`."*
- **Kết quả:**
  - Đạt độ chính xác 100% so với hình ảnh yêu cầu. Cả 5 thể loại đều có kho bài hát phong phú và các banner card gradient tuyệt đẹp.

---

### Lần 6: Nâng cấp Animation Load Trang Điện Ảnh & Hệ thống Background Chủ đề
- **Prompt đã dùng:**
  > *"Tạo cho tôi animation khi load trang web và thêm background phù hợp với chủ đề."*
- **Thách thức gặp phải:**
  - Cần tạo background đậm chất Spotify & Apple Music Luxury (Neon Violet, Cyber Dark, Glassmorphism) nhưng không làm nặng trang hay rối mắt nội dung bài hát.
  - Animation preloader cần có âm hưởng phòng thu âm thanh chất lượng cao (Hi-Res Audio).
- **Kết quả AI tạo ra:**
  - **Preloader Điện ảnh:** Tích hợp vòng sóng âm thanh lan tỏa (`.preloader-soundwaves`), vòng xoay kép Dual-Ring Spinner, thanh nạp tiến trình Gradient lấp lánh (`.preloader-progress-bar`) từ 0% đến 100% trong 1.7 giây.
  - **Hệ thống Background Chủ đề:** 4 vầng sáng cực quang Aurora Orbs chuyển động bồng bềnh (`floatAurora1` đến `floatAurora4`), kết hợp lưới tọa độ âm thanh acoustic (`.theme-grid-overlay`) và viền tối Vignette sang trọng. Các khối nội dung áp dụng hiệu ứng kính mờ để ánh sáng cực quang ẩn hiện phía sau cực kỳ cuốn hút.

---

## 3. Đánh giá cá nhân về quá trình Vibe Coding

### 1. AI đã giúp bạn tiết kiệm thời gian ở phần nào nhất?
- **Viết mã CSS phức tạp:** Việc tạo các bảng màu, hiệu ứng chuyển màu Linear Gradient, hiệu ứng kính mờ (Backdrop Filter Glassmorphism) và các Animation đĩa than xoay tròn, sóng nhạc Equalizer mất rất nhiều thời gian nếu viết thủ công. AI đã sinh mã chuẩn xác chỉ trong vài giây.
- **Tạo kho dữ liệu bài hát mẫu chất lượng:** AI nhanh chóng tổng hợp danh mục hơn 30 bài hát nổi tiếng kèm link ảnh Unsplash bản quyền miễn phí và nguồn âm thanh MP3 trực tiếp hoạt động ổn định.
- **Giải thuật Pure CSS thay thế JavaScript:** Kỹ thuật Sibling Selector (`~`) và `:checked` pseudo-class đòi hỏi tư duy phân cấp DOM chặt chẽ. AI đã tổ chức cấu trúc HTML hợp lý giúp toàn bộ ứng dụng hoạt động như một Single Page Application (SPA) thực thụ mà không có lỗi xung đột.

### 2. Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web?
- **Nguyên tắc "Đặc tả mục tiêu cụ thể (Be Specific)":** Thay vì nói *"hãy làm web đẹp hơn"*, hãy nói rõ *"sử dụng tông màu Đen `#07070a`, Tím Neon `#8b5cf6`, hiệu ứng Glassmorphism mờ 20px, bo góc 18px và bóng đổ Neon Glow"*.
- **Ràng buộc công nghệ rõ ràng (Strict Constraints):** Khi giảng viên yêu cầu không dùng JS, cần nhấn mạnh ngay trong prompt *"100% Pure HTML5 & CSS3 thuần, tuyệt đối không dùng thẻ `<script>` hay file `.js`"*.
- **Phương pháp Lặp & Tinh chỉnh từng bước (Iterative Refinement):** Không nên yêu cầu AI làm tất cả trong một lần duy nhất. Hãy chia nhỏ quá trình: Khởi tạo khung Semantic -> Thêm Design System -> Thêm tính năng tương tác -> Tối ưu UX/Animation.
- **Kiểm soát tính ngữ nghĩa (Semantic Integrity):** Luôn theo dõi đầu ra của AI để đảm bảo AI dùng đúng các thẻ ngữ nghĩa của HTML5 (`<header>`, `<nav>`, `<main>`, `<section>`), tránh để AI lạm dụng quá nhiều thẻ `<div>`.
