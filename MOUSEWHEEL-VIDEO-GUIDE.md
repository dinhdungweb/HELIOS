# Hướng dẫn sử dụng Video trong Mousewheel Collection

## Tính năng mới: Hỗ trợ Video Shopify

Section `mousewheel-collection` hiện đã hỗ trợ 3 loại video:

### 1. Video Shopify (Ưu tiên cao nhất)
- **Cách sử dụng**: Upload video trực tiếp qua Shopify Admin
- **Ưu điểm**: 
  - Tốc độ tải nhanh
  - Tự động tối ưu hóa
  - Có thumbnail mặc định
  - Hỗ trợ nhiều định dạng
- **Cách thiết lập**:
  1. Vào Theme Editor
  2. Chọn section "Mousewheel Collection"
  3. Thêm block "Video"
  4. Click vào "Video" và upload file từ máy tính
  5. Tùy chọn: Thêm ảnh bìa tùy chỉnh

### 2. Video YouTube/Vimeo (Fallback)
- **Cách sử dụng**: Dán link YouTube hoặc Vimeo
- **Khi nào sử dụng**: Khi không muốn upload video lên Shopify
- **Cách thiết lập**:
  1. Để trống trường "Video" 
  2. Dán link vào "Video URL (tùy chọn)"
  3. Thêm ảnh bìa nếu cần

### 3. Thứ tự ưu tiên
1. **Video Shopify** (nếu có) → Sẽ được hiển thị
2. **Video URL** (nếu không có video Shopify) → Sẽ được hiển thị
3. **Placeholder** (nếu không có gì) → Hiển thị icon video mặc định

## Cải tiến kỹ thuật

### Template mới
- File: `templates/collection.video-demo.json`
- Mục đích: Demo các loại video khác nhau

### CSS được cập nhật
- File: `assets/mousewheel-collection.css`
- Thêm style cho video Shopify
- Cải thiện hiển thị poster image

### JavaScript được tối ưu
- Hỗ trợ phát video Shopify
- Reset video về đầu khi chuyển slide
- Xử lý lỗi autoplay tốt hơn

## Hướng dẫn sử dụng

### Bước 1: Tạo Collection Template
1. Vào Admin → Online Store → Themes
2. Click "Customize" 
3. Chọn "Collection pages"
4. Tạo template mới hoặc chỉnh sửa template hiện có

### Bước 2: Thêm Section
1. Click "Add section"
2. Chọn "Mousewheel Collection"
3. Cấu hình chiều cao, pagination, navigation

### Bước 3: Thêm Content Blocks
1. Click "Add block"
2. Chọn "Video" hoặc "Image"
3. Upload nội dung và cấu hình text overlay

### Bước 4: Tối ưu hóa
- Sử dụng video có độ phân giải phù hợp (1920x1080 recommended)
- Đảm bảo video có thời lượng ngắn để tải nhanh
- Thêm ảnh bìa cho trải nghiệm tốt hơn

## Lưu ý quan trọng

1. **Autoplay**: Video sẽ tự động phát khi slide active (muted)
2. **Performance**: Video Shopify được tối ưu tự động
3. **Mobile**: Responsive design, hoạt động tốt trên mobile
4. **Accessibility**: Hỗ trợ keyboard navigation
5. **SEO**: Video có thể được index bởi search engines

## Troubleshooting

### Video không phát
- Kiểm tra định dạng video (MP4 recommended)
- Đảm bảo video không quá lớn (< 100MB)
- Kiểm tra browser có block autoplay không

### Video bị lag
- Giảm độ phân giải video
- Sử dụng video compression
- Kiểm tra kết nối internet

### Layout bị lỗi
- Kiểm tra CSS file đã được load
- Clear browser cache
- Kiểm tra responsive breakpoints