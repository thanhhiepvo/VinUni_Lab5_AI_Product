# Evidence Pack

Nộp kèm thin SPEC cuối Day 05.

*(Bản mẫu được điều chỉnh cho track Food Delivery - App ShopeeFood)*

## 1. Nhóm và track

**Tên nhóm:** Nhóm 1 (Tên nhóm của bạn)
**Track:** Food Delivery
**Product/app đã chọn:** ShopeeFood
**Build slice đang nghĩ:** AI Assistant "Hôm nay ăn gì" - Giúp user tìm món và gợi ý quán ăn dựa trên nhu cầu/ngữ cảnh bằng ngôn ngữ tự nhiên (VD: "đang mệt muốn ăn gì thanh đạm", "trời mưa thèm đồ nước cay cay").

## 2. Self-use evidence

Nhóm tự dùng app/workflow và ghi lại điểm gãy.

| Observation | Screenshot/link | Path liên quan | Điều học được |
|---|---|---|---|
| Mở app ShopeeFood lúc đói nhưng chưa biết ăn gì, lướt màn hình Home 10 phút qua các bộ sưu tập vẫn chưa chọn được món. | (tự chụp/giả định) | Failure | User bị "paradox of choice" (quá tải lựa chọn), tốn nhiều thời gian lướt mà không chốt được đơn. |
| Gõ thử "đồ ăn thanh đạm giải cảm" trên thanh search, kết quả trả về không chính xác hoặc rỗng. | (tự chụp/giả định) | Failure | Thanh tìm kiếm hiện tại chỉ match keyword tên quán/món, không hiểu được nhu cầu phức tạp hay ngữ cảnh tự nhiên. |

## 3. User / review / social evidence

Nguồn có thể là review App Store/Play, group, comment, phỏng vấn nhanh, hoặc nguồn public khác.

| Quote / review / observation | Nguồn | User là ai? | Pain/failure mode |
|---|---|---|---|
| "Ngày nào đến trưa cũng đau đầu với câu hỏi trưa nay ăn gì cùng đồng nghiệp, lướt app mỏi cả tay." | Phỏng vấn nhanh đồng nghiệp văn phòng | Nhân viên văn phòng, hay đặt đồ ăn trưa | Khó khăn, mất thời gian trong việc ra quyết định chọn món. |
| "Thèm ăn món gì đó rẻ rẻ tầm 30k mà ấm bụng nhưng giao diện toàn hiện các thương hiệu lớn hoặc đồ lạnh, tìm thủ công rất mệt." | Bình luận trên group review ShopeeFood | Học sinh sinh viên/người có ngân sách hạn hẹp | Không thể tìm quán kết hợp giữa ngân sách + tâm trạng (mood). |

Nếu chưa có nguồn ngoài nhóm, ghi rõ:
```text
(Nếu cần, bạn ghi vào đây: Nhóm sẽ kiểm chứng lại pain point bằng cách phỏng vấn 3 đồng nghiệp/bạn bè hay dùng ShopeeFood trước Day 06)
```

## 4. Competitor / analog evidence

| App / mô hình tham khảo | Họ xử lý task này thế nào? | Pattern học được | Có áp dụng trong 1 ngày không? |
|---|---|---|---|
| ChatGPT / Claude | Trả lời free-text, gợi ý tên các món ăn chung chung. | LLM hiểu context (trời mưa, ốm, thèm chua) rất tốt, nhưng lại không có action "Đặt hàng ngay". User vẫn phải copy tên món qua app food để search lại. | Có. Sẽ kết hợp khả năng hiểu context của AI với kho dữ liệu quán ăn thực tế của ShopeeFood. |
| Các bộ sưu tập (Collections) hiện có của app | Tạo sẵn playlist "Trời mưa ăn gì", "Món ngon giải nhiệt". | Bị tĩnh (static), không cá nhân hóa được theo đúng định mức giá hay khoảng cách của user lúc đó. | Không áp dụng trực tiếp, nhưng AI sẽ thay thế tính năng này bằng cách tạo "bộ sưu tập động" gồm 3 món. |

## 5. Evidence -> Insight

```text
Evidence nổi bật nhất:
User thường tốn quá nhiều thời gian để chốt món khi không có dự định từ trước, và thanh tìm kiếm hiện tại chỉ hoạt động hiệu quả khi user đã biết chính xác mình muốn ăn gì/ăn ở đâu.

Insight:
User không cần nhiều lựa chọn hơn (danh sách quán dài dằng dặc). Thật ra họ cần hỗ trợ thu hẹp lựa chọn (decision support) dựa trên tâm trạng, thời tiết, hoặc ngân sách hiện tại để giảm bớt gánh nặng tâm lý khi ra quyết định.

Opportunity:
AI có thể giúp bằng cách automate bước suy nghĩ "hôm nay ăn gì" thông qua một ô chat ngữ cảnh, đồng thời augment hành động đặt hàng bằng cách đưa ra đúng 2-3 lựa chọn phù hợp nhất kèm nút "Thêm vào giỏ hàng".
```

## 6. Evidence đổi SPEC như thế nào?

- [ ] Đổi user chính.
- [ ] Đổi pain statement.
- [x] Đổi build slice.
- [ ] Đổi Auto/Aug decision.
- [ ] Đổi 4 paths.
- [x] Đổi failure mode.
- [ ] Đổi owner/test plan.

Ghi rõ 1-2 thay đổi quan trọng:

```text
Trước evidence, nhóm định: 
Làm một thanh tìm kiếm AI đa năng tìm mọi thứ trên app.

Sau evidence, nhóm đổi thành: 
Thu hẹp lại thành một tính năng "Hôm nay ăn gì" dạng chat. User chỉ nhập câu mô tả (VD: "ăn gì cay cay dưới 50k"), AI trả về 3 món đáp ứng tiêu chí.

Lý do: 
Giúp build slice cực kỳ rõ ràng, xử lý trúng insight "lười ra quyết định".
Về Failure mode: Nếu AI gợi ý sai ý, user có path sửa sai (Correction) bằng cách bảo "Đổi món khác đi". Đặc biệt, thêm filter cứng cho các dị ứng (không để AI gợi ý hải sản cho người dị ứng hải sản) để chống rủi ro.
```
