# TechBugs Landing Page Refactoring

## 1. Giới thiệu

Dự án thực hành **Tái thiết Landing Page TechBugs** thuộc chương trình đào tạo CodeGym.

Mục tiêu là cải thiện cấu trúc HTML của trang giới thiệu dịch vụ TechBugs Solutions, chuyển đổi mã nguồn Legacy sử dụng nhiều thẻ `<div>` sang **Semantic HTML**, đồng thời thực hành quản lý mã nguồn bằng Git Branching và Merging.

## 2. Mục tiêu

- Sử dụng Git để quản lý phiên bản, tạo nhánh và hợp nhất mã nguồn.
- Xây dựng thanh điều hướng theo cấu trúc `<nav>`, `<ul>`, `<li>`, `<a>`.
- Thay thế các thẻ `<div>` bao bọc chính bằng Semantic HTML.
- Cải thiện cấu trúc trang web phục vụ SEO và Accessibility.
- Thực hành xử lý Merge Conflict.
- Kiểm tra lịch sử Git bằng Git Graph.

## 3. Yêu cầu kỹ thuật

### 3.1. Cấu trúc HTML

| Thành phần | Thẻ Semantic |
|---|---|
| Header | `<header>` |
| Navigation | `<nav>` |
| Menu | `<ul>`, `<li>`, `<a>` |
| Nội dung chính | `<main>` |
| Banner | `<section>` |
| Danh sách dịch vụ | `<section>` |
| Từng dịch vụ | `<article>` |
| Footer | `<footer>` |

### 3.2. Git Workflow

Dự án sử dụng 3 nhánh:

- `main`: Lưu trữ mã nguồn gốc và phiên bản hoàn chỉnh.
- `feature/nav-menu`: Nâng cấp cấu trúc thanh điều hướng.
- `feature/semantic-layout`: Chuyển đổi bố cục trang sang Semantic HTML.

Hai nhánh tính năng phải được tạo độc lập từ `main` trước khi tiến hành hợp nhất.

## 4. Quy trình thực hiện

### Bước 1: Phân tích

- Đọc và đánh giá Legacy Code.
- Xác định các thành phần cần chuyển đổi sang Semantic HTML.
- Lập kế hoạch phân chia công việc theo từng nhánh Git.

### Bước 2: Khởi tạo

- Khởi tạo Git Repository.
- Tạo file `index.html` chứa Legacy Code.
- Commit mã nguồn ban đầu trên nhánh `main`.

### Bước 3: Phát triển

**Nhánh `feature/nav-menu`**

- Chuyển đổi Menu thành cấu trúc `<nav> > <ul> > <li> > <a>`.
- Commit thay đổi độc lập.

**Nhánh `feature/semantic-layout`**

- Chuyển đổi các thành phần bố cục sang Semantic HTML.
- Không thay đổi cấu trúc Menu.
- Commit thay đổi độc lập.

### Bước 4: Hợp nhất và kiểm thử

- Merge lần lượt hai nhánh vào `main`.
- Xử lý Merge Conflict nếu phát sinh.
- Kiểm tra cấu trúc HTML sau khi hợp nhất.
- Xác minh lịch sử Git bằng lệnh:

```bash
git log --oneline --graph --all
```

## 5. Cấu trúc dự án

```text
techbugs-landing-page-refactoring/
├── index.html
├── README.md
└── Prompt_log.md
```

## 6. Tiêu chí đánh giá

| Tiêu chí | Tỷ trọng |
|---|---|
| Chất lượng HTML Semantic | 20% |
| Lịch sử Git và Merge | 20% |
| Bảo vệ mã nguồn và vấn đáp | 40% |
| Nhật ký Prompt AI | 20% |
| **Tổng cộng** | **100%** |

## 7. Sản phẩm nộp bài

1. GitHub Repository chứa mã nguồn hoàn chỉnh và lịch sử Git.
2. Screenshot Terminal hiển thị Git Graph.
3. File `Prompt_log.md` ghi lại quá trình tương tác với AI và mục đích của từng câu hỏi.

## 8. Công nghệ sử dụng

- HTML5
- Git
- GitHub
- Visual Studio Code

## 9. Ghi chú

Dự án tập trung vào kỹ năng **HTML Semantic** và **Git Workflow**. AI chỉ được sử dụng để giải thích kiến thức, tư vấn kỹ thuật và hỗ trợ xử lý lỗi, không thay thế học viên thực hiện toàn bộ mã nguồn.

---

**Bài tập:** Tái thiết Landing Page TechBugs  
**Đơn vị đào tạo:** CodeGym  
**Loại dự án:** HTML Basic Practice