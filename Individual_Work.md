# Industry Risk Snapshot: Media / News / Social / Political Assistant

| Câu hỏi | Low / Medium / High / Critical | Vì sao? |
| :--- | :--- | :--- |
| Nếu AI sai, có thể gây hại thể chất không? | High | Có thể. Báo chí thường đưa tin về y tế, thiên tai, tình huống khẩn cấp. Nếu AI đưa tin sai (ví dụ: sai đường sơ tán bão, sai hướng dẫn y tế), người đọc làm theo có thể gặp nguy hiểm trực tiếp đến tính mạng. |
| AI có ảnh hưởng đến quyết định hệ trọng không? | High | Báo chí định hướng dư luận. Thông tin sai có thể ảnh hưởng đến quyết định đầu tư tài chính, y tế, hoặc bỏ phiếu bầu cử. |
| Hệ thống có động tới dữ liệu nhạy cảm không? | Medium | Thường là gián tiếp/không sâu. Có thể dùng thông tin cá nhân, nguồn tin nội bộ, hoặc chạm đến dữ liệu sức khỏe, tài chính, danh tính khi viết tin, nhưng không cốt lõi như hệ thống Y tế hay Nhân sự. |
| Nếu sai, hậu quả có khó đảo ngược không? | High | Tin giả (fake news) lan truyền với tốc độ chóng mặt. Dù có đính chính, thiệt hại về uy tín và ấn tượng ban đầu rất khó để xóa bỏ hoàn toàn. |
| Nếu triển khai rộng, blast radius có lớn không? | Critical | Cực kỳ lớn. Một bài báo sai lệch hoặc một deepfake trên mạng xã hội có thể tiếp cận hàng triệu người trong vài giờ. |
| Có cần human review hoặc escalation không? | Critical | Quy trình xuất bản (editorial process) bắt buộc phải có con người kiểm duyệt (human-in-the-loop) để đảm bảo tính xác thực, đạo đức và tránh kiện tụng. |
| **Risk profile tổng thể của ngành** | **High** | Ngành News có risk profile tổng thể ở mức High vì AI có thể tạo ra sai lệch thông tin trên diện rộng, làm xói mòn niềm tin công chúng và gây thiệt hại uy tín, pháp lý hoặc tài chính cho tòa soạn. Rủi ro này không phải lúc nào cũng gây hại thể chất trực tiếp, nhưng tác động lan truyền của tin sai, deepfake, và tóm tắt lỗi có thể rất lớn và khó khắc phục sau khi đã xuất bản. |


---

# Brief Case 1: Apple tạm ngưng tính năng tóm tắt tin bằng AI

| Field | Bạn điền gì |
| :--- | :--- |
| Tên case | Apple AI tạo tiêu đề và tóm tắt tin tức giả mạo |
| Ngành | Media / news / social / political assistant |
| Tổ chức / sản phẩm | Apple (Tính năng tóm tắt tin tức bằng Apple Intelligence) |
| Use case AI | AI được dùng để tự động tóm tắt các bài báo và tạo tiêu đề ngắn gọn cho người dùng đọc nhanh trên hệ sinh thái của Apple. |
| Thời điểm | Tháng 1 năm 2025 |
| Case xảy ra chuyện gì? | Tính năng AI của Apple đã tạo ra hàng loạt tiêu đề giả mạo nghiêm trọng, ví dụ như bịa chuyện Luigi Mangione tự sát, "Benjamin Netanyahu bị bắt giữ" hay "Pete Hegseth bị sa thải". Apple đã bị đài BBC khiếu nại và phải tạm dừng tính năng này vì làm bóp méo nội dung của các báo lớn như NYT, Washington Post. |
| Stakeholder bị ảnh hưởng | Người dùng Apple đọc tin tức, Uy tín của các cá nhân bị đưa tin sai, Các tòa soạn báo (BBC, NYT) bị AI bóp méo nội dung. |
| Số liệu chính | Mặc dù không có con số chính xác số người đọc, Apple đã phải **ngay lập tức tạm dừng** tính năng tóm tắt tin tức trên phạm vi toàn cầu chỉ sau một thời gian ngắn ra mắt do áp lực từ các tòa soạn. |
| Trích nguồn ngắn | Đầu năm 2025, Apple buộc phải tạm ngưng tính năng tóm tắt tin tức bằng AI sau khi bị phát hiện liên tục tạo ra các tiêu đề giả mạo nghiêm trọng về các nhân vật công chúng (CBC, 2025). |
| Nguồn 1 | Báo chí thời sự quốc tế (01/2025) - [Apple pauses AI news summaries after fake headlines] |
| Ghi chú độ tin cậy | High-quality secondary source. |


