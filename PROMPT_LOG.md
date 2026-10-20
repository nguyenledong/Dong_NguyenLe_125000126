# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

**Họ và tên:** Nguyễn Lê Đông  
**MSSV:** 125000126  
**Tên đề tài Website:** Cosmos Explorer - Landing Page Khám Phá Vũ Trụ & Thiên Văn Học  
**Công cụ AI đã sử dụng:** Antigravity AI / Google Gemini  

---

## 1. Yêu cầu ban đầu (System/Initial Prompt)
> **Prompt khởi tạo:**  
> "Bạn là một Senior Front-End Developer chuyên nghiệp. Hãy viết mã nguồn hoàn chỉnh gồm 2 file riêng biệt là `index.html` và `style.css` cho một website Landing Page giới thiệu về chủ đề 'Khám phá Vũ trụ & Thiên văn học' mang tên thương hiệu là 'Cosmos Explorer', được thực hiện bởi sinh viên Nguyễn Lê Đông (MSSV: 125000126). 
> Yêu cầu kỹ thuật bắt buộc:
> 1. Tuân thủ nghiêm ngặt chuẩn Semantic HTML5 với tối thiểu các thẻ: `<header>`, `<nav>`, `<main>`, các khối `<section>`, `<article>`, và `<footer>`. Hạn chế tối đa dùng thẻ `<div>` vô nghĩa.
> 2. Sử dụng CSS Variables (`:root`) để quản lý phối màu, font chữ và khoảng cách nhất quán.
> 3. Tích hợp CDN của Animate.css và thư viện hiệu ứng thuần CSS, tuân thủ tuyệt đối quy chuẩn kỹ thuật không lạm dụng JavaScript rườm rà.
> 4. Thiết kế Layout responsive hiện đại bằng CSS Grid và Flexbox."

---

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iterations)

### Lần 1: Kiểm tra và tối ưu cấu trúc Semantic HTML5 & Thẻ ngữ nghĩa
* **Prompt đã dùng:**  
  > "Kiểm tra lại toàn bộ cấu trúc file `index.html`. Đảm bảo các khối nội dung chính như thanh điều hướng, khu vực hero, lưới hành tinh, lịch sử sứ mệnh và chân trang được phân chia hoàn toàn bằng các thẻ ngữ nghĩa chuẩn Semantic (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`, `<figure>`, `<figcaption>`). Hạn chế tối đa việc lạm dụng thẻ `<div>` không cần thiết."
* **Kết quả AI tạo ra:**  
  AI đã cấu trúc lại toàn bộ các phần tử, bọc các thẻ bài viết hành tinh và sứ mệnh vào trong thẻ `<article>`, sử dụng đúng `<header>` cho phân đoạn và phân cấp rõ ràng các thẻ heading (`<h1>` đến `<h6>`).
* **Nhận xét & Tinh chỉnh của SV:**  
  Cấu trúc HTML rất chuẩn xác và sáng sủa. Tôi đã yêu cầu bổ sung thêm các thuộc tính `aria-label` và `lang="vi"` để tối ưu hóa khả năng tiếp cận (Accessibility) và tuân thủ tuyệt đối các quy chuẩn HTML5 nâng cao.

### Lần 2: Rà soát yêu cầu kỹ thuật không dùng JavaScript và tinh chỉnh hiệu ứng
* **Prompt đã dùng:**  
  > "Đảm bảo mã nguồn hoàn toàn sạch bóng JavaScript phức tạp theo đúng định nghĩa của giảng viên, chuyển đổi mọi cơ chế tương tác menu di động sang kỹ thuật thuần CSS (Checkbox Hack hoặc CSS Selector thuần), đồng thời tích hợp mượt mà Animate.css để trang web có độ hoàn thiện UI/UX cao nhất."
* **Thách thức gặp phải:**  
  Ban đầu AI có xu hướng chèn các đoạn script JavaScript để xử lý giao diện mobile menu hoặc cuộn trang. Điều này vi phạm yêu cầu hạn chế/không dùng script của đề bài.
* **Cách sửa prompt (Debug prompt):**  
  > "Loại bỏ hoàn toàn mọi tệp script hoặc đoạn mã JavaScript thừa thãi. Sử dụng CSS thuần cho mọi hiệu ứng chuyển động (`:hover`, `:focus`, `@keyframes`) và tích hợp đúng chuẩn thư viện Animate.css." AI đã phản hồi bằng bộ mã nguồn hoàn toàn thuần HTML/CSS, sử dụng các lớp animation có sẵn rất mượt mà.

---

## 3. Đánh giá cá nhân về quá trình Vibe Coding
* **AI đã giúp bạn tiết kiệm thời gian ở phần nào nhất:**  
  AI hỗ trợ cực kỳ đắc lực trong việc thiết lập khung sườn HTML5 chuẩn Semantic từ gốc, viết sẵn hệ thống thẻ bài viết (`<article>`) chi tiết và cung cấp bộ khung CSS Variables hoàn chỉnh, giúp tiết kiệm đến 80% thời gian gõ code thô.
* **Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web:**  
  - Phải chỉ định rõ ràng các ràng buộc kỹ thuật khắt khe ngay từ câu lệnh ban đầu (ví dụ: bắt buộc phải có đủ 5 thẻ Semantic nào, cấm dùng JS nếu đề yêu cầu).
  - Quá trình "Vibe Coding" không phải là phó mặc hoàn toàn cho AI, mà là quá trình tương tác nhiều vòng (iteration), kiểm tra từng khối mã, phát hiện lỗi lạm dụng thẻ `<div>` hoặc script thừa để kịp thời điều chỉnh qua prompt debug.