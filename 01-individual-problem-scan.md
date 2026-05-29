## 01 — Individual Problem Scan
## Scan rộng

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Học viên trái ngành không load kịp kiến thức khi học lab buổi chiều do lượng kiến thức tăng quá nhanh | Học viên trái ngành | 5-10 người/buổi phải hỏi lại mentor, nhiều người không hoàn thành lab đúng giờ |
| 2 | Tốn thời gian | Tài liệu học tập mở quá sát giờ học nên không kịp ôn trước | Học viên | Nhiều người vào lớp mới đọc slide nên bị mất nhịp từ đầu buổi |
| 3 | AI có thể tốt hơn | Không có AI tutor hỗ trợ recap kiến thức nền hoặc giải thích nhanh thuật ngữ | Học viên trái ngành | Mentor bị hỏi lại cùng một dạng câu hỏi nhiều lần mỗi buổi |
| 4 | AI có thể tốt hơn | Thiếu API key hoặc môi trường thực hành khiến việc học bị gián đoạn | Học viên | Có người không chạy được lab trong 30-60 phút đầu buổi |
| 5 | Pain từ người khác | App điểm danh khó sử dụng ở thời gian đầu | Học viên | Nhiều câu hỏi lặp lại trên group/chat trong tuần đầu |
| 6 | Pain từ người khác | Team project mất cân bằng kỹ năng | Học viên | Team nhiều tech, ít non-tech, một vài người phải làm phần lớn project |
| 7 | Pain từ người khác | Không có cam kết hoặc định hướng rõ ràng về cơ hội việc làm sau khóa học | Học viên | Câu hỏi “học xong làm được gì?” xuất hiện nhiều trong Q&A/group chat |
| 8 | Pain từ người khác | Bài test đầu vào quá đơn giản so với độ khó thực tế khi vào học | Học viên | Nhiều người bị “shock” sau 1-2 buổi đầu và không theo kịp tiến độ |
| 9 | AI có thể tốt hơn | Không có hệ thống cá nhân hóa tốc độ học cho người nền tảng yếu/mạnh khác nhau | Học viên | Người yếu bị quá tải, người mạnh phải chờ tiến độ chung của lớp |

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Tài liệu học tập mở quá sát giờ học nên không kịp ôn trước | Đây là pain xảy ra thường xuyên, ảnh hưởng nhiều người và tác động trực tiếp tới khả năng theo kịp buổi học | Chưa chắc việc mở tài liệu sớm có giúp cải thiện hiệu quả học rõ rệt không |
| 2 | Học viên trái ngành không load kịp kiến thức khi học lab buổi chiều do lượng kiến thức tăng quá nhanh | Pain lớn và thực tế với nhiều học viên trái ngành, có dấu hiệu thật rõ ràng | Chưa xác định được nguyên nhân chính là do nền tảng yếu hay tốc độ dạy quá nhanh |
| 3 | Không có AI tutor hỗ trợ recap kiến thức nền hoặc giải thích nhanh thuật ngữ | Có tiềm năng AI rõ ràng, giảm tải mentor và hỗ trợ học viên học chủ động hơn | Chưa chắc học viên sẽ dùng thường xuyên thay vì hỏi mentor trực tiếp |

## Problem Card #1

**Problem 1 câu:**  
Học viên không có đủ thời gian ôn trước vì tài liệu thường được mở quá sát giờ học, dẫn đến mất nhịp và khó theo kịp lab.

**Actor:**  
Học viên

**Thời điểm / bối cảnh:**  
Trước buổi học vài giờ hoặc ngay khi buổi học bắt đầu.  
Đặc biệt ở các buổi lab kiến thức mới/chuyên sâu.

**Current workflow:**

```text
CURRENT STATE — 75 phút đầu buổi/lab

+--------------------+     +--------------------+     +--------------------+
| 1 Nhận tài liệu    | --> | 2 Đọc vội slide   | --> | 3 Gặp thuật ngữ   |
|   sát giờ          |     |   + lab guide      |     |   /concept mới    |
|   1'               |     |   15'              |     |   10'             |
+--------------------+     +--------------------+     +--------------------+
                                                               |
                                                               v
+--------------------+     +--------------------+     +--------------------+
| 6 Làm tiếp chậm    | <-- | 5 Hỏi mentor       | <-- | 4 Vừa học lý      |
|   /mất nhịp        |     |   câu cơ bản       |     |   thuyết + lab    |
|   14'              |     |   15'              |     |   20' 🔴          |
+--------------------+     +--------------------+     +--------------------+
          |
          v
+--------------------+
| 7 Không hoàn thành |
|   lab đúng giờ     |
|   /tự ôn lại       |
|   sau lab          |
+--------------------+

🔴 = Bottleneck: phải vừa đọc kiến thức mới vừa làm lab trong cùng một thời điểm.
```