---

# Harm Map 1: Apple AI News Summary Errors

| High-risk moment | Stakeholder bị ảnh hưởng | Failure mode | Layer bắt đầu lỗi | Harm xảy ra là gì? | Harm lens | Severity | Scale | Probability | Frequency | Vì sao? |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| AI tự động tóm tắt sai lệch hoàn toàn nội dung bài báo gốc và hiển thị thành notification/headline trên hàng triệu thiết bị. | Độc giả, Báo chí gốc, Người bị đưa tin | Hallucination | Model (Lỗi tóm tắt) / UX (Thiết kế hiển thị trực tiếp không qua xác minh) | Người dùng tiếp nhận tin tức sai lệch hoàn toàn; Uy tín của báo gốc bị ảnh hưởng vì người dùng tưởng báo viết sai. | Misinformation / Dignity loss | High | High | Medium | Medium | **Severity High**: Tin giả về bắt giữ/sa thải chính trị gia có thể gây hoang mang dư luận. **Scale High**: Apple có hàng trăm triệu thiết bị. **Probability Medium**: Tùy thuộc vào độ dài và độ phức tạp của bài báo gốc. **Frequency Medium**: Thỉnh thoảng xảy ra với các bài báo có nhiều chi tiết dễ nhầm lẫn. |


---

# Brief Case 2: Trích dẫn giả do AI trong nghiên cứu Y sinh học

| Field | Bạn điền gì |
| :--- | :--- |
| Tên case | Hàng ngàn trích dẫn giả do AI tạo ra trong các bài báo khoa học |
| Ngành | Media / news / social / political assistant (Ảnh hưởng trực tiếp đến nguồn tin của nhà báo khoa học/y tế) |
| Tổ chức / sản phẩm | Các tác giả nghiên cứu / Các công cụ Generative AI (LLMs) |
| Use case AI | Các nhà nghiên cứu sử dụng AI để hỗ trợ viết bài và tổng hợp tài liệu tham khảo cho các bài báo khoa học. |
| Thời điểm | Tháng 5 - 6 năm 2026 |
| Case xảy ra chuyện gì? | Một nghiên cứu (ví dụ đăng trên The Lancet) phát hiện hàng ngàn tài liệu tham khảo hoàn toàn không có thật (do AI bịa ra) nằm rải rác trong hàng ngàn bài báo y sinh học. Việc này cực kỳ nguy hiểm vì các tòa soạn báo chí thường dùng các nghiên cứu này làm nguồn đầu vào để viết tin tức, vô tình lan truyền thông tin y tế sai lệch đến công chúng. |
| Stakeholder bị ảnh hưởng | Nhà báo khoa học, Độc giả đọc tin y tế, Bệnh nhân. |
| Số liệu chính | Phát hiện hơn **4.000 trích dẫn giả** trong **2.810 bài báo y sinh học**, với một số bài có tới 60% trích dẫn là giả. |
| Trích nguồn ngắn | Một kiểm toán công bố giữa năm 2026 cho thấy AI đã tạo ra hơn 4.000 trích dẫn y khoa giả mạo trong gần 3.000 bài báo học thuật, đe dọa nghiêm trọng đến tính xác thực của các nguồn tin y tế. |
| Nguồn 1 | Các báo cáo nghiên cứu kiểm toán khoa học (06/2026). |
| Ghi chú độ tin cậy | Primary source (nghiên cứu kiểm toán trực tiếp). |


---

# Harm Map 2: Fake Citations in Biomedical Papers

