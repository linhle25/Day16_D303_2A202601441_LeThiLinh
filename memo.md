# Memo Teardown — GOOGLE NOTEBOOKLM (GEMINI NOTEBOOK)

**Nhóm:** Product Teardown NOTEBOOKLM

**Thành viên:**

| STT | Họ và tên | Mã số sinh viên |
|---:|---|---|
| 1 | Nguyễn Thị Tuyết Mai | 2A202601693 |
| 2 | Trần Thị Vân Anh | 2A202601411 |
| 3 | Lê Thị Linh | 2A202601441 |

**Vì sao chọn sản phẩm này:** NotebookLM (nay là Gemini Notebook) đại diện cho bước chuyển dịch đột phá từ AI Chatbot đơn thuần sang "AI-first Knowledge & Learning Workspace", định hình lại cách con người biến dữ liệu thô thành tri thức chủ động qua đa định dạng (Text, Audio, Video, Flashcards & Interactive Practice).

---

## §1. Timeline các cập nhật lớn

| Thời điểm | Cập nhật | Context lúc đó | Nguyên lý |
|---|---|---|---|
| 05–07/2023 | **Project Tailwind → NotebookLM**: Google thử nghiệm AI-first notebook grounded trên nguồn do user cung cấp    | ChatGPT khiến chatbot AI bùng nổ, nhưng hallucination và thiếu context riêng của user vẫn là vấn đề. Google Labs thử hướng khác: để AI làm việc trực tiếp trên tài liệu user chọn. | **Wrapper → Moat**: Model có thể bị commoditize; context, source grounding và workflow riêng mới tạo giá trị khó bị model nền hấp thụ. ([Nguồn](https://blog.google/innovation-and-ai/technology/ai/notebooklm-google-ai/))                                                                     |
| 06/2024    | **Gemini 1.5 Pro + Global Expansion**: Hỗ trợ nhiều loại source hơn, multimodal, citations và mở rộng toàn cầu | Gemini 1.5 có long context mạnh hơn (1M tokens), cho phép xử lý lượng tài liệu lớn và đa dạng hơn. NotebookLM bắt đầu đi từ experiment → product có khả năng scale.                | **x10 Capacity**: Model mạnh hơn chỉ đáng giá khi mở được workflow trước đây khó làm — từ hỏi một tài liệu sang tổng hợp lượng lớn knowledge trong một workspace. ([Nguồn](https://blog.google/innovation-and-ai/products/notebooklm-goes-global-support-for-websites-slides-fact-check/))      |
| 09/2024    | ⭐ **Audio Overviews**: Biến source thành cuộc thảo luận dạng podcast giữa hai AI hosts                         | Q&A và summary đã giúp đọc nhanh hơn nhưng user vẫn phải chủ động ngồi đọc. Google thử biến knowledge thành một format có thể nghe và tiêu thụ thụ động.                           | **Định nghĩa "Tốt"**: Đừng tối ưu "AI tạo summary hay nhất"; tối ưu outcome thực sự — user hiểu được knowledge với effort thấp hơn. ([Nguồn](https://blog.google/innovation-and-ai/products/notebooklm-audio-overviews/))                                                                       |
| 12/2024    | **Interactive Audio**: User có thể tham gia cuộc hội thoại và hỏi AI hosts                                     | Audio Overview được đón nhận mạnh nhưng trải nghiệm ban đầu vẫn một chiều: AI nói → user nghe.                                                                                     | **Vòng Lặp Học (Learning Loop)**: AI giải thích → user hỏi → AI điều chỉnh → user hiểu hơn. Output không phải điểm cuối; feedback của user tạo thành một learning loop. ([Nguồn](https://blog.google/innovation-and-ai/models-and-research/google-labs/notebooklm-new-features-december-2024/)) |
| 05/2025    | **NotebookLM Mobile**: Đưa notebook và Audio Overviews lên điện thoại                                          | Audio tạo ra context sử dụng mới: user có thể học khi đi đường, tập thể thao hoặc không ngồi trước máy tính. Mobile cũng là yêu cầu phổ biến từ users.                             | **JTBD > Feature**: Sản phẩm phải xuất hiện ở context nơi job thực sự xảy ra, thay vì buộc user quay về interface ban đầu. ([Nguồn](https://blog.google/innovation-and-ai/products/notebooklm-app/))                                                                                            |
| 07/2025    | ⭐ **Video Overviews + Studio**: Knowledge có thể chuyển thành visual explanation bên cạnh text/audio           | Audio phù hợp với multitasking nhưng không phải kiến thức nào cũng truyền đạt tốt bằng âm thanh; diagram/process/visual concepts cần representation khác.                          | **x10 qua Representation**: AI không chỉ tạo content nhanh hơn mà cho phép một source of truth → nhiều representation, phù hợp với từng nhu cầu/context. ([Nguồn](https://blog.google/innovation-and-ai/models-and-research/google-labs/notebooklm-video-overviews-studio-upgrades/))           |
| 09/2025    | ⭐ **Flashcards, Quizzes & Learning Outputs**: Chuyển source thành nội dung luyện tập/kiểm tra kiến thức        | Summary, Audio và Video giúp user tiếp nhận kiến thức nhưng chưa chứng minh user thực sự hiểu và nhớ. Learning outputs bắt đầu đóng vòng từ consumption → practice.                | **Vòng Lặp Học + Định nghĩa "Tốt"**: Success không còn là "AI tạo output tốt" mà là user có học được không: Learn → Test → Feedback → Identify gap → Learn again. ([Nguồn](https://blog.google/innovation-and-ai/models-and-research/google-labs/notebooklm-student-features/))                 |
| 07/2026    | ⭐ **NotebookLM → Gemini Notebook**: Đưa sâu hơn vào Gemini/Search và hệ sinh thái Google                       | NotebookLM đã đạt quy mô lớn; Google chuyển từ các AI experiment riêng lẻ sang một Gemini ecosystem thống nhất.                                                                    | **Moat > Wrapper**: Khi model ngày càng giống commodity, distribution + ecosystem + context + workflow trở thành lợi thế khó bị model thế hệ tiếp theo hấp thụ. ([Nguồn](https://blog.google/innovation-and-ai/products/gemini-notebook/notebooklm-gemini-notebook/))                           |

**Vì sao chọn những mốc này:** Nhóm chọn 8 cột mốc này vì mỗi mốc đánh dấu một bước ngoặt lớn về mặt tư duy sản phẩm: (1) Xác lập vị thế Grounded AI (05–07/2023), (2) Nâng cấp hạ tầng xử lý dữ liệu quy mô x10 (06/2024), (3) Pivot định dạng tiêu thụ thụ động Audio (09/2024), (4) Tăng tính tương tác 2 chiều (12/2024), (5) Mở rộng ngữ cảnh sử dụng di động (05/2025), (6) Đa dạng hóa biểu diễn kiến thức bằng Visual/Video (07/2025), (7) Khép kín vòng lặp học chủ động với Flashcards/Quizzes (2025–26), và (8) Thương mại hóa & gắn kết vào hệ sinh thái Gemini (07/2026). Các bản vá lỗi nhỏ hoặc cập nhật giao diện phụ bị loại bỏ vì không đại diện cho bước chuyển dịch định hướng chiến lược.

---

## §2. Tệp user & JTBD

| | Early adopters (2023–2024) | Tệp hiện tại (2025–2026) |
|---|---|---|
| **Đặc điểm** | Nghiên cứu sinh, sinh viên, học thuật, AI enthusiasts nghiện đọc tài liệu PDF dài trên máy tính. | Học sinh/sinh viên ôn thi, người đi làm học kỹ năng mới, Podcasters/Content Creators, Người học qua thính giác & thị giác trên di động. |
| **JTBD chính** | "Giúp tôi tóm tắt và trích dẫn chính xác 20 bài báo khoa học PDF để viết luận văn mà không lo AI chém gió." | "Giúp tôi biến đống tài liệu/video khô khan thành Podcast để nghe khi đi đường, tạo Video để xem sơ đồ, và Flashcards/Quiz để luyện tập cho đến khi thực sự thuộc bài." |
| **Trước đó họ làm bằng cách nào** | Bấm `Ctrl+F` đọc lướt từng PDF, ghi chép ghi chú thủ công vào Notion/Obsidian. | Vừa làm thẻ Quizlet thủ công, vừa nghe thu âm bài giảng, vừa tìm video giải thích trên YouTube nhưng dữ liệu bị phân mảnh ở nhiều ứng dụng. |

**Dịch chuyển tệp:** Sự dịch chuyển tệp được thúc đẩy qua chuỗi mốc chiến lược: 
1. **Audio Overviews (09/2024)** & **Interactive Audio (12/2024)** giải phóng user khỏi màn hình máy tính, thu hút tệp mass-market ưa thích tiêu thụ âm thanh thụ động.
2. **Mobile Launch (05/2025)** xuất hiện đúng ngữ cảnh người dùng đang di chuyển (JTBD > feature).
3. **Video Studio (07/2025)** phục vụ người học qua thị giác (visual learners).
4. **Flashcards & Quizzes (2025–26)** biến công cụ từ "Đọc/Nghe tóm tắt" (Passive Consumption) thành "Hệ thống luyện tập & làm chủ kiến thức" (Active Mastery), thu hút mạnh mẽ tệp học sinh/sinh viên ôn thi và người luyện thi chứng chỉ chuyên môn.

**Switching cost (map 4 forces):**
- **Push of Present (Lực đẩy từ hiện tại):** Quá tải tài liệu khô khan; cảm giác đọc xong vẫn không nhớ hay hiểu sâu; thời gian ngồi trước màn hình máy tính quá dài.
- **Pull of New (Lực kéo từ giải pháp mới):** Khả năng chuyển 1 nguồn dữ liệu gốc (Single Source of Truth) thành Podcast nghe trên đường, Video giải thích trực quan, và Bộ Quiz tự luyện tập có AI chấm điểm & giải thích lỗ hổng tri thức.
- **Habit of Present (Thói quen cũ):** Thói quen ghi chú truyền thống, dùng Quizlet làm thẻ học độc lập, thói quen lưu file folder.
- **Anxiety of New (Nỗi lo giải pháp mới):** Nỗi lo AI tạo câu hỏi Quiz sai kiến thức hoặc làm mất đi tư duy phản biện tự nhiên khi tự làm bài.
- *Lực giữ người dùng mạnh nhất:* **Ecosystem Distribution & Single Source Multi-Representation Moat**. Khi toàn bộ tri thức, lịch sử luyện tập và thói quen học qua Audio/Video/Quizlet của người dùng đã nằm gói gọn trong Gemini Notebook và đồng bộ với hệ sinh thái Google (Search/Drive/Workspace), switching cost trở nên cực kỳ cao.

---

## §3. Ba dự đoán hướng đi (6–12 tháng tới)

### Dự đoán 1 *(loại: mở rộng tính năng / workflow)*
- **Dự đoán:** Gemini Notebook sẽ tung ra tính năng **Personalized Adaptive Learning & Mastery Graph** — AI tự động phân tích kết quả làm Quizzes/Flashcards của người dùng, phát hiện chính xác lỗ hổng tri thức (knowledge gap) và tự đề xuất lộ trình ôn tập lặp lại ngắt quãng (Spaced Repetition).
- **Lập luận:** Dẫn từ mốc **2025–26 (Flashcards, Quizzes & Learning Outputs)** ở §1. Khi sản phẩm đã chuyển từ "Consumption" sang "Practice", bước tiếp theo tất yếu là đóng vòng lặp học: *Learn → Test → Feedback → Identify gap → Learn again* (§2).

### Dự đoán 2 *(loại: mở rộng segment / mô hình kiếm tiền)*
- **Dự đoán:** Google sẽ mắt gói **Gemini Notebook for Education & Enterprise Team Workspaces** với khả năng chia sẻ Notebook động cho cả lớp học/đội ngũ doanh nghiệp, cho phép giáo viên/quản lý giao bài tập Quiz và theo dõi tiến độ học tập thực tế.
- **Lập luận:** Dẫn từ mốc **07/2026 (NotebookLM → Gemini Notebook)** và **05/2025 (Mobile)**. Khi NotebookLM đã trở thành một phần của hệ sinh thái Gemini/Google Workspace, lợi thế phân phối (distribution moat) cho phép Google chiếm lĩnh phân khúc trường học và doanh nghiệp.

### Dự đoán 3 *(loại: đe dọa Big Tech & trải nghiệm người dùng)*
- **Dự đoán:** Tích hợp **Real-time Multimodal Live Tutor** — người dùng có thể mở camera chiếu vào bài tập vẽ/sơ đồ thực tế hoặc nói chuyện trực tiếp với AI Tutor để cùng giải bài tập trên bảng trắng điện tử (Canvas).
- **Lập luận:** Dẫn từ mốc **12/2024 (Interactive Audio)** và **07/2025 (Video Overviews + Studio)**. Trải nghiệm đa phương tiện 2 chiều là hướng phát triển tự nhiên để tối ưu hóa outcome thực sự của người học (§2).

---

## §4. AI Log

| Việc | AI làm hay nhóm làm? | Nhóm kiểm chứng/phán đoán lại thế nào? |
|---|---|---|
| Tổng hợp dữ liệu & 8 mốc tiến hóa chiến lược | Nhóm chọn mốc & AI trợ giúp tra cứu link | Nhóm tự tay lựa chọn 8 cột mốc trọng yếu nhất từ 2023–2026, đối chiếu với blog chính thức của Google để kiểm chứng tính xác thực. |
| Revert nguyên lý cốt lõi cho 8 mốc | Nhóm | Nhóm trực tiếp thảo luận và revert nguyên lý cho từng mốc (Wrapper→Moat, x10 Capacity, Định nghĩa Tốt, Vòng lặp học, JTBD>Feature, Single Source Multi-Representation,...). |
| Phân tích tệp user (JTBD, 4 Forces) & 3 Dự đoán | Nhóm kết hợp AI | AI gợi ý cấu trúc tổng hợp; nhóm phản biện chi tiết, gắn chặt chuyển dịch tệp user từ Consumption sang Practice và mài sắc 3 dự đoán trỏ về mốc §1–§2. |
