# Template — Evidence Pack

Nộp kèm thin SPEC cuối Day 05.

## 1. Nhóm và track

**Tên nhóm:** Nhóm 6 thành viên (Đoàn Minh Quang, Trường Thành Thảo, Nguyễn Công Tuấn Anh, Nguyễn Công Thành, Nguyễn Tuấn Minh, Võ Thành Hiệp).  
**Track:** Food delivery - decision support.  
**Product/app đã chọn:** ShopeeFood / GrabFood workflow.  
**Build slice đang nghĩ:** AI tạo 3 món phù hợp trong 1 lần mở app, augment việc chọn món bằng cách xếp hạng và gợi ý theo giờ ăn, ngân sách, lịch sử và khoảng cách giao, kèm theo lý do và nút hành động nhằm tối ưu hóa quyết định.  

## 2. Self-use evidence

Nhóm tự dùng app/workflow và ghi lại điểm gãy.

| Observation | Screenshot/link | Path liên quan | Điều học được |
|---|---|---|---|
| Mở app giờ trưa, user phải chọn giữa vô vàn quán gần, món quen, món đang giảm giá, rating, phí ship và thời gian giao. | Chụp màn hình danh sách home/search trong app trước checkpoint M1 Day 06. | Low-confidence | Nếu AI không chắc, nên hỏi 1 câu phân biệt chính: "Bạn muốn ăn nhẹ, no, hay tiết kiệm?". |
| User thường lướt nhiều rồi quay lại món quen (cơm tấm/bún bò) dù ban đầu muốn đổi món, tốn khoảng 5-10 phút cân nhắc. | Self-use note của nhóm. | Correction | Shortlist phải cân bằng món quen và món đổi vị, tránh chỉ lặp lại hoàn toàn lịch sử order. |
| Một gợi ý sai khẩu vị (quá cay, quá xa, vượt ngân sách) có thể làm user mất niềm tin và lập tức quay lại tự lướt. | Observation thực tế từ hành vi tự dùng của thành viên. | Failure | Cần nút phản hồi nhanh: "Không cay", "Rẻ hơn", "Gần hơn", "Đổi món" để ứng biến. |

## 3. User / review / social evidence

Nguồn có thể là review App Store/Play, group, comment, phỏng vấn nhanh, hoặc nguồn public khác.

| Quote / review / observation | Nguồn | User là ai? | Pain/failure mode |
|---|---|---|---|
| "Không biết ăn gì" là câu nói phổ biến nhất khi user mở app nhưng chưa định hình rõ preference[cite: 2]. | Observation thực tế trong nhóm và lớp học[cite: 2]. | Sinh viên, nhân viên văn phòng[cite: 2]. | Preference uncertainty, dễ mất thời gian lướt lâu hoặc chọn đại rồi hối hận[cite: 2]. |
| Food delivery apps dễ khiến sinh viên rơi vào trạng thái quá tải vì có quá nhiều nhà hàng, món ăn, review đi kèm rating[cite: 2]. | Nghiên cứu public về sinh viên và food delivery apps (Arohi & Dayal, 2024)[cite: 2]. | Sinh viên tại các khu vực đô thị[cite: 2]. | Information overload, gánh nặng nhận thức (cognitive strain)[cite: 2]. |
| Choice overload biểu hiện mạnh mẽ hơn khi nhiệm vụ khó, lựa chọn phức tạp, user không chắc chắn về sở thích và muốn giảm bớt effort[cite: 2]. | Nghiên cứu Chernev, Bockenholt & Goodman, 2015[cite: 2]. | Người dùng đang đói, vội và chưa biết rõ mình muốn gì[cite: 2]. | Quá tải lựa chọn dẫn tới tê liệt quyết định (decision paralysis)[cite: 2]. |