| High-risk moment | Stakeholder bị ảnh hưởng | Failure mode | Layer bắt đầu lỗi | Harm xảy ra là gì? | Harm lens | Severity | Scale | Probability | Frequency | Vì sao? |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Các nhà báo y tế trích dẫn lại các bài báo khoa học chứa dữ liệu/nguồn tham khảo giả do AI sinh ra. | Báo chí, Bệnh nhân, Bác sĩ | Hallucination / Over-reliance | Model / Grounding (Dữ liệu đầu vào sai) | Báo chí vô tình phát tán tin giả về y tế; Bệnh nhân có thể áp dụng các phương pháp điều trị sai lầm. | Misinformation / Injury (tiềm năng) | Critical | Medium | High | High | **Severity Critical**: Thông tin y tế sai có thể trực tiếp đe dọa tính mạng (Injury). **Scale Medium**: Phụ thuộc vào mức độ viral của bài báo. **Probability High**: LLM rất dễ sinh ra trích dẫn trông giống thật nhưng không tồn tại. **Frequency High**: Tỉ lệ cao (hàng ngàn bài báo dính lỗi). |


---

# Brief Case 3: Mạng lưới AI tạo tin giả để câu view (BeeUp)

| Field | Bạn điền gì |
| :--- | :--- |
| Tên case | BeeUp vận hành mạng lưới trang Facebook giả mạo bằng AI |
| Ngành | Media / news / social / political assistant |
| Tổ chức / sản phẩm | Công ty marketing BeeUp / Các công cụ AI tạo nội dung và hình ảnh |
| Use case AI | AI được sử dụng ở quy mô công nghiệp để tạo ra các câu chuyện giật gân, bóp méo tin thật và tạo hình ảnh giả mạo nhằm thu hút tương tác (câu view) trên Facebook để kiếm tiền quảng cáo. |
| Thời điểm | Tháng 8/2025 - Tháng 3/2026 |
| Case xảy ra chuyện gì? | BeeUp bị phát hiện điều hành một mạng lưới khổng lồ dùng AI tạo nội dung giả (fake news, deepfake người nổi tiếng) để kéo traffic. Sau khi bị chú ý, chúng chuyển từ "bịa hoàn toàn" sang "bóp méo tin thật". Mạng lưới này dùng hơn 150 trang Facebook để kích động người dùng bấm vào link. |
| Stakeholder bị ảnh hưởng | Người dùng mạng xã hội, Nền tảng Facebook (Meta), Những người nổi tiếng bị giả mạo. |
| Số liệu chính | Mạng lưới này vận hành hàng loạt trang Facebook (với đợt mới nhất là **hơn 150 trang tạo tin giả trực tiếp**) và tiếp cận hàng chục triệu người theo dõi. |
| Trích nguồn ngắn | Đầu năm 2026, các cuộc điều tra đã phanh phui mạng lưới của công ty BeeUp vận hành hàng ngàn trang Facebook sử dụng AI để sản xuất tin giả và hình ảnh bóp méo quy mô lớn nhằm trục lợi quảng cáo. |
| Nguồn 1 | Báo chí điều tra (2026) - Báo cáo về mạng lưới content farm của BeeUp sử dụng AI. |
| Ghi chú độ tin cậy | High-quality secondary source. |


---

# Harm Map 3: BeeUp AI Fake News Network

| High-risk moment | Stakeholder bị ảnh hưởng | Failure mode | Layer bắt đầu lỗi | Harm xảy ra là gì? | Harm lens | Severity | Scale | Probability | Frequency | Vì sao? |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Kẻ xấu sử dụng AI để tự động hóa việc tạo và phát tán tin giả/hình ảnh bóp méo trên hàng trăm fanpage cùng lúc. | Người dùng MXH, Người nổi tiếng | Misuse / Sycophancy (Kích động cảm xúc) | UX / System (Hệ thống content farm) | Bầu không khí thông tin bị ô nhiễm nặng nề; Người dân bị thao túng tâm lý; Lừa đảo chiếm đoạt tài sản. | Misinformation / Dignity loss | High | Critical | Low (Do con người cố ý, không phải lỗi hệ thống) | High | **Severity High**: Thao túng tâm lý và bóp méo sự thật nghiêm trọng. **Scale Critical**: Tiếp cận hàng triệu người qua MXH. **Probability Low**: Đây là hành vi có chủ đích (Misuse) chứ không phải lỗi ngẫu nhiên. **Frequency High**: Máy móc sinh ra hàng ngàn bài viết mỗi ngày. |