**Bottleneck:**  
Không có thời gian chuẩn bị kiến thức nền trước buổi học.  
Kiến thức mới xuất hiện quá nhiều trong thời gian ngắn.

**Impact:**  
Học viên bị quá tải.  
Không theo kịp tiến độ, giảm chất lượng đầu ra.  
Mentor mất nhiều thời gian support câu hỏi lặp lại.  
Một số học viên mất động lực vì không theo kịp.

**Success metric:**  
Tài liệu được mở trước ít nhất 1 ngày.  
Tăng số học viên hoàn thành lab đúng giờ.  
Học viên self-report hiểu bài tốt hơn.

**Non-AI alternative:**  
Publish tài liệu sớm hơn.  
Có checklist prerequisite trước mỗi buổi.  
Gửi video/tóm tắt kiến thức nền trước giờ học.

**AI hypothesis:**  
AI có thể tự động tạo recap/prerequisite ngắn từ slide hoặc lab.  
AI recommend phần cần đọc trước dựa trên trình độ học viên.  
AI chatbot giải thích nhanh thuật ngữ trước buổi học.

**Quick gut:**  
No AI / process fix

### Draft future workflow

```text
FUTURE STATE — 30 phút chuẩn bị trước buổi học

+--------------------+     +--------------------+     +--------------------+
| 1 Mở tài liệu      | --> | 2 AI tạo recap     | --> | 3 Học viên đọc    |
|   trước 1 ngày     |     |   + checklist      |     |   prerequisite    |
|   1'               |     |   3'               |     |   15'             |
+--------------------+     +--------------------+     +--------------------+
                                                               |
                                                               v
+--------------------+     +--------------------+     +--------------------+
| 6 Vào lab đúng     | <-- | 5 Mentor check     | <-- | 4 AI giải thích   |
|   nhịp hơn         |     |   nhanh điểm khó   |     |   thuật ngữ khó   |
|   1'               |     |   5' 🟢            |     |   5'              |
+--------------------+     +--------------------+     +--------------------+

🟢 = Human boundary: mentor/giảng viên vẫn duyệt checklist và giải thích điểm quan trọng.
Fallback: AI recap thiếu hoặc sai -> học viên quay lại slide/lab guide gốc và hỏi mentor.
```

## Problem Card #2

**Problem 1 câu:**  
Học viên trái ngành không load kịp kiến thức khi học lab do tốc độ học và độ khó tăng quá nhanh.

**Actor:**

* Học viên trái ngành

**Thời điểm / bối cảnh:**

* Trong các buổi lab chiều hoặc các buổi kiến thức chuyên sâu
* Đặc biệt sau 1-6 tuần đầu của khóa học

**Current workflow:**

```text
CURRENT STATE — 90 phút trong buổi lab chuyên sâu

+--------------------+     +--------------------+     +--------------------+
| 1 Ôn nền cơ bản    | --> | 2 Vào lab chuyên  | --> | 3 Mentor giải     |
|   trước đó         |     |   sâu              |     |   thích nhanh     |
|   10'              |     |   5'               |     |   10'             |
+--------------------+     +--------------------+     +--------------------+
                                                               |
                                                               v
+--------------------+     +--------------------+     +--------------------+
| 6 Hỏi mentor       | <-- | 5 Gặp lỗi/tool     | <-- | 4 Chưa hiểu       |
|   liên tục         |     |   mới khi code     |     |   context nhưng   |
|   20'              |     |   20'              |     |   vẫn theo lớp    |
+--------------------+     +--------------------+     |   15' 🔴          |
          |                                             +--------------------+
          v
+--------------------+
| 7 Bỏ dở hoặc       |
|   không hoàn thành |
|   lab              |
|   10'              |
+--------------------+

🔴 = Bottleneck: chênh lệch context/kiến thức nền khiến học viên mất flow giữa lab.
```

**Bottleneck:**

* Chênh lệch lớn giữa kiến thức đầu vào và độ khó thực tế
* Người trái ngành thiếu context IT/workflow thực tế

**Impact:**

* Học viên bị quá tải
* Không hoàn thành lab đúng giờ
* Mentor bị overload support
* Một số học viên mất động lực hoặc bỏ cuộc

**Success metric:**

* Tăng số học viên hoàn thành lab đúng giờ
* Giảm số câu hỏi cơ bản lặp lại
* Giảm số học viên bị “mất flow” giữa buổi
* Tăng self-report confidence của học viên

**Non-AI alternative:**

* Chia lớp theo level
* Có lớp foundation trước khóa chính
* Giảm tốc độ hoặc chia nhỏ lab

**AI hypothesis:**

* AI detect học viên đang “kẹt” ở bước nào
* AI giải thích lại concept theo level người học
* AI generate roadmap/prerequisite cá nhân hóa

