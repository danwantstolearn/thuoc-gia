# 💊 Tra giá thuốc

Webapp so sánh giá thuốc giữa các nhà cung cấp (Long Châu, Pharmacity), theo từng đơn vị bán (Viên/Vỉ/Hộp...).

- Chạy 100% tĩnh trên GitHub Pages — gọi thẳng API public của các nhà cung cấp từ trình duyệt.
- `x` = không bán / không có giá công khai (thuốc kê đơn).
- Bản local (Flask + cache) nằm ở `gia-thuoc/` trong workspace, dùng chung file `index.html`.

## Deploy

Push lên `main` là GitHub Actions tự deploy. CNAME: `thuoc.nqhaidang.com` → DNS trỏ `CNAME thuoc → danwantstolearn.github.io`.

## Ghi chú

- Giá lấy trực tiếp từ web nhà cung cấp, có thể thay đổi theo thời điểm. Dùng cho mục đích tham khảo cá nhân.
- API: Pharmacity `api-gateway.pharmacity.vn/.../search/index?keyword=` (GET, CORS `*`), Long Châu `api.nhathuoclongchau.com.vn/lccus/search-product-service/api/products/ecom/product/search` (POST `{"keyword": "..."}`, CORS mở).
