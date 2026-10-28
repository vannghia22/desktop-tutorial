# Vay — bản dựng hình và âm thanh

Nguồn: Vay.MOV, GitHub Release vaykthamdinh, vannghia22/desktop-tutorial.

Bản dựng giữ toàn bộ lời thoại và tốc độ gốc, có punch zoom 104–112%, headline biên tập trung tính, CTA cuối, nhạc nền tổng hợp gốc có ducking, làm sạch nhẹ và cân bằng giọng. Xuất H.264 1080×1920 60fps.

## Giới hạn quan trọng
Không có transcript, phụ đề, bleep đồng bộ hoặc infographic theo lời thoại: model tiếng Việt bị chính sách mạng từ chối tải. Không xác nhận nội dung tài chính trong lời nói. Không coi đây là bản đã được duyệt chạy quảng cáo.

## Trước khi chạy quảng cáo
Cần đối chiếu toàn bộ lời thoại với thông tin thật của đơn vị cung cấp dịch vụ; xác minh tư cách/giấy phép và quyền quảng cáo, điều kiện sản phẩm, lãi suất, tổng phí, kỳ hạn, tiêu chí đối tượng và mọi cam kết xét duyệt. Kiểm tra yêu cầu hiện hành tại Việt Nam trên TikTok Ads và Meta Ads; các yêu cầu này chưa được kiểm chứng từ nguồn chính thức trong phiên làm việc này. Che chữ hoặc bleep không làm nội dung tự động tuân thủ.

## Chỉnh sửa và xuất lại
Yêu cầu Node.js 22+, FFmpeg, Chromium. Giải nén project và chạy:

    npm run dev
    npm run check
    HYPERFRAMES_BROWSER_PATH=/usr/bin/chromium npm run render -- --fps 60 --quality high --workers 2

index.html là composition HTML/CSS/GSAP. footage.mp4 là nguồn hình đã xử lý, mixed.wav là âm thanh đã mix, make_music.py tái tạo nhạc nền. Giữ các file cạnh nhau. Thay đường dẫn trình duyệt nếu dùng Windows/macOS.