**Quick gut:**
Agent

### Draft future workflow

```text
FUTURE STATE — 45 phút hỗ trợ theo level

+--------------------+     +--------------------+     +--------------------+
| 1 Pre-check level  | --> | 2 AI gợi ý        | --> | 3 AI giải thích   |
|   trước lab        |     |   prerequisite    |     |   concept theo    |
|   5'               |     |   roadmap         |     |   level           |
+--------------------+     |   5'              |     |   10'             |
                           +--------------------+     +--------------------+
                                                               |
                                                               v
+--------------------+     +--------------------+     +--------------------+
| 6 Mentor xử lý     | <-- | 5 Học viên hỏi    | <-- | 4 Lab chia thành |
|   case khó         |     |   AI tại bước kẹt |     |   checkpoint nhỏ |
|   10' 🟢           |     |   5'              |     |   10'             |
+--------------------+     +--------------------+     +--------------------+

🟢 = Human boundary: mentor vẫn xử lý lỗi lạ, case khó và điều chỉnh tốc độ lớp.
Fallback: AI giải thích không đúng context -> mentor quay lại mini-explain hoặc chia nhỏ lab hơn.
```

## Problem Card #3

**Problem 1 câu:**  
Không có AI tutor hỗ trợ recap kiến thức nền hoặc giải thích nhanh thuật ngữ khiến mentor phải trả lời lặp lại nhiều lần.

**Actor:**

* Học viên trái ngành
* Mentor bị quá tải support

**Thời điểm / bối cảnh:**

* Trong lúc học lab
* Khi gặp thuật ngữ mới hoặc lỗi kỹ thuật
* Sau giờ học khi tự học lại

**Current workflow:**

```text
CURRENT STATE — 65 phút/cụm câu hỏi lặp lại trong lab

+--------------------+     +--------------------+     +--------------------+
| 1 Gặp thuật ngữ    | --> | 2 Không hiểu       | --> | 3 Google thủ công |
|   /concept mới     |     |   nhưng lớp vẫn    |     |   hoặc hỏi mentor |
|   5'               |     |   chạy tiếp        |     |   10'             |
+--------------------+     |   5'               |     +--------------------+
                           +--------------------+              |
                                                               v
+--------------------+     +--------------------+     +--------------------+
| 6 Flow lớp bị      | <-- | 5 Nhiều người      | <-- | 4 Mentor trả lời  |
|   chậm lại         |     |   hỏi lại tương tự |     |   thủ công        |
|   10'              |     |   15'              |     |   20' 🔴          |
+--------------------+     +--------------------+     +--------------------+

🔴 = Bottleneck: mentor phải giải thích thủ công cùng một nhóm câu hỏi cho nhiều học viên.
```

**Bottleneck:**

* Không có hệ thống hỗ trợ giải thích theo trình độ người học
* Mentor phải trả lời lặp lại nhiều câu giống nhau

**Impact:**

* Mentor quá tải support
* Học viên phụ thuộc mentor
* Flow lớp học bị gián đoạn
* Người yếu ngày càng chậm hơn

**Success metric:**

* Giảm số câu hỏi lặp lại cho mentor
* Tăng tốc độ tự giải quyết vấn đề của học viên
* Tăng completion rate của lab
* Học viên phản hồi hiểu bài tốt hơn

**Non-AI alternative:**

* FAQ/document tổng hợp
* Video recap kiến thức nền
* Session phụ đạo ngoài giờ

**AI hypothesis:**

* AI tutor có thể explain concept theo nhiều level
* AI trả lời dựa trên context bài lab hiện tại
* AI recap nhanh kiến thức prerequisite khi học viên bị kẹt

**Quick gut:**
Agent


### Draft future workflow

```text
FUTURE STATE — 25 phút với AI tutor theo context lab

+--------------------+     +--------------------+     +--------------------+
| 1 Học viên hỏi     | --> | 2 AI tìm trong     | --> | 3 AI giải thích   |
|   AI tutor         |     |   slide/lab/FAQ    |     |   theo level      |
|   1'               |     |   2'               |     |   3'              |
+--------------------+     +--------------------+     +--------------------+
                                                               |
                                                               v
+--------------------+     +--------------------+     +--------------------+
| 6 Mentor review    | <-- | 5 AI hỏi thêm      | <-- | 4 Học viên thử    |
|   câu khó          |     |   nếu thiếu        |     |   áp dụng lại     |
|   6' 🟢            |     |   context          |     |   8'              |
+--------------------+     |   5'               |     +--------------------+
                           +--------------------+

🟢 = Human boundary: mentor xử lý câu hỏi khó, lỗi lạ hoặc khi AI không chắc.
Fallback: AI trả lời mơ hồ -> học viên gửi câu hỏi kèm context cho mentor.
```
