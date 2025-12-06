# Mẫu báo cáo LaTeX - Overleaf

## 1. Giới thiệu

Mẫu báo cáo LaTeX tiếng Việt, hỗ trợ công thức toàn và tô màu code.

## 2. Yêu cầu và tương thích

Yêu cầu sử dụng pdfLatex compiler và bật sẵn shell-escape cho minted

> Overleaf đã có sẵn, có thể dùng trực tiếp.

## 3. Cấu trúc thư mục chính

- `main.tex`: ghép toàn bộ tài liệu, gọi các `\input` chương/phụ lục.
- `config/`:
  - `info.tex`: các thông tin được hiển thị trên trang bìa
  - `titlepage.tex`: trang bìa,
  - `packages.tex`: danh sách các gói được sử dụng,
  - `settings.tex`: thiết lập khổ giấy, lề, giãn dòng, đánh số,...
- `chapters/`: nội dung các chương
- `appendix/`: nội dung phụ lục
- `reference/references.bib`: danh mục tài liệu tham khảo
- `images/`: chứa các hình ảnh được sử dụng trong báo cáo

## 4. Tùy chỉnh thông tin

- Cập nhật thông tin trong `config/info.tex` (trường, tên đề tài, nhóm, giảng viên, sinh viên,...).
- Đổi bố cục bìa (nếu cần): chỉnh trong `config/titlepage.tex`.
- Thay đổi lề/giãn dòng/đánh số: chỉnh trong `config/settings.tex`.
- Thêm/bớt gói: `config/packages.tex` (giữ minted nếu cần tô màu code).

## 5. Thêm và quản lý nội dung

- Chương chính: viết ở `chapters/*.tex`; thêm/bớt chương bằng cách chỉnh danh sách `\input` trong `main.tex`.
- Phụ lục: đặt sau lệnh `\appendix` trong `main.tex`, nội dung trong `appendix/*.tex`.
- Hình ảnh: lưu vào `images/`, chèn với `\includegraphics`.
- Bảng/code: tham khảo ví dụ sẵn trong các file chương và phụ lục.

## 6. Tài liệu tham khảo

- Thêm mục BibTeX vào `reference/references.bib`.
- Trích dẫn trong nội dung bằng `\cite{key}`; danh mục tham khảo hiển thị tự động khi có trích dẫn.

## 7. Lưu ý khi không dùng Overleaf

- Bật `-shell-escape` cho pdfLaTeX để minted hoạt động.
- Giữ mã nguồn ở UTF-8; dùng babel tiếng Việt và fontenc T1 (đã cấu hình sẵn trong `config/packages.tex`).
- Nếu gặp lỗi minted: kiểm tra Python/Pygments trong hệ LaTeX hoặc tạm thời đổi sang môi trường code khác nếu không bật được shell-escape.
