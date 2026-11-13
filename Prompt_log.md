# NHẬT KÝ TƯƠNG TÁC AI – TECHBUGS LANDING PAGE REFACTORING

**Bài tập:** Tái thiết Landing Page TechBugs  
**Dự án:** `techbugs-landing-page-refactoring`  
**Công cụ AI:** ChatGPT  
**Ngày:** 13/11/2026  

### Lượt 1 – Đặt tên thư mục dự án

**Prompt người học (nguyên văn):**

> ## [Bài tập] Tái thiết Landing Page TechBugs
>
> tạo tên folder cho project

**Lý do hỏi:** Chọn tên thư mục và repository theo quy ước `kebab-case`, dễ nhận diện khi nộp bài và quản lý bằng Git.

**Nội dung AI phản hồi:** Đề xuất `techbugs-landing-page-refactoring`; hướng dẫn dùng `mkdir`, `cd`, `git init`.

**Kiến thức rút ra:** Tên thư mục có thể phản ánh rõ tên sản phẩm và hoạt động refactoring; `git init` khởi tạo repository tại thư mục hiện hành.

### Lượt 2 – Phân tích toàn bộ yêu cầu bài tập

**Prompt người học (trích nội dung chính; prompt gốc rất dài):**

> ## [Bài tập] Tái thiết Landing Page TechBugs
>
> Mục tiêu: phân nhánh và hợp nhất Git; thay menu rời rạc bằng cấu trúc `<nav> > <ul> > <li> > <a>`; thay các khối `<div>` chính bằng `<header>`, `<main>`, `<section>`, `<article>`, `<footer>`.
>
> Quy trình: commit Legacy Code trên `main`; tạo hai nhánh `feature/nav-menu` và `feature/semantic-layout` độc lập từ `main`; hợp nhất, xử lý conflict nếu có; nộp GitHub repository, ảnh Git graph và `Prompt_log.md`.
>
> tạo README và tóm tắt đề bài vào đó

**Lý do hỏi:** Hệ thống hóa đề bài thành tài liệu README cho GitHub và đối chiếu các yêu cầu kỹ thuật, quy trình triển khai, sản phẩm cần nộp.

**Nội dung AI phản hồi:** Soạn README với giới thiệu, mục tiêu, bảng thẻ Semantic, ba nhánh Git, các bước triển khai, cấu trúc dự án, tiêu chí chấm điểm và yêu cầu nộp bài. Gợi ý commit tài liệu theo Conventional Commits.

**Kiến thức rút ra:** README giúp người đọc hiểu phạm vi bài tập và Git workflow; hai nhánh tính năng cần phát triển độc lập từ commit gốc.

### Lượt 3 – Chọn thẻ thay cho logo dạng `div`

**Prompt người học (nguyên văn):**

> `<div class="logo">TechBugs Solutions</div>` thay thế bằng thẻ semantic nào

**Lý do hỏi:** Hiểu ngữ nghĩa của phần tên thương hiệu trong header, tránh thay mọi `div` một cách máy móc.

**Nội dung AI phản hồi:** Có thể dùng `<p class="logo">` nếu chỉ hiển thị tên thương hiệu, hoặc `<a href="/" class="logo">` nếu logo dẫn về trang chủ; không cần dùng `<h1>` vì trang đã có tiêu đề chính riêng.

**Kiến thức rút ra:** Chọn thẻ HTML theo chức năng và ý nghĩa nội dung, không chỉ theo tên CSS class. Thẻ `<a>` có ý nghĩa liên kết, còn `<p>` đại diện một đoạn nội dung.

### Lượt 4 – Hủy thao tác Git merge gõ nhầm

**Prompt người học (nguyên văn):**

> xoa lenh merge go nhaam

**Lý do hỏi:** Tìm cách phục hồi trạng thái Git khi merge sai, hạn chế mất công sức và tránh ảnh hưởng lịch sử nhánh.

**Nội dung AI phản hồi:** Phân biệt ba tình huống:

- Merge đang dang dở: `git merge --abort`.
- Merge đã xong, chưa push: có thể trở về trạng thái trước merge bằng `git reset --hard ORIG_HEAD` **nhưng phải kiểm tra kỹ vì lệnh có thể mất thay đổi chưa commit**.
- Merge đã push: cân nhắc `git revert -m 1 <merge-commit-hash>` để giữ lịch sử.

AI yêu cầu kiểm tra `git status` và `git log --oneline --graph -5` trước khi chọn cách xử lý.

**Kiến thức rút ra:** Không có một lệnh hủy merge phù hợp mọi tình huống. Phải xác định merge đang dở, đã commit hay đã push và đánh giá rủi ro trước khi chạy lệnh.

### Lượt 5 – Yêu cầu ghi lại lịch sử trao đổi AI

**Prompt người học (nguyên văn):**

> Lưu lại toàn bộ đoạn chat với AI kèm giải thích ngắn gọn về lý do đặt câu hỏi.

**Lý do hỏi:** Hoàn thiện sản phẩm bắt buộc `Prompt_log.md`, minh bạch quá trình sử dụng AI và chứng minh mục đích học tập của từng lần đặt câu hỏi.

**Nội dung AI phản hồi:** Tạo nhật ký Markdown ghi nhận các prompt đã có, mục tiêu của prompt, nội dung tư vấn và bài học rút ra.

**Kiến thức rút ra:** Nhật ký nên ghi trung thực các tương tác thực tế; không tạo thêm prompt, câu trả lời hoặc thao tác Git giả.

